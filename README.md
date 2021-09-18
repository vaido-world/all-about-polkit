# all-about-polkit
Policykit is required by the GVfs, GVfs is required by XFCE4 to show trash bin icons and the like functionality.

General information  
https://en.wikipedia.org/wiki/Polkit

Official Repository  
https://gitlab.freedesktop.org/polkit/polkit/
 
Documentation  
https://www.freedesktop.org/software/polkit/docs/latest/polkit.8.html


## Binaries
A Source Package, latest version as of now.

#### Debian sid 
https://packages.debian.org/sid/policykit-1

#### Ubuntu Impish 
https://packages.ubuntu.com/source/impish/policykit-1


## Installation notes
**libpolkit-gobject-1-dev** won't even let you pass through GVfs compilation first steps.  
**libpolkit-gobject-1-0** is the most important later on.  
**policykit-1** is required as it resolves polkit.its file being missing.  

### ...

### GVfs errors and their resolvance in regards of Polkit Policy kit
```
  Dependencies
                bluray: True
                  fuse: True
                   gcr: True
                gcrypt: True
                 gudev: True
               keyring: True
                logind: True
                libusb: True

           devel_utils: False
       installed_tests: False
                   man: False

Found ninja-1.9.0.git.kitware.dyndep-1.jobserver-1 at /usr/bin/ninja
[101/255] Generating org.gtk.vfs.file...y_daemon_merge with a custom command.
FAILED: daemon/org.gtk.vfs.file-operations.policy 
/System/Aliens/PIP/3.8/bin/meson --internal msgfmthelper daemon/org.gtk.vfs.file-operations.policy.in daemon/org.gtk.vfs.file-operations.policy xml /Data/Compile/Sources/gvfs-master/po
msgfmt: cannot locate ITS rules for daemon/org.gtk.vfs.file-operations.policy.in
[110/255] Compiling C object 'daemon/...altest@exe/gvfsbackendlocaltest.c.o'.
ninja: build stopped: subcommand failed.
Compile: GVFS 1.48.1 - Build failed.
```

Simply installation of policykit-1 package should resolve this; as it contains files with **.its** extension.  
```
policykit-1_0.105-18+deb9u1_amd64.deb\data.tar\.\usr\share\gettext\its\polkit.its
```
#### Installation in GoboLinux 17
`InstallPackage --symlink "yes" "http://ftp.us.debian.org/debian/pool/main/p/policykit-1/policykit-1_0.105-31_amd64.deb"`

