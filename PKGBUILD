# Maintainer: Jaroslav Lichtblau <dragonlord@aur.archlinux.org>
# Contributor: Ian Snow <ian.snow@btinternet.com>

pkgname=knetstats
pkgver=1.6.2
pkgrel=1
pkgdesc="A simple KDE network monitor"
arch=('i686' 'x86_64')
url="http://knetstats.sourceforge.net/"
license=('GPL')
depends=('kdelibs3' 'qt3')
source=(http://downloads.sourceforge.net/sourceforge/$pkgname/$pkgname-$pkgver.tar.bz2)
md5sums=('6d437b702ce41403575cec5c94a8ae94')

build() {
  cd "${srcdir}"/$pkgname-$pkgver

  source /etc/profile.d/qt3.sh

  ./configure --prefix=/opt/kde --without-arts
  make
}

package() {
  cd "${srcdir}"/$pkgname-$pkgver

  make DESTDIR="${pkgdir}" install
}
