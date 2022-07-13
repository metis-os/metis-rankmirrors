# Maintainer: metislinux.org <info@metislinux.org>
pkgname=rankmirrors
pkgver=1.5.5
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
	install -Dm754 "${srcdir}/files/rankmirrors" "${pkgdir}/usr/bin/rankmirrors"
}

pkgver() {
  cd "$pkgname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}
