Custom Post Type Permalinks
===========================

Adds the ability to configure permalinks for custom post types using rewrite
tags like %post_id% and %author%.

## Usage:

When registering a post type you can add a value to the rewrite property with 
the key 'permastruct' to define your default permalink structure.

eg:

```php
<?php

register_post_type( 'my_type', array(
	...
	'rewrite' => array( 'permastruct' => '/%custom_taxonomy%/%author%/%postname%/' ),
 	...
) );

?>
```

Alternatively you can set the permalink structure from the permalinks settings 
page in admin.