[![Build Status](https://travis-ci.org/elleryq/galaxy-role-android-ndk.svg?branch=master)](https://travis-ci.org/elleryq/galaxy-role-android-ndk)

# Ansible Role: Android NDK

An Ansible Role that installs the Android NDK tools and dependencies on Ubuntu.

And this role is modified from nickp666.android-sdk.

## Requirements

A recent version of Ubuntu.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    android_ndk_version: "10d"

The location to the Android NDK tools package to be installed.

    android_ndk_install_location: /opt

The location on disk where you'd like to NDK to be installed.

    android_ndk_dependency_packages:
  		- "libncurses5"
		- "libstdc++6"
		- "zlib1g"
		- "imagemagick"
		- "expect"
		- "gradle"
		- "ant"
		- "ccache"
		- "autoconf"
		- "automake"
		- "ccache"
		- "python-dev"
		- "zlibc"

A list of aptitude installable build dependency packages.


## Example Playbook

    - hosts: appbuild
      vars_files:
        - vars/main.yml
      roles:
        - { role: elleryq.android-ndk }

## Contributing

 * E. Dunham - edunham (at) mozilla.com

## License

BSD

## Author Information

This role was created in 2015 by [elleryq](https://github.com/elleryq).

