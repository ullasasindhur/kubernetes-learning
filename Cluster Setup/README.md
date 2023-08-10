# Instructions to Setup Kubernetes Cluster via Vagrant and Virtual Box:
1. Install Vagrant by following [link](https://developer.hashicorp.com/vagrant/downloads)
2. Install Virtual Box by following [link](https://www.virtualbox.org/manual/ch02.html)
3. Run the following command from `Cluster Setup` folder
    > vagrant up

## Note:
1. For making any changes, please edit settings.yaml file.

## TO-DO:
- If you get any network related errors, please run the following commands:
    ```shell
    sudo mkdir -p /etc/vbox/
    echo "* 0.0.0.0/0 ::/0" | sudo tee -a /etc/vbox/networks.conf
    ```

### Reference:
> Initial scripts are taken from [techiescamp](https://github.com/techiescamp/vagrant-kubeadm-kubernetes/tree/main) GitHub.

#### Changes Made to initial Scripts:
- Option to configure crio version in settings.yaml file.
- Removed option to configure kubernetes as we need latest version.
- Modified apt packages.
- Updated CRIO and kubernetes setup to latest instructions as per August,2023.
- Removed Dashboard from installation, if you follow this [link](https://github.com/kubernetes/dashboard#manifest).
