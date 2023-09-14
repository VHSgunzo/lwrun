# Maintainer: VHSgunzo <vhsgunzo.github.io>

pkgname='runimage-rootfs-lwrun'
pkgver='0.39.1'
pkgrel='4'
pkgdesc='Rootfs configuration for RunImage container'
url="https://github.com/VHSgunzo/lwrun"
license=('MIT')
arch=('any')
source=(
    'git+https://github.com/VHSgunzo/runimage-rootfs.git'
    'rootfs.tar.gz'
)
sha256sums=('SKIP' 'SKIP')
provides=('filesystem=2023.01.31')
conflicts=(
    'filesystem'
    'runimage-rootfs'
    'runimage-rootfs-portarch'
)
# install='lwrun.install'

package() {
    cp -arTf --no-preserve=ownership "$srcdir/runimage-rootfs/rootfs" "$pkgdir"
    cp -arTf --no-preserve=ownership "$srcdir/rootfs" "$pkgdir"
}
