# Rofi web search

## General description

This is a fork of [pdonadeo's](https://github.com/pdonadeo)
[rofi-web-search](https://github.com/pdonadeo/rofi-web-search)
with added browser and search engine support.

The script allows [Rofi](https://github.com/davatorium/rofi) to be used as a search engine
when launched with a specific launch script.

The script provides you the ability to ask suggestions to the search engine
before actually open the browser. Just close your search string with bang (`!`)
and type `ENTER`. This ability is not available in all search engines.

Suggestions will be listed by Rofi and you can select one of them or refine your
search using `CTRL+ENTER` (this is the standard Rofi binding) to copy the
selected line into the input field, then add a `!` and press `ENTER` again.

When you are using DuckDuckGo you can also use the
[bangs search](https://duckduckgo.com/bang), starting the search with a `!` and
optionally closing it with a `!` to get suggestions, as usual.

## Requirements

* Rofi
* Python 3.*

## Configuration

The script can be configured editing the first couple of lines. You can choose
the browser, search engine, and terminal (if using Lynx browser).

Supported browsers are Google Chrome, Firefox, Brave, Chromium, and Lynx.

Supported search engines are Google and DuckDuckGo.

If using Lynx, the supported browsers are `st` and `gnome-terminal`

Just open the script and edit the necessary variables:

`SEARCH_ENGINE`

* google
* duckduckgo
* brave-search

`BROWSER`

* chrome
* firefox
* chromium
* brave-beta
* lynx

`TERMINAL`

* st
* gnome-terminal

## Launch 
Launch with (replace SCRIPT-LOCATION with the path to the script):

```bash
rofi -lines 10 -padding 0 -show search -modi search:SCRIPT-LOCATION -i -p "Search: "
```
