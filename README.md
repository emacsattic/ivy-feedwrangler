# ivy-feedwrangler

[![MELPA](https://melpa.org/packages/ivy-feedwrangler-badge.svg)](https://melpa.org/#/ivy-feedwrangler)
[![MELPA Stable](https://stable.melpa.org/packages/ivy-feedwrangler-badge.svg)](https://stable.melpa.org/#/ivy-feedwrangler)

An [Ivy](http://oremacs.com/swiper/) interface to the [Feedwrangler RSS](https://feedwrangler.net) service

![](https://asimpson.github.io/ivy-feedwrangler/images/unread-items.png)

## Setup
This package requires that you manually retrieve your access token by using the `curl` command on this page: https://feedwrangler.net/developers/users

Once you have an access token add your credentials to your `authinfo` file with the following fields:

| Field | Value |
|---|---|
| `machine` | feedwrangler.net |
| `login` | account email address |
| `password` | token |


It should look something like this:
`machine feedwrangler.net login EMAIL password TOKEN`

## Usage
The package exposes the `ivy-feedwrangler` function, `M-x ivy-feedwrangler`.

Pressing enter on a post opens the default browser. There are a couple additional key commands:

![](https://asimpson.github.io/ivy-feedwrangler/images/options-screen.png)

| Key | Command |
|---|---|
| `x` | Mark selected post as read |
| `X` | Mark all posts as read |
| `r` | Save as unread in pinboard |
| `p` | View [post body in a buffer](https://asimpson.github.io/ivy-feedwrangler/images/post-view.png) |

Note: that these commands should work in the default ivy interface as well as in a `ivy-occur` buffer.

### Add item to pinboard.in
To be able to save the selected item to [pinboard.in](https://pinboard.in) add another entry to `authinfo` for pinboard like so:

| Field | Value |
|---|---|
| `machine` | pinboard.in |
| `login` | pinboard username |
| `password` | pinboard API token from [here](https://pinboard.in/settings/password). |

This entry will look like:

`machine pinboard.in login username password username:API_TOKEN`.
