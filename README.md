![Google Summer of Code 2016](https://github.com/therealssj/GSoC2016-Final-Report/blob/master/static/gsco.png "Google Summer of Code 2016")

My project for Google Summer of Code 2016 was **Port Google Login Authenticator To Drupal 8**. My organisation was [Drupal](https://drupal.org) which is an Open Source CMS framework written in PHP. I worked under the mentorship of [Adam Bergstein (nerdstein)](https://www.drupal.org/u/nerdstein) and [Peter Droogmans (attiks)](https://www.drupal.org/u/attiks).

**Project Details**

Though my main project was to port [Google Login Authenticator](https://www.drupal.org/project/ga_login) a Drupal 7 module to Drupal 8 later on we decided to merge it with the Drupal [Two Factor Authentication](https://www.drupal.org/project/tfa) module. So what was supposed to be a single module port turned into building a system for pluggable authentication plugins.

When I started working on the Two Factor module a port was already being worked on but had been inactive for sometime so I had two challenges:

- Complete the remaining functionality within the scope of my project.
- Even the ported code had some deprecated functionalities which needed to be removed.

Along side the Two Factor module I also worked on the Google Login Authenticator module but did not make any commits till I had some basic functionality worked out for the Two Factor Module.

**Tasks Completed**

- Port Two factor Authentication Module to Drupal 8.
- Port Google Login Authentication Module to Drupal 8.
- Add Time Based OTP authentication plugin to Two Factor Module and Google Login Autheticator.
- Add Hmac Based OTP authentication plugin to Two Factor Module and Google Login Autheticator.
- Add Fallback authentication (Recovery Codes) authentication plugin to Two Factor Module.
- Add Cookie Based Authentication as TFA Trusted Browser plugin( Not Part of my project but existed in Two Factor from before )

** Commits Made During The Project **

[Two Factor Module](https://github.com/d8-contrib-modules/tfa/commits/master?author=therealssj)

[Google Login Authenticator](https://github.com/d8-contrib-modules/tfa/commits/master?author=therealssj)

** Weekly Blog **

You can read the weekly blog posts for a much better insight into the work done during Google Summer of Code.
Here is the [link](http://techisdope.com/category/weekly-blog/)
