=== Subscribe to Comments ===

Tags: subscribe, notification, email, comments
Contributors: MarkJaquith

Subscribe to Comments is a WordPress plugin that allows commenters on your blog to click a "subscribe to comments" checkbox and receive e-mail notification for subsequent comments to the entry they commented on.  It is based loosely off Jennifer Stuart's Subscribe to Comments version 1, but was completely re-written for version 2.0  The plugin includes functionality for people to subscribe to comment notifications without having to leave a comment on the entry.  This can really help to foster a sense of community and connectedness on blogs that don't receive massive ammounts of comments on posts.  If your blog typically gets 2-20 comments per post, those comments may be spread over a longer time period and people may have forgotten about their comment and will never see the responses.  Comment RSS feeds are one solution, but not a particularly user-friendly way.  Everyone uses e-mail, so this plugin serves a vital function.

The plugin is highly configurable, through the WordPress admin interface.  There are three types of text shown to users where the "subscribe to comments" checkbox goes: the "subscribe" checkbox, the "you are the author" text, and the "you are subscribed to this entry" text.  The latter two have links to the powerful Subscription Manager, which lets users remove subscriptions, block all subscriptions, or globally change their notification e-mail address for all their comments (the latter two are verified using e-mail).  WordPress admins of level 8 or above can edit anyone's subscriptions, or remove a block.

The Subscription Manager is highly configurable.  With the click of one option, you can integrate it into your existing site's design, using your header and footer, and of course using your own CSS to modify how the manager looks.

== Installation ==

1. Put subscribe-to-comments.php into [wordpress_dir]/wp-content/plugins/
2. Put wp-subscription-manager.php into your blog's root WordPress directory (the directory where wp-config.php resides)
3. Go into the WordPress admin interface and activate the plugin
4. Optional: if your WordPress 1.5 theme doesn't have the comment_form hook, or if you would like to manually determine where in your comments form the subscribe checkbox appears, enter this where you would like it: <?php show_subscription_checkbox(); ?>
NOTE: Be sure that you place this within the comment form... i.e. between <form> and </form>
5. Optional: If you would like to enable users to subscribe to comments without having to leave a comment, place this somewhere in your template, but make sure it is outside the comments form. A good place would be right after the ending </form> tag for the comments form: <?php show_manual_subscription_form(); ?>



== Frequently Asked Questions ==

= How easy is it for users to unsubscribe to e-mail notifications? =

Extremely easy.  Their specially encoded link to the Subscription Manager is included in the comment form of the entry to which they subscribed, as well as at the bottom of every comment notification e-mail they get (for any entry).  After clicking this link, it takes one click to select the entry they wish to unsubscribe, and one more click to complete the unsubscription.

Blocking all e-mail notifications (really just there in case some prankster is signing other people up for notifications) is also easy.  After entering the Subscription Manager, one click requests the block, and one click on the link in the verification e-mail completes the process.

= I want the "subscribe to comments" checkbox to be checked by default, can I do this? =

Yes!  Go to Options -> Subscribe to Comments and select the ["Subscribe" box should be checked by default] option and click "Update Options"