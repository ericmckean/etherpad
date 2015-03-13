## File upload and import/export ##

We used a proprietary servlet library to process file uploads.  Consequently, we were unable to include that library with this open source release, and we had to comment out its usage.  (See infrastructure/net.appjet.oui/main.scala and infrastructure/net.appjet.oui/execution.scala).

In addition, import from/export to formats such as DOC or PDF requires integration with open-office, which is a bit of a mess. However, txt and html export do not require open-office or the proprietary servlet library, which means it is easy to export your pads into those formats.

## Email invitations ##

Email invitations were sent using our authsmtp account, but we didn't want to distribute our authsmtp username/password with the release, so we removed those command-line flags.  It should be easy to hook up email sending to your own smtp server.  The end result is that email sending does not work out of the box.

## Professional Accounts ##

Professional accounts do not currently work out of the box because the sign-up process requires sending an email, and emails don't work (see above).  If you can get emails to work, then the professional signup should work as well.  (Just navigate to /ep/pro-signup/.)