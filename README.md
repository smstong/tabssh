# tabssh

A command line tool to open a new SSH session in a separated TMUX window.
It will set the tmux window's title properly based on the ssh server name.

## How to install tabssh?

* make sure you have tmux installed.
* copy "tabssh" to a folder which is included in $PATH.
* run below to enable bash completion.
```
	source <(tabssh completion)
```
* Enjoy the bash completion of your ssh target server name.
```
	tabssh <Tab><Tab>
```

## More configurations
tabssh reads two files to find server names for bash completion.

* ~/.tabssh
e.g.
```
user01@server1.xxx.com
another.yyy.cn
192.168.2.2
```
* ~/.ssh/known_hosts

Both files are read only once when bash completion is enabled.
So after any of the config files changed, please re-source again by
```
	source <(tabssh completion)
```
