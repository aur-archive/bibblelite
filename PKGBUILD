# Maintainer: Mymaud <mymaud@gmail.com>

pkgname=bibblelite
_pkgname=bibble5
pkgver=5.2.3
_pkgver=5.2-3
pkgrel=1
pkgdesc="Professional Workflow and RAW Conversion"
arch=('i686' 'x86_64')
license=('custom')

depends=('rpmextract' 'qt' 'libxdamage' 'glib2' 'pcre' 'libpng12' 'libgl')
[ "$CARCH" = "x86_64" ] && depends=('rpmextract' 'lib32-qt' 'lib32-libxdamage' 'lib32-glib2' 'lib32-pcre' 'lib32-libpng12' 'lib32-libgl' 'lib32-mesa')

conflicts=('bibblepro' 'bibble5pro' 'bibble5pro-pv')
source=("http://edge.bibblelabs.com/523-20111213/${_pkgname}-${_pkgver}.i386.rpm" \
	"LICENSE")
url="http://www.bibblelabs.com"
md5sums=('af3607d6caaab74b2f874b7d29410a1b'
         '6d94c13f40223b03d72f5ef682643525')

build() {
	install -d ${startdir}/pkg/usr/share/licenses/${pkgname}
	install -D -m644 ${startdir}/LICENSE ${startdir}/pkg/usr/share/licenses/${pkgname}/

	rpmextract.sh ${_pkgname}-${_pkgver}.i386.rpm

	mv  ${srcdir}/opt ${pkgdir}/
	mv  ${srcdir}/usr/bin ${pkgdir}/usr/
	mv  ${srcdir}/usr/share/{applications,pixmaps} ${pkgdir}/usr/share/
	}
