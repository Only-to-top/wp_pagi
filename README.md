# wp_pagi

```php
<!-- Pagination -->
<div class="page_nav">
    <?php
    $GLOBALS['wp_query']->max_num_pages = $mypost_Query->max_num_pages;
    the_posts_pagination(array(
        'type'=>'inline',
        'screen_reader_text' => __( '' ),
        'end_size'     => 1,
        'mid_size'     => 1,
        'prev_next'    => True,
        'prev_text'    => __('<i class="fa fa-angle-left"></i>'),
        'next_text'    => __('<i class="fa fa-angle-right"></i>'),
        'add_args'     => False
    ));
   ?>
</div>
```
