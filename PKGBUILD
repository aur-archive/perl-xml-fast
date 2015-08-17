# Maintainer: trizen .= x@gmail.com

pkgname=perl-xml-fast
pkgver=0.11
pkgrel=2
pkgdesc="Simple and very fast XML to hash conversion."
arch=('any')
url="http://search.cpan.org/dist/XML-Fast/"
license=('GPL' 'PerlArtistic')
depends=('perl')
options=('!emptydirs')
source=("http://search.cpan.org/CPAN/authors/id/M/MO/MONS/XML-Fast-${pkgver}.tar.gz")
md5sums=('a2985cc2f328cf9eda6ad75c3f40f6b3')

build() {
  cd ${srcdir}/XML-Fast-${pkgver}
  PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor
  make
}

package() {
  cd ${srcdir}/XML-Fast-${pkgver}
  make install DESTDIR=${pkgdir}
  find ${pkgdir} -name '.packlist' -delete
  find ${pkgdir} -name '*.pod' -delete
}
