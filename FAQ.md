## spgu FAQ
### Soul's Pretty Good Updater for Debian based systems

The following are a list of questions you may have about this software. Will be updated as needed. Please reference this file before opening an issue or if you have any questions. If you have any questions that are not answered, feel free to open an issue with the title "Question" and I will try to help!

#### What is this program?
This is a small script I wrote, initially for use on Arch to update all packages from different package managers seamlessly in one command. Though this version never saw the light of day, I took the concept and adapted it to Debian, when I switched distros.

#### Is it safe?
While you should **not** trust any random executable you download off the internet, you don't have to in this case. You can review the source code yourself if you wish.

As an additional measure, all commits, tags, and releases from v0.1.1 and onward will be signed with my official signing key. To check a signature, see the instructions on my profile.

#### Why did you make it?
I primarily made it for my own personal use and to learn shell scripting. I made it opensource and public, in the hopes that other curious souls out there may hopefully find some enjoyment and/or usefulness from it. As the name suggests, while this app is *pretty good* at what it does, there are almost certainly better options out there!

#### How is this better than apt or Synaptic?
Unlike those programs, this script seamlessly, and with minimal user interaction, can run apt update, apt upgrade, and apt autoremove in one simple command. The is one of the major drawbacks I find when using regular apt to run updates.

In addition to this, I have implemented a *modules* feature which can also call other package managers in the same way. Currently Flatpak is enabled in this way by default, but can be disabled/removed if you wish. You can also call other command line package managers should you wish, such as nala or snapd.

#### How is this better than graphical stores/updaters like Discover Store, mintUpdate, etc?
It's not.

#### Apt has an error and/or requires manual intervention. What do I do?
Because of the silent nature of this application, it always assumes yes using the -y argument. While this is convenient, in the rare case that you need to manually intervene when running apt, it is highly recommended that you simply use apt directly. Alternatively, you can edit the program yourself and remove '-y' from each line entry where it is found.

#### Will you add support for x feature or package manager?
Maybe. However, since I made this specifically for my needs, I will only be likely to add it if I would benefit from it. Currently I consider it mostly feature complete. You are welcome to open feature requests, however, if you want a feature that I haven't, or won't add, feel free to fork it on Github!

#### Will you support x distro?
Probably not, unless I use said distro as my daily driver and feel it would be beneficial for me. See question above.

#### Will you add built in support for snaps?
Absolutely not.

#### Can I contribute?
Absolutely! Simply create a pull request for your code and I will review it. Please be verbose with your coding and leave clear comments in the code. If I don't know what your code does, it will be rejected. You can also submit feature requests and issue reports if you don't want to contribute code yourself!

#### I have other questions.
You can open an issue on Github with the title "Question" or send me an email, which is available on my profile to signed in users.
