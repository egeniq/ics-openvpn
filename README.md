eduVPN fork of OpenVPN for Android
=============

eduVPN changes
--------------
* [Moved the native libraries from the app to this submodule](a095efa4361f2ac4f26581104b33ca8a21ce2de9)
* [Added a static method which allows the app to open its own activity from the permanent notification](d83f545f466ea3b198bd88cf55d411a5f31a5955)
* [Added two public methods to the service to get the latest local IPv4 and IPv6 address](88a6088d972acda9ade78563d12bca97f3820f28)
* [Removed an incorrect annotation which made the lint checks fail](6365053f3cf6a28978066d928c851dd0f7558d90)
* [Changed submodule links to HTTPS so they work without a GitHub account](5d816a1fcb3f3d050b98a467ca079a9a82050c40)
* [Fixed an issue where going back from the log window would open the incorrect parent activity](52696fdf1712003e837f497ee13e95aae5b35a16)
* [Simplified the build files to allow the project to be used as a library](71767b98930f226f85424bca5528dcd3e1830d4d)
* [Converted the project to a library project](2564f05e0469edf7e28a3a11fd0e83e0e9513b85)
* [Removed example code and some assets which were unrelated to the library](3e2cc1d94182651334c28ed54ac9673a5e5d2cc8)
* [Added prebuilt native libraries](adb872390b9d2240b6ac2b5ad31abc430a402dd0)

Description
------------
With the new VPNService of Android API level 14+ (Ice Cream Sandwhich) it is possible to create a VPN service that does not root access. This project is a port of OpenVPN.

Developing
---------------
If you want to develop on ics-openvpn please read the [doc/README.txt](https://github.com/schwabe/ics-openvpn/blob/master/doc/README.txt) *before* opening issues or emailing me. 

Also please note that before contributing to the project that I would like to retain my ability to relicense the project for different third parties and therefore probably need a contributers agreement from any contributing party. To get started, [sign the Contributor License Agreement](https://www.clahub.com/agreements/schwabe/ics-openvpn).

You can help
------------
Even if you are no programmer you can help by translating the OpenVPN client into your native language. [Crowdin provides a free service for non commercial open source projects](http://crowdin.net/project/ics-openvpn/invite) (Fixing/completing existing translations is very welcome as well)

FAQ
-----
You can find the FAQ here (same as in app): http://ics-openvpn.blinkt.de/FAQ.html

Note to administrators
------------------------

You make your life and that of your users easier if you embed the certificates into the .ovpn file. You or the users can mail the .ovpn as a attachment to the phone and directly import and use it. Also downloading and importing the file works. The MIME Type should be application/x-openvpn-profile. 

Inline files are supported since OpenVPN 2.1rc1 and documented in the  [OpenVPN 2.3 man page](https://community.openvpn.net/openvpn/wiki/Openvpn23ManPage) (under INLINE FILE SUPPORT) 

(Using inline certifaces can also make your life on non Android platforms easier since you have only one file.)

For example `ca mycafile.pem` becomes
```
  <ca>
  -----BEGIN CERTIFICATE-----
  MIIHPTCCBSWgAwIBAgIBADANBgkqhkiG9w0BAQQFADB5MRAwDgYDVQQKEwdSb290
  [...]
  -----END CERTIFICATE-----
  </ca>
```
Fotnotes
-----------
Please that OpenVPN used by this project is under GPLv2. 

If you cannot or do not want to use the Play Store you can [download the apk files directly](http://plai.de/android/) . 

The F-Droid project also [builds and distributes the application](https://f-droid.org/repository/browse/?fdid=de.blinkt.openvpn). 

If you want to donate you can donate to [arne-paypal@rfc2549.org via paypal](https://www.paypal.com/cgi-bin/webscr?hosted_button_id=R2M6ZP9AF25LS&cmd=_s-xclick).


The old official or main repository was a Mercurial (hg) repository at http://code.google.com/p/ics-openvpn/source/

The new git repository is now at GitHub under https://github.com/schwabe/ics-openvpn

Please read the doc/README before asking question or starting development.
