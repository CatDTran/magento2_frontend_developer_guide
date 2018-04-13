# Magento 2 Front End Developer Guide Course

This is a code repo following the **Magento 2 - Front End Developer Guide** course on youtube.com by **Andy Myers** https://www.youtube.com/user/PixieSkyTV

### Adding custom favicon:
These are  the steps to add your own favicon to your theme. Let's say you have a favicon called `favicon-32x32.png`:
+ First copy `favicon-32x32.png` to `<your_theme_dir>/Magento_Theme/web/` directory (create the parent folder `<your_theme_dir>/Magento_Theme` if not already exist):
+ Then add `<your_theme_dir>/Magento_Theme/layout/default_head_blocks.xml` file with the following content:
```xml
<page xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="urn:magento:framework:View/Layout/etc/page_configuration.xsd">
    <head>
        <link src="Magento_Theme::favicon-32x32.png" rel="icon" sizes="32x32" />
    </head>
</page>
```

### Notes:
+ New theme must have `media\preview.jpg`, otherwise Magento will throw 'No preview found' error.
+ Switch to developer mode when developing new theme: `deploy:mode:set developer`
