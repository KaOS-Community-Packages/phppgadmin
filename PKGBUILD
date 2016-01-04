pkgname=phppgadmin
pkgver=5.1
pkgrel=1
pkgdesc="A web-based administration tool for PostgreSQL"
arch=('x86_64')
url="http://sourceforge.net/projects/phppgadmin"
license=('GPL')
depends=('php')
backup=('etc/webapps/phppgadmin/config.inc.php')
source=(http://downloads.sourceforge.net/sourceforge/$pkgname/phpPgAdmin-$pkgver.tar.gz)
md5sums=('554c94f5b38a1c6e8327ec3aa4cc6538')

package() {
  _instdir=$pkgdir/usr/share/webapps/phppgadmin
  mkdir -p ${_instdir} $pkgdir/etc/webapps/phppgadmin
  cd ${_instdir}
  cp -ra $srcdir/phpPgAdmin-$pkgver/* .
  cp ./conf/config.inc.php-dist $pkgdir/etc/webapps/phppgadmin/config.inc.php
  rm -f ${_instdir}/conf/config.inc.php
  ln -s /etc/webapps/phppgadmin/config.inc.php ${_instdir}/conf/config.inc.php
}
