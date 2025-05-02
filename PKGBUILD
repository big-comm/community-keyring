# Maintainer: Tales A. Mendonça <talesam@gmail.com>

pkgname=community-keyring
pkgdesc="Community PGP keyring"
depends=('pacman')
pkgver=$(date +%y.%m.%d)
pkgrel=$(date +%H%M)
arch=('any')
license=('MIT')
url="https://github.com/big-comm/${pkgname}"
source=("git+${url}.git")
sha256sums=('SKIP')
install="${pkgname}.install"

prepare() {
  cd "${srcdir}/${pkgname}"
  
  echo "d8009d2e09b0e9e305ccc7450eb840e8fa0b7956bb34c7c336b5bd891fac7c3e Makefile" | sha256sum -c || exit 1
  echo "41cbeb67f535495deb012c77216949ce6ef1344d1238894b45de589423441264 community.gpg" | sha256sum -c || exit 1
  echo "e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 community-revoked" | sha256sum -c || exit 1
  echo "6c6019d563905d64fbb960272268c13b027f4851e0f1666fee52d4bfeeb70484 community-trusted" | sha256sum -c || exit 1
}

package() {
  cd "${srcdir}/${pkgname}"
  make DESTDIR="${pkgdir}" install
}
