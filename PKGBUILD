# Maintainer: Fazlul Shahriar <fshahriar@gmail.com>
# Contributor: Denis Zawada <deno@bajtogrod.pl>
#
# Repository: https://github.com/fhs/archlinux-packages
pkgname=igraph
pkgver=0.7.1
pkgrel=1
pkgdesc="A library for creating and manipulating (un)directed graphs."
arch=('i686' 'x86_64')
url="http://igraph.org/c/"
license=('GPL2')
depends=('libxml2' 'gmp')
options=('!libtool')
#source=("https://github.com/${pkgname}/${pkgname}/archive/${pkgver}.tar.gz") # bigger than below
source=("http://igraph.org/nightly/get/c/${pkgname}-${pkgver}.tar.gz")
md5sums=('4f6e7c16b45fce8ed423516a9786e4e8')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make || return 1
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
