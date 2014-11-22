Pinboard Archiver
=================

Download a copy of every page your bookmark in Pinboard, as images.

## Prerequisites 

You'll need to install a couple of modules from CPAN:

    cpanm IO::Interactive Tie::Persistent WWW::Pinboard

Screenshots of web pages are made using [wkhtmltoimage](http://wkhtmltopdf.org/), which you'll need to install.

If you're using a headless Linux VM you might not have any nice fonts installed. Try the `urw-fonts` package from your package manager.

## Usage

Use with:

    perl fetch-bookmarks

The script keeps track of where it got to, so can be stopped and restarted any time. It will also retry failed fetches on the next run.

You can run it as a one-off, but ideally run it daily on a cron to archive any new bookmarks you add:

	0 1 * * * perl /usr/bin/fetch-bookmarks

## Todo

See the [Issues](https://github.com/willdollman/pinboard-archive/issues) page.
