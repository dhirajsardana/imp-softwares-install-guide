
1)Install VM Driver: Before setting up minishift, VM driver is required.
  xhyve driver will be deprecated soon , so we're installing hyperkit, below are steps to install & setup the same:

   $ brew install docker-machine-driver-hyperkit

   $ sudo chown root:wheel /usr/local/bin/docker-machine-driver-hyperkit

   $ sudo chmod u+s,+x /usr/local/bin/docker-machine-driver-hyperkit

2) Install minishift

  $ brew cask install minishift

3) Start minishift(which will install local openshift cluster).By default it uses xhyve driver, so need to mention vm-driver :

   $ minishift start --vm-driver hyperkit

	After suceessful run(which will take few minutes), output will be like:
	OpenShift server started.

	The server is accessible via web console at:
    		https://<IP>:8443/console


  Now, You can try out openshift commands/deployments via UI or from commands.

References: 
 https://docs.okd.io/latest/minishift/getting-started/setting-up-virtualization-environment.html#setting-up-hyperkit-driver
 https://docs.okd.io/latest/minishift/getting-started/installing.html#installing-with-homebrew
 https://docs.okd.io/latest/minishift/getting-started/quickstart.html

