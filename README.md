## [Xibalba](https://github.com/cuerti/xibalba) – VPN monitor tool and Internet Kill Switch

Xibalba is a networking tool focused on those who use VPN connections most part of the day and want to be sure that their secure connection is always alive.

The application has two major ways of use:
* __"Reconnection" mode:__ If Xibalba detects that your VPN is down, it alert the user and tries to restore the VPN connection automatically. This is Xibalba's default behaviour (no extra flag needed).

* __"Internet Kill Switch" mode:__ If Xibalba detects that your VPN is down, it automatically alert the user and shut down all the network trafic by applying some iptables rules, dropping all INPUT, FORWARD and OUTPUT packages. By doing this you're really secure, and if your VPN goes down there is no way your IP get leaked when your VPN falls. You want to run Xibalba with the Kill Switch feature, you have tu use [-k, --killswitch] param.

It all started when I was looking for some app that could monitor my VPN connections and implements a KillSwitch when any of them fail. After a while I couldn't find nothing that implement this in a secure way, so this project is my take at creating one.


> **Disclaimer**:
> This is an early beta version. It may have undetected security issues, and there is definitely a load of bugs to fix, features to add and so on. 
> For bugfixes, new features or ideas/suggestions feel free to contact me at eif0@hush.com


That said, I'm using this app myself and I'd like to share its sources, so anyone can contribute to the development. Any help is always welcome!


## Technical details

The app is written in pure Python2 (migration to Python3 is planned for the future). 

For those cute GUI windows Xibalba uses PyGTK -GTK2- (migration to GTK3 is also planned for the future).


### Running locally


You can clone this repo with a simple:
``$ git clone https://github.com/cuerti/xibalba.git``


You can also download a bundle with all Xibalba's sources from [here](https://github.com/cuerti/xibalba/archive/master.zip).


### Third party libraries & deps

* [python-geoip](http://pythonhosted.org/python-geoip/)
* [zenity](https://wiki.gnome.org/Projects/Zenity)
* [wget](https://www.gnu.org/software/wget/)
* [less](http://www.greenwoodsoftware.com/less)

Many thanks to all these libraries authors and contributors.


### Special thanks

* To [Tom Viner](https://github.com/tomviner) who allowed me to use the icons he created for [net-panel](https://github.com/tomviner/net-panel). You can find these icons [here](/images).


### Licensing

The source code is licensed under GPLv3. License is available [here](/LICENSE).

## Contribute

You can help this project by reporting problems, suggestions, or contributing to the code.

Also, you can always contact me at eif0@hush.com

### Report a problem or suggestion/ideas

Go to Xibalba's [issue tracker](https://github.com/cuerti/xibalba/issues) and check if your problem/suggestion is already reported. If not, create a new issue with a descriptive title and detail your suggestion or steps to reproduce the problem.

Also, as said before, my email is always available for suggestions, ideas and cat pictures.

### Invite me a beer

Last, but not least, if you like this project and find it usefull you can buy me a beer

* BitCoin: __12toiKBQG8NukypFSd5qKvWCp1rtoPqyur__
* LiteCoin: __LXtAKuXqCKWD6AWnGqZ6iw7HduqCgsXMhR__

