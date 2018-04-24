# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=kickshaw
pkgver=0.6.3
pkgrel=1
pkgdesc='A menu editor for openbox'
url='https://github.com/natemaia/kickshaw'
arch=('x86_64')
sha256sums=('800bf32d78696d2ea2e59c58e4451be31f0059b8c862feb12336d565ce74b12c'
            'c10cb8cab7f32ac4288e4bcdc50b90bb35813993846c5d882c98a7b05a40be22'
            '32b1062f7da84967e7019d01ab805935caa7ab7321a7ced0e30ebe75e5df1670')
license=('GPL2')
source=("http://download.savannah.gnu.org/releases/obladi/${pkgname}_${pkgver}_GTK3_source_only.tar.bz2"
		"kickshaw.desktop"
		"COPYING")
makedepends=('gtk3' 'gcc')
depends=('gtk3')

build() {
  cd ${pkgname}_${pkgver}_GTK3_source_only/source
  make
}

package() {
  cd ${pkgname}_${pkgver}_GTK3_source_only/source
  install -Dm 0755 kickshaw "$pkgdir/usr/bin/kickshaw"
  
  # license , copying readme in license directory for provide author
  cd ${srcdir}
  install -Dm 0644 COPYING "${pkgdir}/usr/share/licenses/kickshaw/COPYING"
  install -Dm 0644 kickshaw.desktop "$pkgdir/usr/share/applications/kickshaw.desktop"

}
