# Maintainer: Barnaby Gray <barnaby@pickle.me.uk>
pkgname=elasticwolf
pkgver=5.1.6
pkgrel=1
pkgdesc="GUI Application for managing Amazon Web Services (AWS) cloud resources"
arch=("any")
url="https://aws.amazon.com/developertools/9313598265692691"
license=('APL')
source=(https://s3-us-gov-west-1.amazonaws.com/elasticwolf/ElasticWolf-linux-$pkgver.zip)
depends=('xulrunner')
md5sums=('77ee7410b7aff985ec3fb13a9f2901af')

package() {
	mkdir "$pkgdir/opt"
	cp -r "$srcdir/ElasticWolf" "$pkgdir/opt/ElasticWolf"
	mkdir -p "$pkgdir/usr/bin"
	echo -e "#!/bin/sh\ncd /opt/ElasticWolf && ./ElasticWolf" > "$pkgdir/usr/bin/ElasticWolf"
	chmod +x "$pkgdir/usr/bin/ElasticWolf"
}
