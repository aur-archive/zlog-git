# Maintainer: Gustavo Alvarez <sl1pkn07@gmail.com>
# Contributor: Chase Geigle <sky@skystrife.com>

pkgname=zlog-git
pkgver=1.2.8.23.g5395842
pkgrel=1
pkgdesc="A flexible, fast, and thread-safe logger for C"
arch=('i686' 'x86_64')
url="http://hardysimpson.github.io/zlog/"
license=('GPLv3')
makedepends=('git')
provides=('zlog')
conflicts=('zlog')
source=('zlog::git+https://github.com/HardySimpson/zlog.git')
md5sums=('SKIP')
_hgrepo="zlog"

pkgver() {
  cd "${srcdir}/${_hgrepo}"
  git describe --always | sed 's|-|.|g'
}

build() {
  cd "${srcdir}/${_hgrepo}"
  make
}

package() {
  cd "${srcdir}/${_hgrepo}"
  make PREFIX="${pkgdir}/usr" install
}
