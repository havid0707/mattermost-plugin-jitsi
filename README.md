# mattermost-plugin-jitsi
This plugin is forked off the [mattermost-plugin-zoom](https://github.com/mattermost/mattermost-plugin-zoom) repo that is maintained by Mattermost.
This plugin will add UI for users to start new Jitsi meetings in a Mattermost channel. Posts are created when a meeting starts.

## Installation

Go to the [releases page of this Github repository](https://github.com/seansackowitz/mattermost-plugin-jitsi/releases) and download the latest release for your server architecture. You can upload this file in the Mattermost system console to install the plugin.

## Developing

This plugin contains both a server and web app portion.

Use `make dist` to build distributions of the plugin that you can upload to a Mattermost server for testing.

Use `make check-style` to check the style for the whole plugin.

### Server

Inside the `/server` directory, you will find the Go files that make up the server-side of the plugin. Within there, build the plugin like you would any other Go application.

### Web App

Inside the `/webapp` directory, you will find the JS and React files that make up the client-side of the plugin. Within there, modify files and components as necessary. Test your syntax by running `npm run build`.

## TODO

There is still a lot of work to do to separate this from the Zoom plugin, such as:
1. Convert names from zoom to jitsi
2. Integrate with the Jitsi server for meeting status
3. Clean up a lot of unnecessary code
