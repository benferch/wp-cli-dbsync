# WP-CLI DB Sync
*Wordpress remote to local database import tool for wp-cli*

## Installation
`composer require timneutkens/wp-cli-dbsync:^1.0.0`

## Configuration
This command uses (https://github.com/xwp/wp-cli-ssh)[wp-cli-ssh].

To get started use their instructions to setup a remote host:
Add an `ssh` section to your `wp-cli.yml`/`wp-cli.local.yml`, as seen in the [sample config](wp-cli.sample.yml).
You indicate the `ssh` command templates for each host you want to connect to. The template variable `%cmd%` is 
replaced with the full command to run on the server; the `%pseudotty%` template variable is replaced 
with `-t`/`-T` depending on whether you're on a TTY or piping the command output.

For a step-by-step guide, please refer to the [wiki](https://github.com/x-team/wp-cli-ssh/wiki/Configuring-the-plugin).


Now you can run the following command:
`wp dbsync <host here>`

Replace `<host here>` with the host you just setup in your `wp-cli.yml`/`wp-cli.local.yml`.
