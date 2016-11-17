pkgname=flatplat-theme-laptop
epoch=1
pkgver=3.22.20161109
pkgrel=2
pkgdesc="A Material Design-like flat theme for GTK3, GTK2, Metacity, and GNOME-Shell. This package does not contain chrome skin extension."
arch=('any')
url="https://github.com/nana-4/Flat-Plat"
license=('GPL')
depends=('gtk3>=3.22','gtk-engine-murrine', 'gnome-themes-standard')
optdepends=()
provides=('flatplat-theme-laptop')
conflicts=('flatplat-theme-laptop-git')
replaces=()
source=("https://github.com/nana-4/Flat-Plat/releases/download/v${pkgver}/Flat-Plat-laptop-${pkgver}.tar.gz"
        "https://github.com/nana-4/Flat-Plat/releases/download/v${pkgver}/Flat-Plat-light-laptop-${pkgver}.tar.gz")
sha256sums=('c8153b7ff56411a0bc2179df06b4ed9987f5c83f8350da8c704a679393df8e58'
            'ab394b9d034ccaeb28ec68f55f444640563e4332474440f4b907ab68674b3abb')

package() {
  cd "Flat-Plat-laptop"
  install -dm 755 "${pkgdir}"/usr/share/themes/Flat-Plat-laptop
  rm -rf chrome img
  sed -i 'index.theme' -e "s/Flat-Plat/Flat-Plat-laptop/g"
  cp -dr --no-preserve='ownership,mode' * "${pkgdir}"/usr/share/themes/Flat-Plat-laptop
  cd ..
  cd "Flat-Plat-light-laptop"
  install -dm 755 "${pkgdir}"/usr/share/themes/Flat-Plat-light-laptop
  rm -rf chrome img
  sed -i 'index.theme' -e "s/Flat-Plat/Flat-Plat-light-laptop/g"
  cp -dr --no-preserve='ownership,mode' * "${pkgdir}"/usr/share/themes/Flat-Plat-light-laptop
}
