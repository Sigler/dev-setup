My Typical Dev Environment
==========================

## Apps
* [Chrome](https://www.google.com/chrome/)
* [Github Desktop](https://desktop.github.com/)
* [Node.js](https://nodejs.org)
* [Sketch](https://www.sketchapp.com)
* [Sublime Text](https://www.sublimetext.com)
* [iTerm2](https://www.iterm2.com/)


## Install Homebrew
First things first.
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
