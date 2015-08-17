# Maintainer: archtux <antonio dot arias99999 at gmail dot com>

pkgname=tickvue
pkgver=0.13.05
pkgrel=3
pkgdesc="Nearly real-time stock and portfolio tracker. Queries data from Yahoo Finance."
arch=('i686' 'x86_64')
url="http://tickvue.sourceforge.net/"
license=('GPL2')
depends=('qt4')
source=(http://downloads.sourceforge.net/$pkgname/TickVue%20-%20$pkgver.zip
        $pkgname.desktop)
md5sums=('78c39a55ba0a21e2bf1bd20307e0d49f'
         '148f161acc9f103ec5002a20062253e1')

prepare() {
  cd $srcdir/TickVue*
  qmake-qt4
}

build() {
  cd $srcdir/TickVue*
  make
}

package() {
  cd $srcdir/TickVue*

  # Binary
  install -Dm755 tickvue $pkgdir/usr/bin/tickvue

  # Desktop icon
  install -Dm644 tickvue.png $pkgdir/usr/share/pixmaps/tickvue.png
  install -Dm644 ../tickvue.desktop $pkgdir/usr/share/applications/tickvue.desktop
}