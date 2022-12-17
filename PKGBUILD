pkgname=ufetch-artix
pkgver=0.3.r0.g12b68fa
pkgrel=1
pkgdesc='Tiny system info for Unix-like operating systems'
arch=(any)
url=https://gitlab.com/jschx/ufetch
license=(MIT)
makedepends=(git)
source=("git+${url}.git")
md5sums=('SKIP')

pkgver() {
	cd "$srcdir/${pkgname%-artix}"
	git describe --long --tags | sed 's/^v//;s/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
	cd "${srcdir}/${pkgbase%-artix}"
	install -Dm755 "${pkgbase%-artix}-artix" "${pkgdir}/usr/bin/${pkgname%-artix}"
	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname%-artix}/LICENSE"
}