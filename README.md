# My Boxen

This is my Boxen project for auto-configuring a development environment for
my future MacBook Pros.



## Modules

### What is Included in the Boxen Template

Modules included in the template `Puppetfile`:

* Boxen Internal
  * Full Disk Encryption requirement
  * repository
  * stdlib
  * inifile
* Utilities
  * sudo
  * dnsmasq (with .dev resolver for localhost)
  * GNU softwares
    * Findutils
    * GNU tar
* openssl
* xquartz
* foreman
* Version Control
  * Git
  * Hub
  * gitx
* pkgconfig
* gcc
* go
* Ruby
  * rbenv
  * Ruby 1.9.3
  * Ruby 2.0.0
  * Ruby 2.1.0
  * Ruby 2.1.1
  * Ruby 2.1.2
* Web
  * nginx
  * phantomjs
  * Node.js
    * Node.js 0.6
    * Node.js 0.8
    * Node.js 0.10
* Package Management
  * Homebrew
  * brewcask
  * Anaconda

More existing modules can be found under the
[boxen organization](https://github.com/boxen) as `puppet-*`.

* postgresql
* macvim
* atom
* virtualbox
* iterm2
* googledrive
* dropbox
* slack
* skype
* chrome
* flux
* intellij
* pycharm
* webstorm

### What Else Do I Need to Install

* Python package & environment (as `virtualenv`) manager
  * [Anaconda3](https://www.continuum.io/downloads#_macosx) (recommended)
* [R](www.r-project.org)
  * RStudio
* [Julia](http://julialang.org/downloads/)
* Jupyter kernels
  * [IRkernel](http://irkernel.github.io/installation/)
  * [IJulia](https://github.com/JuliaLang/IJulia.jl)
  * [Spark Kernel](https://github.com/ibm-et/spark-kernel)
* GIS
  * QGIS
  * JOSM
  * GDAL
* LaTeX (TeXShop, BibDesk, etc.)
* Available in package managers
  * homebrew `brew list`
  * npm
* Available on homebrew-cask
  * java 8 jdk
  * anaconda (It's recommended to directly install from Continuum Analytics)
* Cloud Storage
  * Box
  * Copy
* Wechat
* Chromecast
* Adobe
  * Acrobat
  * Illustrator

Update Snippets

```sh
conda info
conda update conda anaconda
conda install jupyter
conda create -n snakeskin python=2.7
```

## Getting Started

> There are a few potential conflicts to keep in mind.
> Boxen does its best not to get in the way of a dirty system,
> but you should check into the following before attempting to install your
> boxen on any machine (we do some checks before every Boxen run to try
> and detect most of these and tell you anyway):

> * Boxen __requires__ at least the Xcode Command Line Tools installed.
> * Boxen __recommends__ installing the full Xcode.
> * Boxen __will not__ work with an existing rvm install.
> * Boxen __may not__ play nice with a GitHub username that includes dash(-)
> * Boxen __may not__ play nice with an existing rbenv install.
> * Boxen __may not__ play nice with an existing chruby install.
> * Boxen __may not__ play nice with an existing homebrew install.
> * Boxen __may not__ play nice with an existing nvm install.



## Customization

### Change Module Defaults

`hiera/` is the preferred mechanism to make changes to module defaults,
e.g. version and service port.

### Creat New Puppet Modules

You can make new modules in the `modules/` directory for these softwares.
Then add `include $modulename` in `manifests/site.pp` to include
the new modules.

See [The official Puppet documentation](http://docs.puppetlabs.com/) for:

 * [Modules](http://docs.puppetlabs.com/learning/modules1.html#modules)
 * [Classes](http://docs.puppetlabs.com/learning/modules1.html#classes)
 * [Defined Types](http://docs.puppetlabs.com/learning/definedtypes.html)
 * [Facts](http://docs.puppetlabs.com/guides/custom_facts.html)

See `modules/people/README.md` for creating per-user modules.
See `modules/projects/README.md` for creating organization-wide modules.



## Halp!

See [FAQ](https://github.com/boxen/our-boxen/blob/master/docs/faq.md).

Use Issues or #boxen on irc.freenode.net.
