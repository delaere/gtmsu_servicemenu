# Maintainer: pdq <pdq@localhost>
pkgname=gtmsu_servicemenu
pkgver=0.0.1
pkgrel=1
pkgdesc="KDE servicemenu for tmsu. (http://tmsu.org/) - GIT Version"
arch=(any)
url="https://github.com/idk/gtmsu_servicemenu.git"
license=('GPL')
depends=('tmsu' 'kdebase-dolphin')
makedepends=('git')

_gitroot="git://github.com/idk/gtmsu_servicemenu.git"
_gitname="gtmsu_servicemenu"

#install=$pkgname.install

build() {
	cd "$srcdir"
	msg "Connecting to GIT server...."

	if [ -d $_gitname ] ; then
		cd $_gitname && git pull origin
		msg "The local files are updated."
	else
		git clone $_gitroot $_gitname
	fi

	msg "GIT checkout done or server timeout"
	msg "Starting make..."

	rm -rf "$srcdir/$_gitname-build"
	git clone "$srcdir/$_gitname" "$srcdir/$_gitname-build"
	cd "$srcdir/$_gitname-build"

	# Create pkgdir folders
	install -d $pkgdir/usr/share/kde4/services/ServiceMenus

	# Install
	cp -r gtmsu_tag.desktop $pkgdir/usr/share/kde4/services/ServiceMenus/gtmsu_tag.desktop
}
