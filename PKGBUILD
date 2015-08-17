# Maintainer: Lukas Jirkovsky <l.jirkovsky@gmail.com>
pkgname=ocropus-models
pkgver=0.5.4
pkgrel=1
pkgdesc="State-of-the-art document analysis and OCR system"
arch=('any')
url="http://code.google.com/p/ocropus/"
license=('APACHE')
makedepends=('curl')
source=("http://ocropus.googlecode.com/hg-history/ocropus-$pkgver/ocroinst")
md5sums=('65afad44f14a1ae73899ec04e2de60f2')

package() {
  cd "$srcdir"

  # download and install models
  sed "s|^datadir=.*|datadir=$pkgdir/usr/share/ocropus|" -i ocroinst
  sh ocroinst dl
}

# vim:set ts=2 sw=2 et:
