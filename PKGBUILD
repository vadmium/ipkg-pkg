# Contributor: Olivier Mehani <olivier.mehani@inria.fr>
# $Id$

pkgname=ipkg
pkgver=0.99.163
pkgrel=1
pkgdesc="The Itsy Package Management System"
url="http://handhelds.org/moin/moin.cgi/Ipkg"
source=(http://www.handhelds.org/download/packages/${pkgname}/${pkgname}-${pkgver}.tar.gz)
md5sums=('0b10ad2924611bccaea8ddf98481a192')

build() {
	cd $startdir/src/$pkgname-$pkgver
	./configure --prefix=/usr || exit 1
	make || exit 2
	make DESTDIR=$startdir/pkg install || return 3
}
