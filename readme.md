## About this fork

This fork was created to handle subscriptions to Google Alert RSS feeds.  
These uri's contain a url parameter in the link, which prevents the crawler from accessing the correct page when attempting to pull the page content during the 'Read here' event.  

No other changes have been made to this project, for any questions on the project, please refer to [nkanaev](https://github.com/nkanaev)'s original [yarr](https://github.com/nkanaev/yarr) project.

Full credit to [nkanaev](https://github.com/nkanaev) the original author.

----

# yarr

**yarr** (yet another rss reader) is a web-based feed aggregator which can be used both
as a desktop application and a personal self-hosted server.

It is written in Go with the frontend in Vue.js. The storage is backed by SQLite.

![screenshot](etc/promo.png)

## usage

The latest prebuilt binaries for Linux/MacOS/Windows are available
[here](https://github.com/nkanaev/yarr/releases/latest).

### macos

Download `yarr-*-macos64.zip`, unzip it, place `yarr.app` in `/Applications` folder.
To open the app follow the instructions provided [here][macos-open] or run the command below:

    xattr -d com.apple.quarantine /Applications/yarr.app

[macos-open]: https://support.apple.com/en-gb/guide/mac-help/mh40616/mac

### windows

Download `yarr-*-windows32.zip`, unzip it, open `yarr.exe`

### linux

The Linux version doesn't come with the desktop environment integration.
For easy access on DE it is recommended to create a desktop menu entry by
by following the steps below:

    unzip -x yarr*.zip
    sudo mv yarr /usr/local/bin/yarr
    sudo nano /usr/local/share/applications/yarr.desktop

and pasting the content:

    [Desktop Entry]
    Name=yarr
    Exec=/usr/local/bin/yarr -open
    Icon=rss
    Type=Application
    Categories=Internet;

For self-hosting, see `yarr -h` for auth, tls & server configuration flags.
For building from source code, see [build.md](build.md)

## credits

[Feather](http://feathericons.com/) for icons.
