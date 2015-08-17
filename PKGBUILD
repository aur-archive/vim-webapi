# Maintainer: Matt Monaco <cx monaco matt>

pkgname=vim-webapi
pkgver=0.3.2.g6d577e4
pkgrel=1
pkgdesc="Vim Interface to Web API"
arch=(any)
url=https://github.com/mattn/webapi-vim
license=(UNKNOWN)
depends=(vim curl)
makedepends=(git)
source=(git://github.com/mattn/webapi-vim.git)
md5sums=(SKIP)
install=vim-helptags.install

pkgver()
{
	cd "$srcdir"/webapi-vim
	local ver=$(git describe --tags )
	printf "%s" "${ver//-/.}"
}

package()
{
	cd "$srcdir"/webapi-vim
	for f in autoload/webapi/* doc/* example/*; do
		install -D "$f" "$pkgdir"/usr/share/vim/vimfiles/"$f"
	done
}
