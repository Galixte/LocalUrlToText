[![Build Status](https://travis-ci.org/Mar-tin-G/LocalUrlToText.svg?branch=master)](https://travis-ci.org/Mar-tin-G/LocalUrlToText)

# LocalUrlToText

[phpBB 3.1](https://www.phpbb.com/) Extension Local URL To Text

## Beta

This extension is still in beta status. Please do not use this extension on production boards without testing.

## Description

Replaces local URLs (links to forums, topics, posts or member profiles within your board) with a customizable text.

Examples:
* If a user of your board posts a link to a forum, it appears as a link like _http://yourboard/viewforum.php?f=5_.
* With this extension, the link to the forum is rather displayed as _Forum Name_.
* Links to topics can be displayed as _Topic Title_ instead of _http://yourboard/viewtopic.php?f=5&t=2_.
* You can also include the name of the forum containing that topic to the link, e.g. _Topic Title (Forum Name)_.
* Similar text replacements are available for links to posts and to member profile pages.
* Local links within Custom profile fields can be replaced as well.
* Supports [Pages extension](https://www.phpbb.com/customise/db/extension/pages/)
* Works with [External Links extension](https://www.phpbb.com/community/viewtopic.php?f=456&t=2270671)

The extension only replaces these links when displaying a message (post, private message, etc.). It does not alter the messages that are stored into the database.
So when a topic gets renamed, all links to this topic will display the new topic title automatically.

## Text replacements

The following replacements are available:
* For forum or category links: forum/category name
* For topic links: topic title, forum name of containing forum
* For post links: poster user name, poster user colour, post subject, topic title, forum name, topic title (only if post subject is empty)
* For member profile links: user name, user colour
* For links to pages of the [Pages extension](https://www.phpbb.com/customise/db/extension/pages/): page title
* Option to enable or disable (default) replacement of local links within Custom profile fields

## Authorization

Users will only see content from forums they are authorized to read. E.g. if someone posts a link to a topic that resides in a protected forum, only members with access to this forum will see the title of this topic. Unauthorized members will see the default _viewtopic.php?t=xx_ link.

## Changelog

### v1.0.0-beta3

Initial release.

### v1.1.0-beta1

* Support post links with `#pXXX` parameter
* Support for links to pages of Pages extension
* Support for Custom profile fields
* Better link matching to support External Links extension (and other extensions that modify phpBBs generated links)

## Installation Instructions

* Download ZIP file from master branch
* Extract the ZIP file locally
* Create the following folders in you phpBB root path (if they do not exist already): `ext/martin/localurltotext/`
* Upload all files from the extracted ZIP file to this folder `ext/martin/localurltotext/` (overwrite any existing files)
* Log into your forum and enter the *Administration Control Panel*
* Go to *Customise* > *Extension Management* > *Manage Extensions*
* Find *Local URL To Text* in the list on the right side and click on *Enable*
* Go to *Extensions* > *Local URL To Text* > *Settings* to set up the extension

## Feedback

Please feel free to post any feedback to the [Local URL To Text topic](https://www.phpbb.com/community/viewtopic.php?f=501&t=2284236) in phpBB's extension community forum.

## License

[GPLv2](license.txt)
