# desfire-tools-for-android
A collection of tools for interaction with [MIFARE DESFire EV1] NFC tags using Android, mostly adapted from [libfreefare] and [nfcjlib].

Note: This repository was forked from the original source available at:

https://github.com/skjolber/desfire-tools-for-android by Thomas Skjølberg (skjolber)

I changed as less as necessary to get the app run on modern Android SDK's - this app is running on SDK 33 and 
Gradle version 7.4.2. I know that there are a lot of "deprecated" notices in the source code but that could be 
the task for further enhancements. All credits are going to Thomas Skjølberg who created this fine piece of 
app in helping us to work with Mifare DESFIRE EV1 cards (b.t.w. the app is working on DESFire EV2 and EV3 as well :-).

One note regarding the file "MifareDesfireKey1.java" located in com.github.skjolber.desfire.libfreefare. The file 
equals to "MifareDesfireKey.java" in the original repository but as there is another file named "MifareDESFireKey.java"
(see the capitol letters "DES" compared to "Des") only one file can exist in a MacOS file system (I don't know about Windows, sorry). 
I renamed the file from "MifareDesfireKey.java" to "MifareDesfireKey1.java" and changed all references in the code to the 
new file name.

Second note: I included the "libfreefare" and "model" libraries direct into my package so they are no included within 
the build.gradle (app) file.

The original app in Google PlayStore: https://play.google.com/store/apps/details?id=com.skjolberg.mifare.desfiretool&hl=no

Features:
  * [MIFARE DESFire EV1] tag model
  * Encryption support
    * AES
    * (3)DES 
    * 3K3DES
  * [Mifare Desfire Tool] demo application

As NXP now has a freely available [TapLinx] SDK for supporting these cards, so this project is mostly for educational and/or debugging purposes.

## Licenses
For following licenses apply

  * nfcjlib - [Modified BSD License (3-clause BSD)]
  * libfreefare - [LGPL 3.0 with classpath exception]
  * everything else - [Apache 2.0]

# Obtain
The project is based on [Gradle].

# Usage
See the example application.

# History
 - 1.0.0: Initial version

[Gradle]:                               https://gradle.org/
[Apache 2.0]:          		            http://www.apache.org/licenses/LICENSE-2.0.html
[issue-tracker]:       		            https://github.com/skjolber/desfire-tools-for-android/issues
[Modified BSD License (3-clause BSD)]:  nfcjlib/LICENSE
[LGPL 3.0 with classpath exception]:    libfreefare/LICENSE
[Mifare Desfire Tool]:          		https://play.google.com/store/apps/details?id=com.skjolberg.mifare.desfiretool&hl=no
[TapLinx]:                              https://www.mifare.net/en/products/tools/taplinx/
[MIFARE DESFire EV1]:                   https://en.wikipedia.org/wiki/MIFARE#MIFARE_DESFire_EV1_(previously_called_DESFire8)
[libfreefare]:                          https://github.com/nfc-tools/libfreefare
[nfcjlib]:                              https://github.com/Andrade/nfcjlib
