# Omnibus Tiered Upgrade

This directory contains the Terraform code used to instantiate a "back-end" Chef Infra Server followed by a "front-end" Chef Infra Server utilizing an Omnibus built artifact downloaded from `$install_version_url`.

Both servers receive a `/etc/opscode/chef-server.rb` configuration file that is setup with the "tier" topology.

Once both servers are installed and configured the servers are then upgraded using the artifact downloaded from `$upgrade_version_url` before the pedant tests are run against the front-end.
