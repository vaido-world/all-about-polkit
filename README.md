# all-about-polkit
Policykit is required by the XFCE4  

Official Repository  


 
Documentation  
https://www.freedesktop.org/software/polkit/docs/latest/polkit.8.html


## Binaries
A Source Package  

#### Debian sid 
https://packages.debian.org/sid/policykit-1

#### Ubuntu Impish 
https://packages.ubuntu.com/source/impish/policykit-1


## Installation notes
**libpolkit-gobject-1-dev** won't even let you pass through GVfs compilation first steps.  
**libpolkit-gobject-1-0** is the most important later on.  
**policykit-1** is required as it resolves polkit.its file being missing.  
```
policykit-1_0.105-18+deb9u1_amd64.deb\data.tar\.\usr\share\gettext\its\polkit.its
```

