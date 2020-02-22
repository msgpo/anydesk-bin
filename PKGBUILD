pkgname=anydesk
pkgver=5.5.3
pkgrel=1
pkgdesc="'AnyDesk Free' is an All-In-One Software for Remote Support"
arch=('i686' 'x86_64')
url="https://anydesk.com"
license=('custom:Freeware')
depends=('fakeroot' 'python-shiboken2' 'gtkglext' 'libglvnd' 'gtk2' 'libx11' 'glibc' 'glib2' 'gdk-pixbuf2' 'libxcb' 'cairo' 'pango' 'libxi' 'libxrandr' 'libxtst' 'libxext' 'libxfixes' 'libxdamage' 'gcc-libs')
optdepends=('libpulse')

source_i686=(https://download.anydesk.com/linux/anydesk-${pkgver}-i386.tar.gz)
source_x86_64=(https://download.anydesk.com/linux/anydesk-${pkgver}-amd64.tar.gz)

sha256sums_i686=('9e99cebe0229a01ccd519255874ebaad0fea28466f2f6261ba35f6b9317a24ba')
sha256sums_x86_64=('784c051ee0a1d9fbb4238a246d11e4fa5df6538a5b64cbfce13559a09b6dc3fa')

package() {
    install -Dm 755 "${srcdir}/anydesk-${pkgver}/anydesk" "${pkgdir}/usr/bin/anydesk"
    install -Dm 644 "${srcdir}/anydesk-${pkgver}/anydesk.desktop" "${pkgdir}/usr/share/applications/anydesk.desktop"
    msg2 "\e[1;32mAnyDesk has a systemd service for unattended access. Enable it with: systemctl enable --now anydesk \e[0m"
    install -Dm 644 "${srcdir}/anydesk-${pkgver}/systemd/anydesk.service" "${pkgdir}/usr/lib/systemd/system/anydesk.service"
}
