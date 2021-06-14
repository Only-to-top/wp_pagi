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
        'prev_text'    => __('«'),
        'next_text'    => __('»'),
        'add_args'     => False
    ));
   ?>
</div>
```

### function.php

```php
// удаляение H2 из шаблона пагинации
add_filter('navigation_markup_template', 'my_navigation_template', 10, 2);
function my_navigation_template($template, $class)
{
    return '<nav class="navigation %1$s" role="navigation">
        <div class="nav-links">%3$s</div>
    </nav>';
}
```
