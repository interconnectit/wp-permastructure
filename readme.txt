=== WP Permastructure ===
Contributors: interconnectit, sanchothefat
Donate link: http://interconnectit.com/
Tags: permalinks, rewrite rules, custom post types, custom taxonomies, URLs, links
Requires at least: 3.3
Tested up to: 3.4.1
Stable tag: 1.2

Adds the ability to configure permalinks for custom post types using rewrite tags like %post_id% and %author%.

== Description ==

In addition to controlling your custom post type permalinks this plugin adds support for using custom taxonomies in your permalink structures as well.

Not only that but you can control the full permalink so the post type slug is not required at the start of the link.

Multiple post types can use the same permalink structure.

= Usage =

There are 2 ways to use this plugin:

**Permalink Settings**

The plugin adds fields to the permalinks settings page for any public facing custom post types.

**In Code**

When registering a post type you can add a value to the rewrite property with the key 'permastruct' to define your default permalink structure.

eg:

`
<?php

register_post_type( 'my_type', array(
    ...
    'rewrite' => array(
        'permastruct' => '/%custom_taxonomy_name%/%author%/%postname%/'
    ),
    ...
) );

?>
`

== Installation ==

1. You can install the plugin using the auto-install tool from the WordPress back-end.
2. To manually install, upload the folder `/wp-permastructure/` to `/wp-content/plugins/` directory.
3. Activate the plugin through the 'Plugins' menu in WordPress
4. You should now see input boxes for any custom post types you have on the permalink settings page


== Frequently Asked Questions ==

None so far.


== Screenshots ==

1. The extended permalink settings panel

== Changelog ==

* 1.2: Fixed attachment URL rewrites, fixed edge case where permastruct is %postname% only
* 1.1: Fixed problem with WP walk_dirs and using %category% in permalink - overly greedy match
* 1.0: Initial import
