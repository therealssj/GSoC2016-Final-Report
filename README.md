![Google Summer of Code 2016](https://github.com/therealssj/GSoC2016-Final-Report/blob/master/static/gsoc.png "Google Summer of Code 2016")

My project for Google Summer of Code 2016 was **Port Google Login Authenticator To Drupal 8**. My organisation was [Drupal](https://drupal.org) which is an Open Source CMS framework written in PHP. I worked under the mentorship of [Adam Bergstein (nerdstein)](https://www.drupal.org/u/nerdstein) and [Peter Droogmans (attiks)](https://www.drupal.org/u/attiks).

**Project Details**

Though my main project was to port [Google Login Authenticator](https://www.drupal.org/project/ga_login) a Drupal 7 module to Drupal 8 later on we decided to merge it with the Drupal [Two Factor Authentication](https://www.drupal.org/project/tfa) module. So what was supposed to be a single module port turned into building a system for pluggable authentication plugins.

When I started working on the Two Factor module a port was already being worked on but had been inactive for sometime so I had two challenges:

- Complete the remaining functionality within the scope of my project.
- Even the ported code had some deprecated functionalities which needed to be removed.

Along side the Two Factor module I also worked on the Google Login Authenticator module but did not make any commits till I had some basic functionality worked out for the Two Factor Module.

**Plugin Architecture**

The Two Factor Module is just a pluggable provider. On its own it is of no use and needs external plugins/modules like Google Login Authenticator for the the site to be able to use it.

There are three types of plugins in Two Factor:
- Validation plugins like TFA Time Based OTP and TFA Hmac Based OTP.
- Login plugins like TFA Trusted Trusted Browser(Cookie based authentication)
- Send plugins ( No plugins implemented yet )
- Setup plugins ( Required to setup a authentication method )

The Two Factor Module comes with classes to handle the Authentication side but for the plugin to work you need Setup plugin classes like the Time Based OTP setup and Hmac Based OTP setup classes provided by the Google Login Authenticator.

If someone wants to implement a new authentication method they will need to provide the two classes one to handle the authentication and the other to handle the plugin setup. 

**Tasks Completed**

- Port Two factor Authentication Module to Drupal 8.
- Port Google Login Authentication Module to Drupal 8.
- Add Time Based OTP authentication and setup classes.
- Add Hmac Based OTP authentication and setup.
- Add Fallback authentication (Recovery Codes) authentication and setup classes.
- Add Cookie Based Authentication as TFA Trusted Browser ( Not a part of my project but existed in Two Factor Module from before )
- Add Flood Control.
- Add Basic Tests.
- Utilise the [encrypt](https://www.drupal.org/project/encrypt) module to handle the encryption.

**Repositories Contributed To**

- [Two Factor Module](https://github.com/d8-contrib-modules/tfa)

- [Google Login Authenticator](https://github.com/d8-contrib-modules/ga_login)

- We use an external library to handle the OTP side of the module and I also made some contributions to the library for some features that I needed in my project.
[OTP Library](https://github.com/ChristianRiesen/otp)

**Commits Made During The Project**

- [Two Factor Module](https://github.com/d8-contrib-modules/tfa/commits/master?author=therealssj)

- [Google Login Authenticator](https://github.com/d8-contrib-modules/tfa/commits/master?author=therealssj)

- [OTP Library](https://github.com/ChristianRiesen/otp/commits/master?author=therealssj) ([Pull Request](https://github.com/ChristianRiesen/otp/pull/12))

**Remaining issues**

- [Two Factor Module](https://github.com/d8-contrib-modules/tfa/issues)

- [Google Login Authenticator](https://github.com/d8-contrib-modules/ga_login/issues)

**Weekly Blog**

You can read the weekly blog posts for a much better insight into the work done during Google Summer of Code.
Here is the [link](http://techisdope.com/category/weekly-blog/).
