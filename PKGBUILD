# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=nfs-utils-s6serv
pkgver=0.2
pkgrel=1
pkgdesc="nfs-utils service for s6"
arch=(x86_64)
license=('beerware')
depends=('nfs-utils' 's6' 's6-rc' 's6-boot')
conflicts=()
install=nfs-utils-s6serv.install
source=('nfs-utils.daemon.finish.s6'
		'nfs-utils.daemon.run.s6'
		'nfs-utils.log.run.s6'
		'LICENSE')
md5sums=('41eb983805469d677e40f69e0793b8b5'
         'ebbbf41165a4c01416b70096fbfdd83a'
         '5dbff003a88135827a706dcb690bd509'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/nfs-utils.daemon.finish.s6" "$pkgdir/etc/s6-serv/available/classic/nfs-utils/finish"
	install -Dm 0755 "$srcdir/nfs-utils.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/nfs-utils/run"
	
	# log
	install -Dm 0755 "$srcdir/nfs-utils.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/nfs-utils/log/run"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/nfs-utils-s6serv/LICENSE"
}
