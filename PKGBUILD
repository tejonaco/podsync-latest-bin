# Maintainer: tejonaco <tejonaco@gmail.com>
# Maintainer: Artem Vasilev <artem.vasilev@rwth-aachen.de>
# Creator:  Dimitris Kiziridis <ragouel at outlook dot com>

pkgname=podsync-latest-bin
pkgver=2.6.1
pkgrel=1
pkgdesc="Turn YouTube or Vimeo channels, users, or playlists into podcast feeds"
arch=('x86_64')
url='https://github.com/mxpv/podsync'
license=('MIT')
provides=('podsync')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/mxpv/podsync/releases/download/v${pkgver}/Podsync_${pkgver}_Linux_x86_64.tar.gz")
makedepends=('curl')
md5sums=("SKIP")

pkgver(){
	curl -s -X GET "https://api.github.com/repos/mxpv/podsync/releases" | jq '.[0].tag_name' -r | sed 's/^v//'
}

package() {
	  install -Dm644 LICENSE -t "${pkgdir}/usr/share/licenses/${pkgname}"
	    install -Dm644 *.md -t "${pkgdir}/usr/share/doc/${pkgname}"
	      install -Dm755 podsync "${pkgdir}/usr/bin/podsync"
      }
