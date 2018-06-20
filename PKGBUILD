# Maintainer: Gui||aume <michaudg@gmail.com>

pkgname=rocketchat-client-bin
pkgver=2.11.0
pkgrel=1
pkgdesc="The Ultimate Open Source Web Chat Platform"
arch=('x86_64')
license=('The MIT License (MIT)')
url="https://rocket.chat"
options=()

source_x86_64=("https://github.com/RocketChat/Rocket.Chat.Electron/releases/download/${pkgver}/rocketchat_${pkgver}_amd64.deb"
               "rocketchat.sh")
md5sums_x86_64=('77fdb26dd69034f8fc0fdda49bce4b7e'
                '06d1a6b04291d97e4d70f33e42a8a0a3')

depends=('libnotify' 'gconf' 'libxss')
optdepends=()

package() {
    cd "${srcdir}"

    tar xf data.tar.xz -C "${pkgdir}"

    mkdir -p "$pkgdir/usr/bin"
    install -m755 rocketchat.sh "$pkgdir"/usr/bin/rocketchat
}
