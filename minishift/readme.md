For Mac:
1)Setup xhyve driver:


brew install docker-machine-driver-xhyve
sudo chown root:wheel $(brew --prefix)/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve
sudo chmod u+s $(brew --prefix)/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve

2) Install minishift


brew cask install minishift

3) Start minishift(which will install local openshift cluster) :
minishift start

References: 
https://docs.okd.io/latest/minishift/getting-started/installing.html#installing-with-homebrew
https://docs.okd.io/latest/minishift/getting-started/setting-up-virtualization-environment.html#for-macos
https://docs.okd.io/latest/minishift/getting-started/quickstart.html

