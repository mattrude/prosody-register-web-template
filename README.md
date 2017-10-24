# Prosody mod_register_web Template
This repository holds the Prosody [mod_register_web](https://modules.prosody.im/mod_register_web.html) templates for my Jekyll 
[xmpp-site](https://github.com/mattrude/xmpp-site) and [xmpp-site-lite](https://github.com/mattrude/xmpp-site-lite) themes.

### Features

* bootstraps v3.3.7
* reCAPTCHA support

## Installing Template

1. You must install the [prosody](https://prosody.im) module [mod_register_web](https://modules.prosody.im/mod_register_web.html) on your prosody server before this template will be used.
   1. Add the module as you would any other module, by adding:
    `modules_enabled = {
        "mod_register_web";
    }`

2. Download the template from this repository and place it on your prosody server.
3. In your `prosody.cfg.lua` file, add the following line pointing to the location you saved this repository.

    `register_web_template = "/path/to/your/custom-templates"`

4. Once complete, reload your prosody server.


### reCAPTCHA Support

This template supports reCAPTCHA, to prevent bots from creating accounts on your server, to enable, add the below lines to your `prosody.cfg.lua` file.   You will need to replace the values with the keys recived from the [reCAPTCHA](https://developers.google.com/recaptcha/) site.

    captcha_options = {
      recaptcha_public_key = "78901";
      recaptcha_private_key = "12345";
    }
