# Ansible OctoPrint Role
This is a role to setup OctoPrint on a Debian based system. Currently it is tested on Raspbian based systems.
Besides octoprint this role can also take of installing necessary tools to compile firmware for Arduino based controller boards and flash them via USB.

## Requirements
* A Debian based system (Raspbian is tested)
* Ansible 1.7

## Role variables
This role can be configured in many ways. Basically all options in the octoprint config can be set via variables

Name | Default | Description
-----|---------|------------
octoprint_version | 1.1.2 | What octoprint version to checkout. This should be a branch or tag name.
octoprint_user | octoprint | The system user under which octoprint runs.
octoprint_group | octoprint | The system group used for octoprint.
octoprint_installDir | /opt/octoprint | Where to checkout the octoprint sources.
octoprint_repo | https://github.com/foosel/OctoPrint.git | What upstream repo to use. Useful for using forks.
octoprint_udev_symlink | reprap | This role can create a symlink for your serial port so you always find your printer. This is the name for the symlink.
octoprint_config_api | list | This is a list of named properties configuring the api section of the octoprint config. 
octoprint_config_server_host | 0.0.0.0 | Octoprint should bind to these IP addresses