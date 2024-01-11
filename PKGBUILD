# Maintainer: Sefa Eyeoglu <contact@scrumplex.net>
# Contributor: Alexandros Theodotou <alex at zrythm dot org>

pkgname=lsp-dsp-lib
pkgver=1.0.20
pkgrel=1
pkgdesc='DSP library for signal processing'
arch=('any')
url='https://github.com/sadko4u/lsp-dsp-lib'
license=('LGPL3')
makedepends=('pkg-config')
source=("https://github.com/sadko4u/$pkgname/releases/download/$pkgver/$pkgname-src-$pkgver.tar.gz")
sha512sums=('beaf252dd9deeb02183287394c27cb089d17edba73e94c723256db39be050109cf769535ada6ca87e942af97464ca614f4cd813f03ab894e39f658e553ca0681')

build() {
  cd "$pkgname"

  make config PREFIX=/usr
  cat ./.config.mk
  #make fetch
  make
}

package() {
  cd "$pkgname"

  make DESTDIR="$pkgdir" install
}
