Sendy-WPCF
==========

### Differences from CrystalAsia/sendywpcf
- The original plugin uses an [acceptance] field, which prevents the form from submitting if not checked. E-mail signup should be opt-in and should not prevent the form from submitting. Use a regular `<input>` field instead, as seen in the example below.
- `name` is a reserved field in WP Contact Form 7, so it can't actually be used as the name for e-mail opt-in. This uses different fieldnames instead

### Original readme (with updated example)
Sendy integration for WP Contact Form 7 (https://wordpress.org/plugins/contact-form-7/) that we use for Awesome Presentation (awesome-presentation.com). Because the other plugins were featureless, complicated and mostly people use the Contact Form plugin anyway.

It's pretty easy and automatic. Just change the line to your Sendy location:

``$sendyUrl = "http://www.yoursendy.com/subscribe";``

Then use the Contact Form 7 to build you form like so:

```
<p>Name *<br />
    [text* your-name] </p>

<p>Your Email *<br />
    [email* your-email] </p>

<p><input type="checkbox" name="sendy_subscribe" value="1" checked /> Yes! Sign me up for the BETA list!</p>

[sendywpcf id=""]

[quiz quiz-44 "4+2=?|6" "2+10=?|12" "X+Y=?|Z" "33+33=?|66" "A+B=?|C"]

<p>[submit "Sign ME Up!"]</p>
```

In the shortcode [sendywpcd id=""] add in your list id from Sendy. I recommend a quiz, and acceptance checkbox. I also recommend double opt-in on the Sendy side :)
