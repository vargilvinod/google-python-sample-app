SendGrid on Google App Engine
======================

This git repository helps you to send emails quickly and easily through SendGrid on Google App Engine using Python.


Running on Google App Engine
----------------------------

Create an SendGrid account at http://sendgrid.com/pricing.html

Create an account at https://appengine.google.com/ and set up your local machine with the client tools https://developers.google.com/appengine/docs/python/gettingstartedpython27/devenvironment

Create an application on https://appengine.google.com/start/createapp

Clone project on your local machine
<pre>
    git clone https://github.com/sendgrid/google-python-sample-app
</pre>

###Configuration###
Configure `googleSendgridPython.py` file with your information:

Update the *&lt;sendgrid_username&gt;* and *&lt;sendgrid_password&gt;* with your SendGrid credentials.
```python
    s = Sendgrid('<sendgrid_username>', '<sendgrid_password>', secure = True)
```
Update the *&lt;from_address&gt;* with your email address
```python
    message = Message('<from_address>', subject, content, '')
```

Update application identifier in `app.yaml` file
```yaml
    application: application_identifier
```

Upload your application to Google App Engine
<pre>
    appcfg.py update google-sendgrid-python/
</pre>
That's it, you can now checkout your application at:
<pre>
    http://application_identifier.appspot.com/
</pre>

For more details about SendGrid libray please read http://sendgrid.com/docs/Code_Examples/python.html

