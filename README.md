Run Jekyll using Vagrant
------------------------

Jekyll does not support Windows officially at the moment. While there are a few
ways to run it natively, the setup is complex and it may not be ideal if you
need to this on multiple computers.

This repository contains the Vagrant configuration and provisioning in order to
have a working Jekyll installation running on an Ubuntu based virtual machine.

Usage
-----

1. Start the vagrant instance:

   ```shell
   vagrant up
   ```
2. SSH to the vagrant box:
   ```shell
   vagrant ssh
   ```
3. Go to the shared folder that contains your Jekyll project:
   ```shell
   cd /srv/src/<your_jekyll_project_path>
   ```
4. Start Jekyll:
   ```shell
   jekyll serve --host=0.0.0.0
   ```

*Note:* Make sure to include the `--host=0.0.0.0` argument, otherwise you will not be able to connect to the Jekyll server from your host machine.

