# Contributor: Peter Kosyh <p.kosyhgmail.com>

pkgname=instead
pkgver=1.8.0
pkgrel=1
pkgdesc="instead quest interpreter"
arch=('i686' 'x86_64')
url="http://instead.googlecode.com/"
license=('GPL')
depends=('sdl_image' 'sdl_mixer' 'sdl_ttf' 'lua')
source=(http://instead.googlecode.com/files/instead_${pkgver}.tar.gz)
md5sums=(08acf9f7de60b8e1c23d6e9368093d1f)

optdepends=('instead-launcher: install and update INSTEAD games from net')

build() {
cd "${srcdir}/instead-${pkgver}"

echo "2" | ./configure.sh
make PREFIX=/usr
}

package() {
cd "${srcdir}/instead-${pkgver}"

make DESTDIR="${pkgdir}" PREFIX=/usr install
}
