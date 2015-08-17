# Maintainer: Marti Raudsepp <marti@juffo.org>
# Contributor: Sven-Hendrik Haase <sh@lutzhaase.com>
pkgname=pypy-bin
pkgver=1.8
pkgrel=2
pkgdesc="Python interpreter and JIT written in Python"
url="http://pypy.org/"
arch=('i686' 'x86_64')
depends=('python2' 'libffi' 'openssl098' 'ncurses' 'expat' 'zlib' 'bzip2')
conflicts=('pypy')
provides=("pypy=$pkgver")
license=('MIT')

[ "${CARCH}" = "i686"   ] && source=(https://bitbucket.org/pypy/pypy/downloads/pypy-$pkgver-linux.tar.bz2)
[ "${CARCH}" = "x86_64" ] && source=(https://bitbucket.org/pypy/pypy/downloads/pypy-$pkgver-linux64.tar.bz2)
[ "${CARCH}" = "i686"   ] && md5sums=('c4a1d11e0283a390d9e9b801a4633b9f')
[ "${CARCH}" = "x86_64" ] && md5sums=('3b81363ccbc042dfdda2fabbf419e788')

build() {
  return 0
}
package()
{
  name=pypy-$pkgver

  mkdir -p $pkgdir/usr/share/licenses/$pkgname/
  cp $srcdir/$name/LICENSE $pkgdir/usr/share/licenses/$pkgname

  mkdir -p $pkgdir/opt/
  mv $srcdir/$name $pkgdir/opt/pypy

  mkdir -p $pkgdir/usr/bin/
  ln -s /opt/pypy/bin/pypy $pkgdir/usr/bin/pypy
}

# vim: ts=2 sw=2 et:
