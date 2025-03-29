# Maintainer: VHSgunzo <vhsgunzo.github.io>

pkgname='runimage-rootfs-lwrun'
pkgver='0.40.7'
pkgrel='1'
pkgdesc='Rootfs configuration for RunImage container'
url="https://github.com/VHSgunzo/lwrun"
license=('MIT')
arch=('x86_64')
source=(
    'git+https://github.com/VHSgunzo/runimage-rootfs.git'
    'rootfs.tar'
)
sha256sums=('SKIP' 'SKIP')
provides=('filesystem=2024.11.21')
depends=('runimage-utils')
conflicts=(
    'runimage-rootfs'
    'runimage-rootfs-portarch'
)
install='lwrun.install'

package() {
    cp -arTf --no-preserve=ownership "$srcdir/runimage-rootfs/rootfs" "$pkgdir"
    install -Dm644 "$srcdir/runimage-rootfs/mirrorlist-x86_64" "$pkgdir/var/rootfs/etc/pacman.d/mirrorlist"
    cp -arTf --no-preserve=ownership "$srcdir/rootfs" "$pkgdir"
    find "$pkgdir" -type f -name '.keep' -exec rm -f {} \;
}
