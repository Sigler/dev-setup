My Typical Dev Environment
==========================

## Apps
* [Chrome](https://www.google.com/chrome/)
* [Dropbox](https://www.dropbox.com)
* [1Password](https://1password.com)
* [Github Desktop](https://desktop.github.com/)
* [Node.js](https://nodejs.org)
* [Sketch](https://www.sketchapp.com)
* [Sublime Text](https://www.sublimetext.com)
* [iTerm2](https://www.iterm2.com/)
* [Cyberduck](https://cyberduck.io/)

## X-Code Command Line Tools
First things first. Don't need X-Code, just the CLTs.
```
xcode-select --install
```

## Install Homebrew
[https://brew.sh/](https://brew.sh/)
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Configure Git

```
git config --global color.ui true
git config --global user.name "YOUR NAME"
git config --global user.email "YOUR@EMAIL.com"
ssh-keygen -t rsa -C "YOUR@EMAIL.com"
```
Paste the following in [Github](https://github.com/settings/ssh).
```
cat ~/.ssh/id_rsa.pub
```
Test it
```
ssh -T git@github.com
```

## Ruby on Rails
Source: [https://gorails.com/setup/osx/10.12-sierra](https://gorails.com/setup/osx/10.12-sierra)

### Ruby
Installing Ruby 2.4.
```
brew install rbenv ruby-build

# Add rbenv to bash so that it loads every time you open a terminal
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
source ~/.bash_profile

# Install Ruby
rbenv install 2.4.0
rbenv global 2.4.0
ruby -v
```

### Rails
```gem install rails -v 5.0.1```

Tell *rbenv* about it.

```rbenv rehash```

Verify it

```rails -v```

## Sublime Text Setup

### Package Manager

[Package Control](https://packagecontrol.io/installation)

Hit Ctl+` to open console.

```
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

#### Packages to install
* Jade
* Ruby Slim
* Haml
* Sass
* SCSS
* Emmet
* Material Theme
* AdvancedNewFile
* A File Icon
* Sublime Jekyll

### User Preferences

```
{
  "always_show_minimap_viewport": true,
  "bold_folder_labels": true,
  "caret_extra_width": 1,
  "caret_style": "phase",
  "color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme",
  "draw_minimap_border": true,
  "ensure_newline_at_eof_on_save": true,
  "font_face": "Source Code Pro",
  "font_options":
  [
    "no_round"
  ],
  "font_size": 15,
  "highlight_line": true,
  "ignored_packages":
  [
    "Vintage"
  ],
  "indent_guide_options":
  [
    "draw_normal",
    "draw_active"
  ],
  "line_padding_bottom": 3,
  "line_padding_top": 3,
  "overlay_scroll_bars": "enabled",
  "tab_size": 2,
  "theme": "Material-Theme.sublime-theme",
  "translate_tabs_to_spaces": true,
  "trim_trailing_white_space_on_save": true
}
```

### Coding Fonts
[Source Code Pro](https://github.com/adobe-fonts/source-code-pro)
