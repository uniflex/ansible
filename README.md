UniFlex Ansible support
=======================

Provides custom Ansible configuration that install UniFlex on remote nodes.

## Usage

- Install Ansible

        pip install ansible

- Define nodes in hosts file.

- Check the connection to ALL nodes (will fail if device is not provisioned)

        ansible nodes -m ping

- Run example playbook that gets and displays kernel and ubuntu versions
    
        ansible-playbook example.yml

    This command will run on all nodes.

- To disable cowsay run:

        export ANSIBLE_NOCOWS=1

- Install the UniFlex framework using an Ansible playbook (Check if all nodes are connected to Internet!)

        ansible-playbook install_uniflex.yml -t install

    This command will run on all nodes defined in the hosts file.

- Delete UniFlex directory on remote nodes

		ansible-playbook install_uniflex.yml -t delete

- Access the nodes

        ssh -F ssh.cfg nuc3

Note that all Ansible commands must be executed from this directory as it is source for the configuration file (`ansible.cfg`). For details refer to Ansible documentation.
