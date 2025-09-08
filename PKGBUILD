pkgname=python-sphinx-hawkmoth
pkgver=0.21.0
pkgrel=1
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
sha256sums=(e18571ee6aac1e5e87e60681505d853ea52c804fac6b66d5bc370269a81743ee)

build() {
    cd hawkmoth-${pkgver}

    python3 -m build --wheel --no-isolation
}

package() {
    cd hawkmoth-${pkgver}

    python3 -m installer -d ${pkgdir} dist/*.whl
}
