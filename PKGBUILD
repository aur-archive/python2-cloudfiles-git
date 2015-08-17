# Maintainer: Daniel Wallace <danielwallace at gtmanfred dot com>
pkgname=python2-cloudfiles-git
pkgver=1.7.11.11.g8855764
pkgver(){
  cd $srcdir/$pkgname
  git describe --tags --long |sed 's/-/./g'
}
pkgrel=1
pkgdesc="Python language bindings for Cloud Files API"
arch=('i686' 'x86_64')
url="http://www.rackspacecloud.com/"
license=('GPL')
depends=('python2')
makedepends=('git' 'python2-distribute')
provides=('python2-cloudfiles')
source=("$pkgname::git://github.com/rackerlabs/python-cloudfiles.git")
md5sums=('SKIP')

build() {
  cd "$srcdir/$pkgname"
  python2 setup.py build
}

package() {
  cd "$srcdir/$pkgname"
  python2 setup.py install --root=$pkgdir
}

# vim:set ts=2 sw=2 et:
