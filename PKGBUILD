# Contributor: matthiaskrgr <matthiaskrgr _strange_curverd_character_ freedroid D0T org>

pkgname=gource-gravatar-getter
pkgver=1.0
pkgrel=2
pkgdesc="gets gravtar avatars to be used by 'gource' for git repositories"
license=('unknown')
arch=('any')
url="http://code.google.com/p/gource/wiki/GravatarExample"
depends=('perl' 'gource' 'git')
source=('script.pl'
        'print-hint.patch')
sha1sums=('38a57cc55feae9e1bc0d355d1d25a55d7b032397'
          '1b55f2d9edaec04fdef7f6bebb9b6fc149faf737')

build() {
	patch $srcdir/script.pl print-hint.patch --follow-symlinks
}

package() {
	cd ${srcdir}
	install -Dm 755 script.pl ${pkgdir}/usr/bin/gource-gravatar-getter
}
