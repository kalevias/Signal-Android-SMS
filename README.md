# Signal Android SMS 

Signal is a simple, powerful, and secure messenger.

Signal uses your phone's data connection (WiFi/3G/4G/5G) to communicate securely. Millions of people use Signal every day for free and instantaneous communication anywhere in the world. Send and receive high-fidelity messages, participate in HD voice/video calls, and explore a growing set of new features that help you stay connected. Signal’s advanced privacy-preserving technology is always enabled, so you can focus on sharing the moments that matter with the people who matter to you.

Signal Android SMS is a fork of Signal which puts SMS messaging capabilities back into the hands of the users who want it, and gets rid of several other pesky "features" that have made their way into Signal.

If you find bugs with this fork of Signal, you are welcome to try to resolve them. I'm working on this project because Signal annoyed me enough to do something about it. Please submit any bug reports to the official Signal repository.

No, this fork will probably never be in an app store. However, you can clone the repository and build an APK for yourself if you like it enough.

## Migrating from Official Signal

Alright, if you're trying to migrate from the official Signal Android app to this one, let me give you some warnings. I've tried this myself, and if you do it wrong, you risk losing all of your message history. Even if you follow my instructions, it still might not work because I'm not going to extensively test this.

Problem: You can't install an unsigned APK over a signed one. This means you can't just download the APK from GitHub and install it, because Android will prevent you from doing this due to reasonable security concerns. There are some ways around this, but I haven't tried this personally, so you're on your own here.

Here's what I did to migrate to this fork of Signal:
1. Build an unsigned APK of this repository.
2. Create a backup file for all of your chat messages. Remember where this is located on your phone.
3. Have your Signal PIN and chat backup passphrase on hand.

WARNING: I recommend you try this on a new device first, rather than proceeding to step 4. If you proceed and lose everything, it's on you.
4. Uninstall Signal from your device. (This is the part where you can lose everything)
5. Download the APK you built earlier to your phone.
6. Install said APK.
7. When starting the app for the first time, choose "Transfer or restore account" > "Restore from backup". Follow the steps shown in app, and when you get the opportunity to choose the backup file to restore from, select the one you created earlier.

If everything worked correctly, you should see your Signal app just like it was before, with all of your messages. BUT WAIT! You may be experiencing a strange problem: the app crashes whenever you open one of your text message threads!

I was experiencing this issue myself, and frankly, I didn't have any good solution to it. It seems like it is due to database corruption during the backup or restore process (I'm not sure which), and I tried several different things to correct the corruption, but none of them worked.

Then, one day, I received a text message from one of my contacts who also has Signal, and somehow, the app started working as if it was never crashing in the first place. How did this fix the problem? I can't be sure, honestly. Maybe it refreshed the database somehow, I don't know.

In any case, this problem: the "Signal crashes every time I try to open a message thread" problem - is the reason why this whole process may break Signal for you, not to mention the possibility of other bugs in the process.

So, the final step of this process may be the following, but don't put your money on it:

8. Get one of your contacts that uses Signal to send you a message.

# Boilerplate from Signal Android

## Contributing Bug reports
We use GitHub for bug tracking. Please search the existing issues for your bug and create a new one if the issue is not yet tracked!

https://github.com/signalapp/Signal-Android/issues

If you are specifically looking to contribute to Signal Android SMS, your contributions are welcome!

## Joining the Beta
Want to live life on the bleeding edge and help out with testing?

You can subscribe to Signal Android Beta releases here:
https://play.google.com/apps/testing/org.thoughtcrime.securesms

If you're interested in a life of peace and tranquility, stick with the standard releases.

## Contributing Code

If you're new to the Signal codebase, we recommend going through our issues and picking out a simple bug to fix (check the "easy" label in our issues) in order to get yourself familiar. Also please have a look at the [CONTRIBUTING.md](https://github.com/signalapp/Signal-Android/blob/main/CONTRIBUTING.md), that might answer some of your questions.

For larger changes and feature ideas, we ask that you propose it on the [unofficial Community Forum](https://community.signalusers.org) for a high-level discussion with the wider community before implementation.

## Contributing Ideas
Have something you want to say about Signal projects or want to be part of the conversation? Get involved in the [community forum](https://community.signalusers.org).

Help
====
## Support
For troubleshooting and questions, please visit our support center!

https://support.signal.org/

## Documentation
Looking for documentation? Check out the wiki!

https://github.com/signalapp/Signal-Android/wiki

# Legal things
## Cryptography Notice

This distribution includes cryptographic software. The country in which you currently reside may have restrictions on the import, possession, use, and/or re-export to another country, of encryption software.
BEFORE using any encryption software, please check your country's laws, regulations and policies concerning the import, possession, or use, and re-export of encryption software, to see if this is permitted.
See <http://www.wassenaar.org/> for more information.

The U.S. Government Department of Commerce, Bureau of Industry and Security (BIS), has classified this software as Export Commodity Control Number (ECCN) 5D002.C.1, which includes information security software using or performing cryptographic functions with asymmetric algorithms.
The form and manner of this distribution makes it eligible for export under the License Exception ENC Technology Software Unrestricted (TSU) exception (see the BIS Export Administration Regulations, Section 740.13) for both object code and source code.

## License

Copyright 2013-2022 Signal

Licensed under the GPLv3: http://www.gnu.org/licenses/gpl-3.0.html

Google Play and the Google Play logo are trademarks of Google LLC.
