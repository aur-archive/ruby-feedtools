# Contributor: Simon Lipp <sloonz+aur@gmail.com
# Maintainer: Alexsandr Pavlov <kidoz at mail dot ru>
pkgname=ruby-feedtools
_gemname=${pkgname#ruby-}
pkgver=0.2.29
pkgrel=2
pkgdesc="Implements a simple system for handling xml news feeds with caching."
arch=('any')
url="http://sporkmonger.com/projects/feedtools"
license=('MIT')
depends=('ruby' 'rubygems' 'ruby-builder' 'ruby-activerecord' 'ruby-uuidtools')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('38d545466ee4246b5479ecd0122fa879')

build() {
  cd "${srcdir}"
  export HOME=/tmp
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" ${_gemname}-${pkgver}.gem
}
