# Maintainer: Jan Boelsche <jan@lagomorph.de>
pkgname=phidget22networkserver
pkgver=1.0.0.20180406
pkgrel=1
pkgdesc="network server for Phidget devices"
url="https://www.phidgets.com/docs/Phidget_Network_Server"
provides=('phidgetnetworkserver')
arch=('x86_64')
license=('GPL')
depends=('libphidget' 'libphidgetextra')
source=(
  "phidgetnetworkserver.service"
  "https://www.phidgets.com/downloads/phidget22/servers/linux/$pkgname/$pkgname-$pkgver.tar.gz"
)
sha256sums=(
  'SKIP'
  '907330401a5b7e61ea4e57edcb00fce69fe7682b7c324ad5251c7cf6aeefb6ef'
)

build() {
  cd $pkgname-$pkgver
  ./configure --prefix=/usr
  make
}

package() {
   cd $pkgname-$pkgver
   make DESTDIR="$pkgdir/" install
   cp -r files/etc $pkgdir/etc
   install -D -m644 "${srcdir}/phidgetnetworkserver.service" "${pkgdir}/usr/lib/systemd/system/phidgetnetworkserver.service"
}
