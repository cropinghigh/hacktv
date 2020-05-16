# Maintainer: fsphil <phil@sanslogic.co.uk>
# Modified by Indir <joinmark60@gmail.com>

pkgname=hacktv
pkgver=f3504c
pkgrel=1
pkgdesc="Analog TV transmitter."
arch=('i686' 'x86_64')
url="https://github.com/cropinghigh/hacktv"
license=('GPL')
depends=(
    'hackrf'
    'ffmpeg'
    )
makedepends=(
    'git'
    'cmake'
    )
#optdepends=()
provides=('hacktv')

source=('git+https://github.com/cropinghigh/hacktv.git')
md5sums=('SKIP')
_gitname="hacktv"

pkgver() {
  cd $_gitname
  git describe --always | sed 's|-|.|g; s|^.||'
}

build() {
  cd "$srcdir/$_gitname"
  make
}

package() {
  cd "$srcdir/$_gitname/"
  make DESTDIR=${pkgdir} install
}
