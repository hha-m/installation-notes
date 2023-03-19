# ROR installation on Mac
Mac → homebrew → rbenv or RVM → ruby (gem) → rails

## Homebrew installation
```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

##  rbenv installation
```
$ brew install rbenv
```

- loading rebenv in your shell
```
$ rbenv init
```

- clone rbenv into ~/.rbenv
```
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
```

- configure your shell to load rbenv

option 1: for ~/.bashrc
```
$ echo 'eval "$(~/.rbenv/bin/rbenv init - bash)"' >> ~/.bashrc
$ source ~/.bashrc
```

option 2: for ~/.zshrc
```
$ echo 'eval "$(~/.rbenv/bin/rbenv init - zsh)"' >> ~/.zshrc
$ source ~/.bashrc
```
## Ruby installation using rbenv
```
# installing specific ruby version
$ rbenv install 3.0.3
```

- list latest stable releases version of ruby
```
$ rbenv install -l
```

- list all downloaded versions to your pc
```
$ rbenv install -L
```

- check all your installed ruby versions
(Note: asterisk next to the currently active global version)
```
$ rbenv versions
```

- set a Ruby version to finish installation and start using Ruby:

option 1:  set the default Ruby version for this machine
```
$ rbenv global 3.0.3
```

option 2: set the Ruby version for specific directory
(Note: this way is preferred for project based)
```
$ cd myproject

# choose specific Ruby version
$ rbenv local 3.0.3
```

## Bundler installation
```
$ gem install bundler
```

## Rails installation

option 1: installing latest rails version
```
$ gem install rails
```

option 2: installing specific version without document (--no-document, it saves your storage)
```
$ gem install rails -v '5.2.3' -V --no-document
```

- check your installed rails version
```
$ rails -v
```

## Extra Notes
Ref:
1. https://brew.sh/
https://formulae.brew.sh/formula/rbenv
2. https://devcenter.heroku.com/articles/ruby-versions
3. https://bundler.io/guides/gemfile_ruby.html
4. https://github.com/rbenv/rbenv
