# edit-slack.vim

 Open slack, like a file

![demogif](https://68.media.tumblr.com/eca8562405343fe62cce8f65179c2d27/tumblr_oihg6bGRZ21riy4fno1_1280.gif)

## Installation

### 1. download vim script

*  [vim-plug](https://github.com/junegunn/vim-plug)
  * `Plug 'yaasita/edit-slack.vim'`
*  [NeoBundle](https://github.com/Shougo/neobundle.vim)
  * `NeoBundle 'yaasita/edit-slack.vim'`
*  [Vundle](https://github.com/gmarik/vundle)
  * `Plugin 'yaasita/edit-slack.vim'`
*  [Vim packages](http://vimhelp.appspot.com/repeat.txt.html#packages) (since Vim 7.4.1528)
  * `git clone https://github.com/yaasita/edit-slack.vim ~/.vim/pack/plugins/start/edit-slack.vim`

### 2. download [edit-slack](https://github.com/yaasita/edit-slack) binary

* Linux
    * 64bit: https://github.com/yaasita/edit-slack/releases/download/v0.2.0/linux-amd64-edit-slack
    * 32bit: https://github.com/yaasita/edit-slack/releases/download/v0.2.0/linux-386-edit-slack
* FreeBSD
    * 64bit: https://github.com/yaasita/edit-slack/releases/download/v0.2.0/freebsd-amd64-edit-slack
    * 32bit: https://github.com/yaasita/edit-slack/releases/download/v0.2.0/freebsd-386-edit-slack
* Windows
    * 64bit: https://github.com/yaasita/edit-slack/releases/download/v0.2.0/windows-amd64-edit-slack.exe
    * 32bit: https://github.com/yaasita/edit-slack/releases/download/v0.2.0/windows-386-edit-slack.exe
* macOS
    * 64bit: https://github.com/yaasita/edit-slack/releases/download/v0.2.0/darwin-amd64-edit-slack
    * 32bit: https://github.com/yaasita/edit-slack/releases/download/v0.2.0/darwin-386-edit-slack


Save binary under edit-slack.vim directory.  
Rename the file name to edit-slack (windows user is edit-slack.exe)

ex. Linux User

    cd /path/to/install/directory/edit-slack.vim
    # download binary
    mv linux-amd64-edit-slack edit-slack # windows user is edit-slack.exe
    chmo +x edit-slack

## Settings

Get token from [slack API page](https://api.slack.com/web).

[<img src="https://68.media.tumblr.com/a3f5b61ee105e7932460a1303d2b496f/tumblr_oihao1lNZW1riy4fno1_250.png">](https://api.slack.com/web#authentication)

Add the token to vimrc.

    let g:yaasita_slack_token = "xoxp-xxxxxxxxxx-xxxxxxxxxx-xxxxxxxxxx-xxxxxx"

When displaying Unicode characters

    set fileencodings+=utf-8
    set encoding=utf-8

## Usage

![uri](http://i.imgur.com/aZnPw54.png)

    # open channels/private group/users list
    vim slack://ch
    vim slack://pg
    vim slack://dm
    # gf command opens a chat under the cursor

    # open general channel
    vim slack://ch/general

    # in the vim
    :e slack://ch
    :tabe slack://dm/hogeuser

    # reload
    :e

    # post
    # write it under the "=== Message ===" mark
    :w

## Mechanism

![mechanizm](https://68.media.tumblr.com/0aea501a67c0eb4ce83598c6fe4385fc/tumblr_oih8utLU2C1riy4fno1_500.png)

(c) [gopher stickers](https://github.com/tenntenn/gopher-stickers)
