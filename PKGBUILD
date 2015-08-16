# Maintainer: Antonio Rojas <nqn1976 @ gmail.com>

pkgname=libqinfinity
pkgver=0.5.1
pkgrel=1
pkgdesc="Qt wrapper around libinfinity, a library for collaborative editing"
arch=('i686' 'x86_64')
url='https://projects.kde.org/projects/playground/libs/libqinfinity'
license=('LGPL')
depends=('libinfinity' 'qt4')
makedepends=('cmake')
source=("http://download.kde.org/stable/$pkgname/$pkgver/src/$pkgname-v$pkgver.tar.xz")
md5sums=('ca40902e7a9a699d3d83138cb76d569a') 

build() {
	cd "$pkgname-v$pkgver"
	mkdir build
	cd build
	cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr -DQT_QMAKE_EXECUTABLE=/usr/bin/qmake-qt4
	make
}

package() {
	cd "$pkgname-v$pkgver/build"
	make DESTDIR="$pkgdir" install
}
