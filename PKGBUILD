# Maintainer: metislinux.org <info@metislinux.org>
pkgname=rankmirrors
pkgver=r4.a76d0e8
pkgrel=1
pkgdesc="read a list of mirrors from a file and rank them by speed"
arch=('any')
url="https://github.com/metis-os/metis-rankmirrors"
license=('MIT')
makedepends=('git')
depends=('bash')
provides=("${pkgname}")
options=(!strip !emptydirs)
source=(${pkgname}::"git+${url}")
sha256sums=('SKIP')

package() {
    cd "metis-$pkgname-master/files"
	install -Dm754 ./rankmirrors "${pkgdir}/usr/bin/rankmirrors"
}

pkgver() {
  cd "metis-$pkgname-master"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}
