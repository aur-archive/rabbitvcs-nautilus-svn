# Maintainer: Patryk Szalanski <patryk.szalanski+aur@gmail.com>
pkgname=rabbitvcs-nautilus-svn
pkgver=r3231
pkgrel=2
pkgdesc="Nautilus front-end for RabbitVCS."
arch=('i686' 'x86_64')
url="http://code.google.com/p/rabbitvcs/"
license=('GPL')
depends=('nautilus>=2.22.0' 'python2-nautilus>=0.7.0-2' 'python2-gnomevfs' 'dbus-python>=0.80' 'rabbitvcs-svn')
makedepends=('subversion')
provides=('rabbitvcs-nautilus')
conflicts=('rabbitvcs-nautilus')
install=rabbitvcs-nautilus-svn.install
source=("rabbitvcs::svn+http://rabbitvcs.googlecode.com/svn/trunk/")
noextract=()
md5sums=(SKIP) #generate with 'makepkg -g'

_svntrunk=http://rabbitvcs.googlecode.com/svn/trunk/
_svnmod=rabbitvcs

pkgver(){
  cd "$srcdir/$_svnmod"
  local ver="$(svnversion)"
  printf "r%s" "${ver//[[:alpha:]]}"
}

package() {
  install -D "$srcdir/rabbitvcs/clients/nautilus-3.0/RabbitVCS.py" "$pkgdir/usr/share/nautilus-python/extensions/RabbitVCS.py"
}

