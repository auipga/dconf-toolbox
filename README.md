# dconf-toolbox
Import, export, diff, merge and sync multiple dconf databases

**Contibutors wanted.**

Reading [this post](https://plus.google.com/u/0/+AdonisK/posts/EXsi58iptkW), an idea was born:
Sync some part of the dconf database over multiple installations (e.g. office PC and private laptop).

##### Here I'll just write down my thoughts:

###### v0.1
* Get all changed dconf entries from an master installation.
* Send those changes to a slave installation.
* If the changes are not sent immediately, just collect them (and discard overwritten changes).
* Import received changes on the slave installation.

###### v0.2
* Switch from master/slave to a central database/server and unlimited clients:
* Use a seperate database which is accessable from any installation (online) for collecting all changes from any installation.
* Pull changes in this database to your clients and apply them.

###### v0.3
* Option to whitelist/blacklist paths/keys for sending and receiving.
* Log of outgoing changes and transmit only selected.
* Log of incoming changes and apply only selected (which should blacklist the selected)
* Better handling of array values. (e.g. enabled shell extensions)
