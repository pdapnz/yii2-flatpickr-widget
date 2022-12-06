Flatpickr JS Widget for Yii2
====================================

[![Latest Stable Version](http://poser.pugx.org/cgsmith/yii2-flatpickr-widget/v)](https://packagist.org/packages/cgsmith/yii2-flatpickr-widget) 
[![Total Downloads](http://poser.pugx.org/cgsmith/yii2-flatpickr-widget/downloads)](https://packagist.org/packages/cgsmith/yii2-flatpickr-widget) 
[![Latest Unstable Version](http://poser.pugx.org/cgsmith/yii2-flatpickr-widget/v/unstable)](https://packagist.org/packages/cgsmith/yii2-flatpickr-widget) 
[![License](http://poser.pugx.org/cgsmith/yii2-flatpickr-widget/license)](https://packagist.org/packages/cgsmith/yii2-flatpickr-widget) 


Renders a [flatpickr Datepicker plugin](https://flatpickr.js.org/).

Installation
------------
The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```bash
$ composer require cgsmith/yii2-flatpickr-widget:~1.0
```
or add

```json
"cgsmith/yii2-flatpickr-widget": "~1.0"
```

to the require section of your application's `composer.json` file.

Usage
-----
The widget renders the flatpickr onto your form.

***Example of use with a form***  
Use the widget by setting up its `model` and `attribute`.

```php
<?php
use cgsmith\flatpickr\FlatpickrWidget;

// as a widget
?>

<?= FlatpickrWidget::widget([
    'model' => $model,
    'attribute' => 'date',
]);?>


<?php 
// additional config options for flatpickr

echo $form->field($model, 'date')->widget(
    FlatpickrWidget::widget([
    'model' => $model,
    'attribute' => 'date',
    'flatpickrConfig' => [ // This is passed as a JSON object to flatpickr
        'enableTime' => false,
        'dateFormat' => 'F j, Y H:i',
        'altInput' => true,
        'altFormat' => 'F j, Y',
    ]
]);
?>
```  

Resources Information
-------------------
Please, check the [flatpicker site](https://flatpickr.js.org/options/) documentation for further information about its configuration options.

Contributing
------------

Contributions are welcome! 

Credits
-------

- [Chris Smith](https://github.com/cgsmith)
- [All Contributors](../../contributors)

License
-------

The BSD License (BSD). Please see [License File](LICENSE.md) for more information.
