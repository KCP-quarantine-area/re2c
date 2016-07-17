pkgname=re2c
pkgver=0.16
pkgrel=1
arch=(x86_64)
depends=(gcc-libs)
pkgdesc='A tool for generating C-based recognizers from regular expressions'
url='http://re2c.sourceforge.net/'
license=(GPL)
source=(http://downloads.sourceforge.net/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('3bf508fabd52ed7334647d0ccb956e8d')

build() {
  cd $pkgname-$pkgver
  ./configure --prefix=/usr
  make
}

check() {
  cd $pkgname-$pkgver
  make tests
}

package() {
  cd $pkgname-$pkgver
  make DESTDIR="$pkgdir" install
}
