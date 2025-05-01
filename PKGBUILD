# Community <talesam[at]gmail.com>

# Manjaro credits
# Maintainer: Philip Müller <philm[at]manjaro[dot]org>
# Maintainer: Bernhard Landauer <bernhard[at]manjaro[dot]org>

# Arch credits:
# Pierre Schmitz <pierre@archlinux.de>

pkgname=community-keyring
pkgdesc="Community PGP keyring"
depends=('pacman')
pkgver=$(date +%y.%m.%d)
pkgrel=$(date +%H%M)
arch=('any')
license=('MIT')
url="https://github.com/big-comm/${pkgname}"
source=("Makefile"
        "community.gpg"
        "community-revoked"
        "community-trusted")
sha256sums=('d8009d2e09b0e9e305ccc7450eb840e8fa0b7956bb34c7c336b5bd891fac7c3e'
            '41cbeb67f535495deb012c77216949ce6ef1344d1238894b45de589423441264'
            'e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855'
            '6c6019d563905d64fbb960272268c13b027f4851e0f1666fee52d4bfeeb70484')
install="${pkgname}.install"

package() {
    cd "${srcdir}"
    make DESTDIR="${pkgdir}" install
}
