# ImagePlaceholder
Processwire module for easy creation of placeholder images on the frontend. Uses true type fonts for the text.

## Configuration options
- Set the default text for the placeholder image (multilanguage)
- Set the default background color for the image in hexadecimal color code
- Set the default color for the text in hexadecimal color code
- Set the default font for the text from a select field
- Set the default fontsize

Additional font files in true type format (ttf) can be uploaded via an upload field.
Font files which are not longer needed can be selected and deleted.

## Methods
- setTextColor(string) 
- setBackgroundColor(string)
- setWidth(int)
- setHeight(int)
- setFontFamily(string)
- setFontSize(int)
- setText(string)

Use these methods to overwrite default values from the module configuration.

## Examples for usage in templates

### Usage with default values (only the size will be set manually)

`echo $modules->ImagePlaceholder->setWidth(800)->setHeight(400)->render();`

This will output the img src as base64 string.

### Usage with all parameters set individually (default values will be overwritten)

`echo $modules->ImagePlaceholder->setFontSize(30)->setWidth(800)->setHeight(400)->setBackgroundColor('#dddddd')->setTextColor('#000000')->setText('My placeholder')->setFontFamily('pacifico')->render(true);`

Take a look at the render method, which includes true as a boolean value. This means that a complete image tag will be rendered instead of only the src value.

## Multilanguage

The text for the placeholder can be set multilingual (in module configuration and via setText() method). By setting the text via setText() method in template, please use translateable strings(_('My text')) for multilanguage text.





