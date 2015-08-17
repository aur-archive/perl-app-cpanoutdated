# Maintainer : Simon Hollingshead <me at [firstnamelastname] dot com>
# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-app-cpanoutdated'
pkgver='0.28'
pkgrel='2'
pkgdesc="cpan-outdated - detect outdated CPAN modules in your environment"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl' 'perl-cpan-distnameinfo>=0.1' 'perl-libwww' 'perl-local-lib>=1.006008')
makedepends=()
url='http://search.cpan.org/dist/cpan-outdated'
source=('http://search.cpan.org/CPAN/authors/id/T/TO/TOKUHIROM/cpan-outdated-0.28.tar.gz')
md5sums=('3f0dbeb84a9c854dc31b090f09880f84')
sha512sums=('fa011be0393f1c22685b4ad2ff26a71a3b2ba045fdf489ce40e716dfd6610d718fbcb0769567493b1895232c993ef49ce10fb242a37ad04999aaefe0aa223e59')
_distdir="cpan-outdated-0.28"

build() {
    cd "$srcdir/$_distdir"

    export PERL_MM_USE_DEFAULT=1 PERL_AUTOINSTALL=--skipdeps \
    PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'" \
    PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
    MODULEBUILDRC=/dev/null

    /usr/bin/perl Build.PL
    /usr/bin/perl Build 
}

check() {
  cd "$srcdir/$_distdir"

  export PERL_MM_USE_DEFAULT=1 PERL_AUTOINSTALL=--skipdeps \
  PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'" \
  PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
  MODULEBUILDRC=/dev/null

  /usr/bin/perl Build test
}

package() {
  cd "$srcdir/$_distdir"

  export PERL_MM_USE_DEFAULT=1 PERL_AUTOINSTALL=--skipdeps \
  PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'" \
  PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
  MODULEBUILDRC=/dev/null

  /usr/bin/perl Build install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
