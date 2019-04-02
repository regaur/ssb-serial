# Maintainer: Jan Boelsche <jan@lagomorph.de>
pkgname=ssb-serial
pkgver=1.2.1
pkgrel=1
pkgdesc="Scuttlebot plugin that allows access to serial port"
arch=('any')
url=""
license=('MIT')
groups=()
depends=('nodejs')
makedepends=('npm')
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
source=()

pkgver () {
  npm view ${pkgname}@latest version
}

package () {
  source "$HOME/.nvm/nvm.sh"
  nvm use 10.8.0
  local _npmdir="${pkgdir}/usr/lib/node_modules/"
  mkdir -p $_npmdir
  npm install -g --prefix "${pkgdir}/usr" ${pkgname}@${pkgver}
}
