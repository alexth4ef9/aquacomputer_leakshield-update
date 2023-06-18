pkgname=aquacomputer_leakshield
pkgver=1.0
pkgrel=1
pkgdesc="aquacomputer leakshield update service"
arch=('any')
license=('MIT')
depends=('python'
         'systemd'
         'aquacomputer_d5next-dkms')
conflicts=("${pkgname}")
source=("aquacomputer-leakshield"
        "aquacomputer-leakshield.service")
md5sums=('ce17b3dc1e16da19bbd06a0ca1db82ca'
         'b06509c4e5c1599f498ad3a7036b6f52')
prepare() {
    return 0
}

package() {
    # copy service
    install -Dm755 aquacomputer-leakshield "${pkgdir}"/usr/local/bin/aquacomputer-leakshield

    # copy serice unit
    install -Dm644 aquacomputer-leakshield.service "${pkgdir}"/etc/systemd/system/aquacomputer-leakshield.service
}
