# Maintainer: Tom Debruyne <tomdebruyne at gmail dot com>
pkgname=cputemp
pkgver=1.0.1
pkgrel=2
pkgdesc="A tool to monitor CPU Temperature from command line"
arch=('i686' 'x86_64')
license=('GPL')
depends=('python2')
url=('http://py-cputemp.sourceforge.net/')
source=(http://downloads.sourceforge.net/project/py-cputemp/$pkgname/$pkgname-$pkgver/$pkgname-$pkgver.tar.gz)
md5sums=('2a1e42a2c850c6f4ec99fe19cf0596ee')

package() {
	cd $srcdir/$pkgname-$pkgver
        install -dm755 ${pkgdir}/usr/bin
        install -dm755 ${pkgdir}/var/log
        python2 ./Setup.py --binprefix=${pkgdir}/usr --logpath=${pkgdir}/var/log
        sed -i -e '1 s/python/python2/' ${pkgdir}/usr/bin/cputemp
      

}
