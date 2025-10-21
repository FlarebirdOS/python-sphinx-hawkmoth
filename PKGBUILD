pkgname=python-sphinx-hawkmoth
pkgver=0.22.0
pkgrel=2
pkgdesc="Sphinx autodoc C extension"
arch=('x86_64')
url="https://github.com/jnikula/hawkmoth"
license=('BSD-2-Clause')
depends=(
    'clang'
    'python'
    'python-docutils'
    'python-sphinx'
)
makedepends=(
    'python-build'
    'python-hatchling'
    'python-installer'
    'python-setuptools'
    'python-wheel'
)
source=(https://github.com/jnikula/hawkmoth/archive/v${pkgver}/hawkmoth-${pkgver}.tar.gz)
sha256sums=(549328f0555a81280dc47d6910ce240fd1808702cb6cd88a37cf5c86f572ffbc)

build() {
    cd hawkmoth-${pkgver}

    python3 -m build --wheel --no-isolation
}

package() {
    cd hawkmoth-${pkgver}

    python3 -m installer -d ${pkgdir} dist/*.whl
}
