# Contributor: C Anthony Risinger

pkgname=mkinitcpio-btrfsadm
pkgver=0.4.0
pkgrel=1
pkgdesc='Extensive hook for operations on a BTRFS root device'
url='https://github.com/extofme/mkinitcpio-btrfsadm'
arch=('any')
license=('BSD')
backup=('etc/mkbootcpio.conf')
install=PKGINST.${pkgname}
depends=('btrfs-progs' 'btrfsadm')
conflicts=('mkinitcpio-btrfs')
provides=('mkinitcpio-btrfs')
source=('btrfsadm_bootramfs.inst'
        'btrfsadm_bootramfs.preset'
        'btrfsadm.hook'
        'btrfsadm.inst'
        'btrfsadm.init'
        'mkbootcpio.conf'
        'PKGINST.mkinitcpio-btrfsadm')

build() { return; }

package() {

    install -o root -g root -D \
        ${srcdir}/btrfsadm_bootramfs.inst ${pkgdir}/lib/initcpio/install/btrfsadm_bootramfs
    install -o root -g root -D \
        ${srcdir}/btrfsadm_bootramfs.preset ${pkgdir}/etc/mkinitcpio.d/btrfsadm_bootramfs.preset
    install -o root -g root -D \
        ${srcdir}/btrfsadm.hook ${pkgdir}/lib/initcpio/hooks/btrfsadm
    install -o root -g root -D \
        ${srcdir}/btrfsadm.inst ${pkgdir}/lib/initcpio/install/btrfsadm
    install -o root -g root -D \
        ${srcdir}/btrfsadm.init ${pkgdir}/lib/initcpio/btrfsadm/init
    install -o root -g root -D \
        ${srcdir}/mkbootcpio.conf ${pkgdir}/etc/mkbootcpio.conf

}
