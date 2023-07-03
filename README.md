# kubectl
Use this script instead of original kubeclt to avoid accidental context change.

# installation
1. move or rename original `kubectl` to the 'kubectl_orig'
2. save current script in the `/usr/local/bin` directory
```
cd /usr/local/bin
sudo mv /usr/local/bin/kubectl /usr/local/bin/kubectl_orig
curl -O https://raw.githubusercontent.com/litvinovandrew/kubectl/main/kubectl
```
   

# how does it works
script shows countdown timer if you are using `kubectl` without global variable `KUBECTL_CONTEXT_FROZEN`
after comman execution you can see which context is used and you can cancel the command withing 10 secons

Warning message would not be shown if global variable `KUBECTL_CONTEXT_FROZEN` is set
Command won't be executed if your current context is different with  the one set by `KUBECTL_CONTEXT_FROZEN`


# deinstallation 
```
sudo mv /usr/local/bin/kubectl /usr/local/bin/kubectl_safe
sudo cp /usr/local/bin/kubectl_orig /usr/local/bin/kubectl
```
