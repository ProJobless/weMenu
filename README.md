weMenu
======

Modul for OpenCart

##

Использвание в любом шаблоне:

```php
<?php if($we_menu_cache = $this->config->get('we_menu_cache')){ ?> 
    <ul class="<?php echo $this->config->get('we_menu_class') ?>">
        <?php if(!empty($we_menu_cache)){ ?>
            <?php foreach($we_menu_cache as $item){ 
                $tpl = strpos($item['href'], $_SERVER['REQUEST_URI']) && $_SERVER['REQUEST_URI'] != '/'  ? 'tpl_row_act' : 'tpl_row';
                echo html_entity_decode($item[$tpl]); 
                } ?>
        <?php } ?>
    </ul>
<?php } ?>
```