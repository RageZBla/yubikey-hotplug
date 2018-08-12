pkgname=yubikey-hotplug
pkgver=1
pkgrel=1
pkgdesc="udev hotplug event for Yubikey devices"
arch=('any')
url="https://github.com/fuhry/yubikey-hotplug"
license=('MIT')
depends=('bash' 'yubikey-manager' 'grep' 'awk' 'xautolock')
source=('yubikey-hotplug' '95-yubikey-hotplug.rules')
install='yubikey-hotplug.install'

package() {
  install -d -m0755 "${pkgdir}/etc/udev/rules.d"
  install -m0644 "${srcdir}/95-yubikey-hotplug.rules" "${pkgdir}/etc/udev/rules.d/"
  install -d -m0755 "${pkgdir}/usr/bin"
  install -m0755 "${srcdir}/yubikey-hotplug" "${pkgdir}/usr/bin/"
}
