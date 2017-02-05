# This repo is a vagrant playground

After cloning the repo, run (from the root of this repo):
  `vagrant up`

  ** Note: You may see an error message about your UID; this can be fixed by updating the following file:

  `.vagrant\machines\default\virtualbox\creator_uid`

   with the correct user ID ( as output by the vagrant error ).  Run `vagrant destroy` and `vagrant up`.

After that finishes, you can connect to your machine with the following ip, user, and key from the root of this repo

  `ssh vagrant@192.168.33.10 -i .vagrant/machines/default/virtualbox/private_key`

Some example inspec profiles are included in this repo (copied from inspec/examples).

In order to run one of the profiles, run the following command from the root of this repo:

  `inspec exec ./profile-examples/profile -i .vagrant/machines/default/virtualbox/private_key -t ssh://vagrant@192.168.33.10`

To connect to your vm via the inspec shell:

  `inspec shell -i .vagrant/machines/default/virtualbox/private_key -t ssh://vagrant@192.168.33.10`