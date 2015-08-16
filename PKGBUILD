# Maintainer: Antonio Vázquez Blanco <antoniovazquezblanco[at]gmail[dot]com>

pkgname=mineshafter
pkgver=7.0
pkgrel=1
pkgdesc="Mineshafter is an authentication and texture proxy for Minecraft."
arch=(any)
license=('unknown')
url="http://mineshafter.info/"
depends=('minecraft')
provides=('mineshafter')
source=('mineshafter'
        'Mineshafter.jar'
        'mineshafter.desktop'
        'mineshafter.png')
md5sums=('29ab715581bba68240cff1a21913a346'
         '24e003229cb67b0d75e7aa5e6c2ae9b0'
         'c8c897299487b6454f5c1268979762c6'
         'd2d898ab75604fcc92980a0a7db96a98')
noextract=('Mineshafter.jar')

package() {
	cd "$srcdir" || return 1

	install -D -m755 "${srcdir}/mineshafter" "${pkgdir}/usr/bin/mineshafter"
	install -D -m644 "${srcdir}/Mineshafter.jar" "${pkgdir}/usr/share/minecraft/Mineshafter.jar"

	# Desktop launcher with icon
	install -D -m644 "${srcdir}/mineshafter.desktop" "${pkgdir}/usr/share/applications/mineshafter.desktop"
	install -D -m644 "${srcdir}/mineshafter.png" "${pkgdir}/usr/share/pixmaps/mineshafter.png"
}
