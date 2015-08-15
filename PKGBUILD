# Maintainer: Manalishi <manalishi at freenet dot de>
pkgname=ft232r_prog
pkgver=1.24
pkgrel=2
pkgdesc="A command-line interface for reconfiguring the FT232R chip."
arch=('i686' 'x86_64')
url="http://www.rtr.ca/ft232r/"
license=('GPL')
provides=('ft232r_prog')
depends=('libusb-compat' 'libftdi-compat')
source=("http://www.rtr.ca/ft232r/ft232r_prog-${pkgver}.tar.gz")
md5sums=('5f5c841151c02cd04f88502f02ce9094')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make || return 1
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  install -Dm 755 ft232r_prog ${pkgdir}/usr/bin/ft232r_prog
  install -Dm 644 LICENSE.txt ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE || return 1
}
