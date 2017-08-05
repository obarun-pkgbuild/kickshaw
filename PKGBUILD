# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=kickshaw
pkgver=0.5
pkgrel=2
pkgdesc='A menu editor for openbox'
url='http://download.savannah.gnu.org/releases/obladi/'
arch=( 'x86_64' )
md5sums=('SKIP')
license=( 'GPL2' )


source=("$url/kickshaw_0.5_RC2_source_only.tar.bz2")
validpgpkeys=('6DD4217456569BA711566AC7F06E8FDE7B45DAAC') # Eric Vidal

build() {
	cd "kickshaw_0.5_RC2_source_only/source"
	
	make 
}

package(){

	cd "kickshaw_0.5_RC2_source_only/source"
	install -Dm755 kickshaw "$pkgdir/usr/local/bin/kickshaw"
	
	# license , copying readme in license directory for provide author 
	cd "../"
	install -Dm755 README "${pkgdir}/usr/share/licenses/kickshaw/README"
	install -Dm755 COPYING "${pkgdir}/usr/share/licenses/kickshaw/COPYING"
}
