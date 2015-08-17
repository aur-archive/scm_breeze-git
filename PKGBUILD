# $Id: pkgbuild-mode.el,v 1.23 2007/10/20 16:02:14 juergen Exp $
# Maintainer: Artyom Olshevskiy <siasiamail@gmail.com>
pkgname=scm_breeze-git  
pkgver=20120426
pkgrel=1 
pkgdesc="Streamline your SCM workflow"
url="http://github.com/ndbroadbent/scm_breeze"
arch=('i686' 'x86_64')
license=('MIT')
depends=('ruby')
makedepends=('git')
conflicts=()
replaces=()
backup=()
install=scm_breeze-git.install
#source=($pkgname-$pkgver.tar.gz)
md5sums=()
_gitroot='http://github.com/ndbroadbent/scm_breeze.git'
_gitname='scm_breeze'
build() {
	cd ${srcdir}
	if [ -d ${_gitname} ]; then
		cd ${_gitname} && git pull origin
		cd ..
	else
		git clone ${_gitroot}
	fi
	cd ${_gitname}
	mkdir -p ${pkgdir}/usr/share/scm_breeze
	git archive HEAD | tar -x -C ${pkgdir}/usr/share/scm_breeze
}
