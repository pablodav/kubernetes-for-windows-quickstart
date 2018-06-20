# kubernetes-for-windows-quickstart

quickstart for https://github.com/pablodav/kubernetes-for-windows to start using it faster.
It will be used to test the roles before going to start working on a merge to kubespray, so in the future it could be fully integrated with kubespray, but changes will be required to get it done so this quickstart is supported for prod envs and don't worry for future support, I'm will try to create a smooth migration for that time.

fork this repo

clone with submodules:

    git clone  https://github.com/yourusername/kubernetes-for-windows-quickstart --recursive

update submodules

    git submodule update --init
    git submodule foreach git checkout master
    git submodule foreach git pull

You can also go inside each submodule dir ex: cd `roles/3d/kubespray` and update to the version you want.
You can use above commands to update the submodules any time.

install the requirements from kubespray:

```shell
sudo pip install -r roles/3d/kubespray/requirements.txt
```

## Edit vars and inventory

Edit inventory in `inventory` and vars in `inventory/group_vars`

## Run the playbooks

https://github.com/pablodav/kubernetes-for-windows#step-3---install-kubernetes-packages-using-roleskubernetesyml-playbook

# Warning

Be careful, don't save the credentials in a public repository, do not upload the changes you made in vars to your forked repo. Also use vaults to save credentials whenever is possible.
