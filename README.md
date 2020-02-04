# ImagePlaceholder
Processwire module for easy creation of placeholder images on the frontend. Uses true type fonts for the text.

## Configuration options
- Set the default text for the placeholder image (multilanguage)
- Set the default background color for the image in hexadecimal color code
- Set the default color for the text in hexadecimal color code
- Set the default font for the text from a select field
- Set the default fontsize

Additional font files in true type format (ttf) can be uploaded via an upload field.

## Methods
- setTextColor(string) 
- setBackgroundColor(string)
- setWidth(int)
- setHeight(int)
- setFontFamily(string)
- setFontSize(int)
- setText(string)

Use this methods to overwrite default values from the module configuration.

## Examples for usage in templates

`echo $modules->ImagePlaceholder->setFontSize(30)->setWidth(800)->setHeight(400)->render();`





