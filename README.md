## Magisk Hosts
A Magisk module that blocks a select set of distracting platforms via a custom hosts file (YouTube, Twitter, Facebook, Reddit, etc).

## Why?
In my quest for reducing distractions, I tend to block myself from certain things. On Android, I usually did that using the Stay Focused app, but as a dev I think it's nicer to just maintain a custom hosts file.

On my laptop, I use `hblock`, which works great. The hosts file featured in this module is largely a copy from my `/etc/hblock/deny.list`.

## What this is not
This is not a module to block adware/spam/etc. There are plenty modules that do that.

This module also doesn't feature a complete list of domains, just a select few that I find distracting. If you want to add some, feel free to open a PR, probably things that you find distracting are also distracting for me. But note that it's explicitly not the goal to have multiple MBs of domains and be exhaustive.

## Requirements
An Android phone which runs Magisk. Enable "systemless hosts" in the Magisk settings. It should be compatible with pretty much any Android version.

## Installation
Download the zip from here: https://github.com/SimonBaars/magisk-hosts/releases/tag/v1.2

Flash the zip using Magisk. Reboot when Magisks prompts you to. After reboot, use your browser to go to Youtube.com to test that it works.
