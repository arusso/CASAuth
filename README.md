CASAuth(entication) Extension for Mediawiki
===========================================

A CAS Authentication extension for Mediawiki 1.16

Introduction
------------

The CASAuth extension facilitates CAS authentication for your Mediawiki installation.  This particular cade dervies from work found at http://www.mediawiki.org/wiki/Extension:CASAuthentication

This code is customized towards usage for private wikis, with the ability to restrict access to the wiki to specific usernames.

This extension is currently written for, and tested against Mediawiki 1.16.  However, if you find it works well against a different version of Mediawiki, please feel free to let me know and I will keep track of it in this README.

The extension will follow whatever version of Mediawiki is found in the [http://fedoraproject.org/wiki/EPEL EPEL] repository.

Installation
------------

Assuming a working CAS system, installation should take under 15 minutes.  Assume $WIKI is the directory for your wiki.

1 Create folder $WIKI/extensions/CASAuth/
2 Download this source code into that directory
3 Download the [https://wiki.jasig.org/display/CASC/phpCAS phpCAS] extension and extract it to the folder $WIKI/extensions/CASAuth/CAS/
4 Add the following lines to your LocalSettings.php
<pre>
require_once( "$IP/extensions/CASAuth/CASAuth.php" );
casSetup();
</pre>
5 In the $WIKI/extensions/CASAuth/ directory, copy the CASAuthSettings.php.template file to CASAuthSettings.php and modify it for your environment.
6 You should now have working CAS authentication for your wiki!

Credits
-------

Source code found here is derived from the extension found at http://www.mediawiki.org/wiki/Extension:CASAuthentication, originally written by Ioannis Yessios.