# Maintainer: xsigil <xsigil@users.noreply.github.com>
pkgname=toc2pikchr
pkgver=1.0.0
pkgrel=1
pkgdesc="CLI tool to convert table of contents into pikchr diagram scripts"
arch=('x86_64')
url="https://github.com/xsigil/toc2pikchr"
license=('MIT')
depends=('glibc')
makedepends=('gcc' 'make' 'flex' 'bison')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/xsigil/${pkgname}/archive/refs/tags/v${pkgver}.tar.gz")
sha256sums=('0a8ae94aad723088e9178636bacc122931fd4e124df1c03f1cf11e8a8ec68c10')

build() {
    cd "${pkgname}-${pkgver}"
    make
}

package() {
    cd "${pkgname}-${pkgver}"
    install -Dm755 build/toc2pikchr "${pkgdir}/usr/bin/toc2pikchr"

    if [ -f LICENSE ]; then
        install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    fi
}
