# Maintainer: Yamada Hayao <hayao@fascode.net>
# Maintainer: Kevin Mihelich <kevin@archlinuxarm.org>

pkgname=archlinuxarm-keyring
pkgver=20140119
pkgrel=2
pkgdesc='Arch Linux ARM PGP keyring'
arch=('any')
url='http://archlinuxarm.org'
license=('GPL')
install="${pkgname}.install"
source=(
        "http://archlinuxarm.org/builder/src/${pkgname}-${pkgver}.tar.gz"
        #"http://archlinuxarm.org/builder/src/${pkgname}-${pkgver}.tar.gz.sig"
		0001-add-Atom-s-key.patch
)
md5sums=(
        '187140dd1078a4466f79f82f85a43f29'
        #'SKIP'
		'79d07b6d0e4ac0ba4072f31146c64069'
)

prepare() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  patch -Np1 -i ${srcdir}/0001-add-Atom-s-key.patch
}

package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	make PREFIX=/usr DESTDIR=${pkgdir} install
}
