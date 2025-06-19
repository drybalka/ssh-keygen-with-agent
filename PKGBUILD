pkgname=ssh-keygen-with-agent
pkgver=1.0.0
pkgrel=1
pkgdesc="A wrapper for ssh-keygen that automatically adds SSH keys to the agent when signing Git commits"
arch=('any')
url="https://github.com/drybalka/ssh-keygen-with-agent"
license=('MIT')
depends=('openssh')

package() {
    cd ..
    install -Dm755 "ssh-keygen-with-agent" "$pkgdir/usr/bin/ssh-keygen-with-agent"
    install -Dm644 "LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
    install -Dm644 "README.md" "$pkgdir/usr/share/doc/$pkgname/README.md"
}
