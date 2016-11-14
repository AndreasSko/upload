# Upload by ![flagrow logo](https://avatars0.githubusercontent.com/u/16413865?v=3&s=15) [flagrow](https://discuss.flarum.org/d/1832-flagrow-extension-developer-group)

[![Latest Stable Version](https://poser.pugx.org/flagrow/upload/v/stable)](https://packagist.org/packages/flagrow/upload) [![Total Downloads](https://poser.pugx.org/flagrow/upload/downloads)](https://packagist.org/packages/flagrow/flarum-ext-:package)

An extension that handles file uploads intelligently for your forum. This is the descendant of the Flagrow image upload extension.

![image demo](https://discuss.hyn.me/assets/files/2016-11-04/06:25:460-test-gif)

### goals

- [Intelligently delete images](https://github.com/flagrow/upload/issues/7)
- [Send notifications](https://github.com/flagrow/upload/issues/8)
- [Prevent upload of malevolent files](https://github.com/flagrow/upload/issues/9)
- Support a wide bunch of upload systems (anything support by the League flysystem will work) that provides an URL to access the file
- Intelligently provide markdown strings per mime type

For a complete overview of our releases, please visit the [milestones tracker](https://github.com/flagrow/upload/milestones) on Github.

### installation

```bash
composer require flagrow/upload
```

### updating

```bash
composer update flagrow/upload
php flarum cache:clear
```

### configuration

Enable the extension, a new tab will appear on the left hand side. This separate settings page allows you to further configure the extension.

### donate

If you're happy with this extension, feel free to [buy me a cup of coffee](https://paypal.me/luceos/5).

---

### changelog

Please visit the [thread](https://discuss.flarum.org/d/4154-flagrow-file-upload-the-intelligent-file-attachment-extension).

Check [future milestones](https://github.com/flagrow/upload/milestones).

### links

- [on github](https://github.com/flagrow/upload)
- [on packagist](http://packagist.com/packages/flagrow/upload)
- [issues](https://github.com/flagrow/upload/issues)
- [flagrow group information](http://flagrow.github.io/)

> Flagrow is a collaboration of Flarum extension developers to provide quality, maintained extensions.

## FAQ

-  __AWS S3__: you will need to install the league AWS s3 adapter: `composer require league/flysystem-aws-s3-v3`, the aws-s3 choice will now pop up in the admin settings page.
-  __flarum-ext- prefix__: I am aware that the convention is to prefix an extension with `flarum-ext-`, after considerate investigation I came to the conclusion that using the exact package name flarum-ext-upload prevented me to enable the extension in the admin panel with an error "route not found".