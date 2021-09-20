# Maintainer: Matthew Spangler (mattspangler@protonmail.com)

# SecureCRT software is owned and copyrighted by Vandyke Inc. The software is free to download for eval and requires a separately purchased license for full features and support

## To install this package, you need to download the SecureCRT for Linux package in tar.gz format and place it in the same directory as the PKGBUILD

## Ensure the 'pkgver' and 'pkgrel' variables are updated below to match your package version

pkgname=scrt-sfx
pkgver=9.1.0
pkgrel=2579
pkgdesc='SecureCRT + SecureFX 9.0 Bundle'
arch=('x86_64')
url='https://www.vandyke.com/'
license=('custom:VanDyke')
depends=('fontconfig' 'freetype2' 'gcc-libs' 'glibc' 'krb5' 'libcups' 'libpng'
  'libx11' 'libxcb' 'libxkbcommon' 'libxkbcommon-x11' 'openssl'
  'qt5-base' 'qt5-multimedia' 'xcb-util-image' 'xcb-util-keysyms'
  'xcb-util-renderutil' 'xcb-util-wm' 'zlib' 'icu66')
options=('!strip' '!emptydirs')
provides=('SecureCRT' 'SecureFX')
source=("local://${pkgname}-${pkgver}.${pkgrel}.ubuntu20-64.tar.gz")
md5sums=('5c67d0a51af27bb8f18546a885b5ffbe')


package() {
      cd "${srcdir}"/${pkgname}-${pkgver}

      install -Dm 755 ./SecureCRT ${pkgdir}/usr/bin/SecureCRT
      install -Dm 755 ./SecureFX ${pkgdir}/usr/lib/securefx/SecureFX

      install -Dm 755 ./libClientConfigUiQt.so ${pkgdir}/usr/lib/scrt/libClientConfigUiQt.so
      install -Dm 755 ./libQt5Multimedia.so.5 ${pkgdir}/usr/lib/scrt/libQt5Multimedia.so.5
      install -Dm 755 ./libpython3Qt.so ${pkgdir}/usr/lib/scrt/libpython3Qt.so
      install -Dm 755 ./libibusplatforminputcontextplugin.so ${pkgdir}/usr/lib/scrt/plugins/platforminputcontexts/libibusplatforminputcontextplugin.so
      install -Dm 755 ./libcomposeplatforminputcontextplugin.so ${pkgdir}/usr/lib/scrt/plugins/platforminputcontexts/libcomposeplatforminputcontextplugin.so
      install -Dm 755 ./libqxcb.so ${pkgdir}/usr/lib/scrt/plugins/platforms/libqxcb.so
      install -Dm 755 ./libCommonUiQt.so ${pkgdir}/usr/lib/scrt/libCommonUiQt.so
      install -Dm 755 ./libQt5Gui.so.5 ${pkgdir}/usr/lib/scrt/libQt5Gui.so.5
      install -Dm 755 ./libQt5PrintSupport.so.5 ${pkgdir}/usr/lib/scrt/libQt5PrintSupport.so.5
      install -Dm 755 ./libQt5Core.so.5 ${pkgdir}/usr/lib/scrt/libQt5Core.so.5
      install -Dm 755 ./libQt5Widgets.so.5 ${pkgdir}/usr/lib/scrt/libQt5Widgets.so.5
      install -Dm 755 ./libQt5Network.so.5 ${pkgdir}/usr/lib/scrt/libQt5Network.so.5
      install -Dm 755 ./libQt5XcbQpa.so.5 ${pkgdir}/usr/lib/scrt/lib/libQt5XcbQpa.so.5
      install -Dm 755 ./libQt5DBus.so.5 ${pkgdir}/usr/lib/scrt/lib/libQt5DBus.so.5

      install -Dm 644 ./SecureCRT_fr.qm ${pkgdir}/usr/share/vandyke/data/SecureCRT_fr.qm
      install -Dm 644 ./SecureCRT_README.txt ${pkgdir}/usr/share/doc/scrt/SecureCRT_README.txt
      install -Dm 644 ./SecureCRT_SecureFX_Ubuntu_Copyright.txt ${pkgdir}/usr/share/doc/scrt/copyright
      install -Dm 644 ./SecureCRT_SecureFX_EULA.txt ${pkgdir}/usr/share/doc/scrt/SecureCRT_EULA.txt
      install -Dm 644 ./SecureCRT_HISTORY.txt ${pkgdir}/usr/share/doc/scrt/SecureCRT_HISTORY.txt
      install -Dm 644 ./changelog.Debian.gz ${pkgdir}/usr/share/doc/scrt/changelog.Debian.gz

      cp -rp ./SecureCRTHelp ${pkgdir}/usr/share/doc/scrt/SecureCRTHelp

      install -Dm 644 ./securecrt_64.png ${pkgdir}/usr/share/vandyke/data/securecrt_64.png
      install -Dm 644 ./SecureCRT.desktop ${pkgdir}/usr/share/applications/SecureCRT.desktop
      install -Dm 644 ./SecureFX.desktop ${pkgdir}/usr/share/applications/SecureFX.desktop
      install -Dm 644 ./securefx_64.png ${pkgdir}/usr/share/vandyke/data/securefx_64.png
}
