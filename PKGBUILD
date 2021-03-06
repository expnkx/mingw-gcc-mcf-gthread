# Maintainer: Alexey Pavlov <alexpux@gmail.com>
# Maintainer: Ray Donnelly <mingw.android@gmail.com>
# Contributor: Alexey Borzenkov <snaury@gmail.com>
# Contributor: Renato Silva <br.renatosilva@gmail.com>
# Contributor: Liu Hao <lh_mouse@126.com>
# Contributor: Tim Stahlhut <stahta01@gmail.com>
# Contributor: cqwrteur <euloanty@live.com>

_realname=gcc
_sourcedir=${_realname}-git
pkgbase=mingw-w64-${_realname}-mcf
pkgname=("${MINGW_PACKAGE_PREFIX}-${_realname}-mcf"
         "${MINGW_PACKAGE_PREFIX}-${_realname}-mcf-libs")
pkgver=10.0.0.d20191027.c12.gfb8972269b4
pkgrel=1
pkgdesc="GNU Compiler Collection (C,C++,OpenMP) for MinGW-w64 with MCF thread model"
depends=("${MINGW_PACKAGE_PREFIX}-binutils"
         "${MINGW_PACKAGE_PREFIX}-crt"
         "${MINGW_PACKAGE_PREFIX}-headers"
         "${MINGW_PACKAGE_PREFIX}-isl"
         "${MINGW_PACKAGE_PREFIX}-libiconv"
         "${MINGW_PACKAGE_PREFIX}-mpc"
         "${MINGW_PACKAGE_PREFIX}-windows-default-manifest"
         "${MINGW_PACKAGE_PREFIX}-winpthreads"
         "${MINGW_PACKAGE_PREFIX}-zlib"
         "${MINGW_PACKAGE_PREFIX}-mcfgthread-libs")
arch=('any')
url="https://gcc.gnu.org"
license=('GPL' 'LGPL' 'FDL' 'custom')
groups=("${MINGW_PACKAGE_PREFIX}-toolchain")
makedepends=("${MINGW_PACKAGE_PREFIX}-${_realname}"
             "${MINGW_PACKAGE_PREFIX}-binutils"
             "${MINGW_PACKAGE_PREFIX}-crt"
             "${MINGW_PACKAGE_PREFIX}-headers"
             "${MINGW_PACKAGE_PREFIX}-gmp"
             "${MINGW_PACKAGE_PREFIX}-isl"
             "${MINGW_PACKAGE_PREFIX}-libiconv"
             "${MINGW_PACKAGE_PREFIX}-mpc"
             "${MINGW_PACKAGE_PREFIX}-mpfr"
             "${MINGW_PACKAGE_PREFIX}-windows-default-manifest"
             "${MINGW_PACKAGE_PREFIX}-winpthreads"
             "${MINGW_PACKAGE_PREFIX}-zlib"
             "${MINGW_PACKAGE_PREFIX}-mcfgthread")
#checkdepends=('dejagnu')
optdepends=()
options=('staticlibs' '!emptydirs') # '!strip' 'debug'

#_branch=gcc-7-branch
_branch=master
_realpkgver="$(git archive --remote=git://gcc.gnu.org/git/gcc.git refs/heads/${_branch}:gcc/ BASE-VER | tar -xO)"

# git+https://gcc.gnu.org/git/gcc.git#branch=${_branch}
source=(${_sourcedir}::"git://gcc.gnu.org/git/gcc.git#branch=${_branch}"
        "0002-Relocate-libintl.patch"
        "0003-Windows-Follow-Posix-dir-exists-semantics-more-close.patch"
        "0004-Windows-Use-not-in-progpath-and-leave-case-as-is.patch"
        "0005-Windows-Don-t-ignore-native-system-header-dir.patch"
        "0006-Windows-New-feature-to-allow-overriding.patch"
        "0007-Build-EXTRA_GNATTOOLS-for-Ada.patch"
        "0008-Prettify-linking-no-undefined.patch"
        "0010-Fix-using-large-PCH.patch"
        "0011-Enable-shared-gnat-implib.patch"
        "0014-clone_function_name_1-Retain-any-stdcall-suffix.patch"
        "0014-gcc-9-branch-clone_function_name_1-Retain-any-stdcall-suffix.patch"
        "0016-gcc-7-branch-disable-weak-refs-in-libstdc++.patch"
        "0017-gcc-7-branch-Enable-std-experimental-filesystem.patch"
        "0018-gcc-7-branch-Enable-a-native-GCC-to-color-diagnostic-messages-sen.patch"
        "0019-gcc-8-branch-Backport-patches-for-std-filesystem-from-master.patch"
        "0020-gcc-10-devel-master-Windows-Don-t-ignore-native-syst.patch"
        "0021-gcc-10-devel-master-Fix-using-large-PCH.patch"
        "0022-We-no-longer-rely-on-BUFSIZ-macro-any-more-since-BUF.patch"
        "9000-gcc-7-branch-Added-mcf-thread-model-support-from-mcfgthread.patch"
        "9000-gcc-8-branch-Added-mcf-thread-model-support-from-mcfgthread.patch"
        "9000-gcc-9-branch-Added-mcf-thread-model-support-from-mcfgthread.patch"
        "9000-master-Added-mcf-thread-model-support-from-mcfgthread.patch")
sha256sums=('SKIP'
            '83e9c6f76f728ae3e2f2eabb588b0d6cea7a3eda03cd5e77aed9d613143b7348'
            '6033acda690786397059536787a6577e1a9f2b39f8a66276821917066094f43c'
            '388f423a67e4be6f547ca7e340ff8ee4c78b1ed83f3fd698daa409e309911807'
            '86fc77d5a6c137a9aca65ad6ba56653fb41b05636b763ce2c0b0b14d617c9de4'
            'd1e10cd2ef5594c34acead334bb93af500e00699ba673edc8916da22a572677d'
            '3629446c0039d9061cfedcb6d7a7589279588bb4601c7ce233546d357bd4be34'
            'ec6800816632234afc35ce40542a6aab3ee76e8514a7d0cb4171fd874353ecd7'
            '0decbbebda7ceac91da5d3dec9b7330f406a4358fa150560f08ff6f54739035f'
            '8faff8e503a617f283270f411399a8bcacda3ab62b4072dedf117e108af4844a'
            '60a58ed41389691a68ef4b7d47a0328df4d28d26e6c680a6b06b31191481ca65'
            '2321c7dce29a600477e481d16d847f05dc8c6d6461ee1eba7814c5bf62c2ef95'
            'c1e271c166de0062092cb61d50977c0e61d75b0ae6fb086cb8bb4da2b3fd18d7'
            'b1c3c20bf501cebbcb02b4a50f117a4f90eb4fb79eac7aa99c85e2c54c106790'
            '33392651e17b81609718873ff32606deee5f3fc5176c197bb96eedc3dada8912'
            'bf83cbc79de4c86f02664c8a624e26b12f570e3c31116fc7c46ecf655696f9a6'
            'e793c491f83e460e50df5b72672518649fbfe5088bddbe5163cf7aeb7d28411a'
            '98134921a38554b53d65fb97d698465d86728a340ccfcc8ed6ca90691a8fb01e'
            '22b23fe476273f77e25cdf8e2563e3d5a20c6d2b8da855809e629d124fa952c4'
            'bd2eb0241ff406cfc40c864cbc2229666dca7341199ffbfebc11fef8c4ed24fe'
            'f22282601f9d55b11354153dcfc1b3465a10949e0104a50145a7cb2d131f2ae5'
            'f22282601f9d55b11354153dcfc1b3465a10949e0104a50145a7cb2d131f2ae5'
            '66038b785a6f56b2fb3442adc7b5be1af62e9a11ad9fe142104d6ee9760aeee5')

_threads="mcf"
_git_base_commit=
_gcc_version=
_gcc_date=

pkgver() {
  cd ${srcdir}/${_sourcedir}
  _gcc_version=$(head -n 34 gcc/BASE-VER | sed -e 's/.* //' | tr -d '"\n')
  _gcc_date=$(head -n 34 gcc/DATESTAMP | sed -e 's/.* //' | tr -d '"\n')
  printf "%s.d%s.c%s.g%s" "$_gcc_version" "$_gcc_date" $(git rev-list --count ${_git_base_commit}..HEAD) $(git rev-parse --short ${_git_base_commit})
}

prepare() {
  cd ${srcdir}/${_sourcedir}
  _git_base_commit=$(git rev-parse HEAD)
  GIT_AM="git am --committer-date-is-author-date"
  ${GIT_AM} ${srcdir}/0002-Relocate-libintl.patch
  ${GIT_AM} ${srcdir}/0003-Windows-Follow-Posix-dir-exists-semantics-more-close.patch
  ${GIT_AM} ${srcdir}/0004-Windows-Use-not-in-progpath-and-leave-case-as-is.patch
  if [ "${_branch}" == "gcc-10-branch" ] || [ "${_branch}" == "master" ]; then
    ${GIT_AM} ${srcdir}/0020-gcc-10-devel-master-Windows-Don-t-ignore-native-syst.patch
  else
    ${GIT_AM} ${srcdir}/0005-Windows-Don-t-ignore-native-system-header-dir.patch
  fi
  ${GIT_AM} ${srcdir}/0006-Windows-New-feature-to-allow-overriding.patch
  ${GIT_AM} ${srcdir}/0007-Build-EXTRA_GNATTOOLS-for-Ada.patch
  ${GIT_AM} ${srcdir}/0008-Prettify-linking-no-undefined.patch
  if [ "${_branch}" == "gcc-10-branch" ] || [ "${_branch}" == "master" ]; then
    ${GIT_AM} ${srcdir}/0021-gcc-10-devel-master-Fix-using-large-PCH.patch
    ${GIT_AM} ${srcdir}/0022-We-no-longer-rely-on-BUFSIZ-macro-any-more-since-BUF.patch
  else
    ${GIT_AM} ${srcdir}/0010-Fix-using-large-PCH.patch
  fi
  ${GIT_AM} ${srcdir}/0011-Enable-shared-gnat-implib.patch
  if [ "${_branch}" == "gcc-9-branch" ] || [ "${_branch}" == "gcc-10-branch" ] || [ "${_branch}" == "master" ]; then
    ${GIT_AM} ${srcdir}/0014-gcc-9-branch-clone_function_name_1-Retain-any-stdcall-suffix.patch
  else
    ${GIT_AM} ${srcdir}/0014-clone_function_name_1-Retain-any-stdcall-suffix.patch
  fi
  if [ "${_branch}" == "gcc-7-branch" ]; then
    ${GIT_AM} ${srcdir}/0016-gcc-7-branch-disable-weak-refs-in-libstdc++.patch
    ${GIT_AM} ${srcdir}/0017-gcc-7-branch-Enable-std-experimental-filesystem.patch
    ${GIT_AM} ${srcdir}/0018-gcc-7-branch-Enable-a-native-GCC-to-color-diagnostic-messages-sen.patch
  fi
  if [ "${_branch}" == "gcc-8-branch" ]; then
    ${GIT_AM} ${srcdir}/0019-gcc-8-branch-Backport-patches-for-std-filesystem-from-master.patch
  fi
  ${GIT_AM} ${srcdir}/9000-${_branch}-Added-mcf-thread-model-support-from-mcfgthread.patch

  # do not expect $prefix/mingw symlink - this should be superceded by
  # 0004-Windows-Don-t-ignore-native-system-header-dir.patch .. but isn't!
  sed -i 's/${prefix}\/mingw\//${prefix}\//g' configure

  # change hardcoded /mingw prefix to the real prefix .. isn't this rubbish?
  # it might work at build time and could be important there but beyond that?!
  local MINGW_NATIVE_PREFIX=$(cygpath -am ${MINGW_PREFIX}/${MINGW_CHOST})
  sed -i "s#\\/mingw\\/#${MINGW_NATIVE_PREFIX//\//\\/}\\/#g" gcc/config/i386/mingw32.h
}

build() {
  [[ -d ${srcdir}/build-${MINGW_CHOST} ]] && rm -rf ${srcdir}/build-${MINGW_CHOST}
  mkdir -p ${srcdir}/build-${MINGW_CHOST} && cd ${srcdir}/build-${MINGW_CHOST}

  case "${CARCH}" in
    i686)
      LDFLAGS+=" -Wl,--large-address-aware"
      local _arch=i686
      local _conf="--enable-sjlj-exceptions"    # "--disable-sjlj-exceptions --with-dwarf2"
    ;;

    x86_64)
      local _arch=x86-64
      local _conf=""
    ;;
  esac

  ../${_sourcedir}/configure \
    --prefix=${MINGW_PREFIX} \
    --with-local-prefix=${MINGW_PREFIX}/local \
    --build=${MINGW_CHOST} \
    --host=${MINGW_CHOST} \
    --target=${MINGW_CHOST} \
    --with-native-system-header-dir=${MINGW_PREFIX}/${MINGW_CHOST}/include \
    --libexecdir=${MINGW_PREFIX}/lib \
    --with-arch=${_arch} \
    --with-tune=nocona \
    --enable-languages=c,lto,c++ \
    --enable-shared --enable-static \
    --enable-threads=${_threads} \
    --enable-graphite \
    --enable-fully-dynamic-string \
    --enable-libstdcxx-time=yes \
    --disable-libstdcxx-pch \
    --disable-libstdcxx-debug \
    --enable-libstdcxx-filesystem-ts=yes \
    --disable-isl-version-check \
    --enable-lto \
    --enable-libgomp \
    --disable-multilib \
    --enable-checking=release \
    --disable-rpath \
    --disable-win32-registry \
    --enable-nls \
    --disable-werror \
    --disable-symvers \
    --with-libiconv \
    --with-system-zlib \
    --with-{gmp,mpfr,mpc,isl}=${MINGW_PREFIX} \
    --with-pkgversion="${_branch} HEAD with MCF thread model, built by cqwrteur." \
    --with-bugurl="https://gcc-mcf.lhmouse.com/" \
    --with-gnu-as --with-gnu-ld \
    --disable-tls \
    --enable-plugin  \
    --disable-bootstrap  \
    ${_conf}
    #--enable-libitm
    #--enable-objc-gc
    #--with-gxx-include-dir=${MINGW_PREFIX}/include/c++/${_realpkgver} \
    #--enable-version-specific-runtime-libs \
    #--enable-libatomic \

  # While we're debugging -fopenmp problems at least.
  # .. we may as well not strip anything.
  if check_option "strip" "n"; then
    sed -i 's,^STRIP = .*$,STRIP = true,g'                   Makefile
    sed -i 's,^STRIP_FOR_TARGET=.*$,STRIP_FOR_TARGET=true,g' Makefile
  fi

  make all

  rm -rf "${srcdir}${MINGW_PREFIX}"
  make -j1 DESTDIR=${srcdir} install
}

package_mingw-w64-gcc-mcf() {
  pkgdesc="GNU Compiler Collection (C,C++,OpenMP) for MinGW-w64 with MCF thread model (devel)"
  depends=("${MINGW_PACKAGE_PREFIX}-binutils"
           "${MINGW_PACKAGE_PREFIX}-crt"
           "${MINGW_PACKAGE_PREFIX}-headers"
           "${MINGW_PACKAGE_PREFIX}-isl"
           "${MINGW_PACKAGE_PREFIX}-libiconv"
           "${MINGW_PACKAGE_PREFIX}-mpc"
           "${MINGW_PACKAGE_PREFIX}-windows-default-manifest"
           "${MINGW_PACKAGE_PREFIX}-winpthreads"
           "${MINGW_PACKAGE_PREFIX}-zlib"
           "${MINGW_PACKAGE_PREFIX}-${_realname}"-libs)
  provides=("${MINGW_PACKAGE_PREFIX}-${_realname}")
  conflicts=("${MINGW_PACKAGE_PREFIX}-${_realname}"
             "${MINGW_PACKAGE_PREFIX}-${_realname}-git")

  mkdir -p "${pkgdir}${MINGW_PREFIX}"
  cd "${srcdir}${MINGW_PREFIX}"
  _files_cp="$(find bin -type f -and -not -name "*.dll")"
  [[ -z "${_files_cp}" ]] || cp --parents -r ${_files_cp} --target-directory="${pkgdir}${MINGW_PREFIX}"
  cp --parents -r include   --target-directory="${pkgdir}${MINGW_PREFIX}"
  cp --parents -r lib       --target-directory="${pkgdir}${MINGW_PREFIX}"
}
package_mingw-w64-gcc-mcf-libs() {
  pkgdesc="GNU Compiler Collection (C,C++,OpenMP) for MinGW-w64 with MCF thread model (libs)"
  depends=("${MINGW_PACKAGE_PREFIX}-gmp"
           "${MINGW_PACKAGE_PREFIX}-libwinpthread")
  provides=("${MINGW_PACKAGE_PREFIX}-${_realname}-libs")
  conflicts=("${MINGW_PACKAGE_PREFIX}-${_realname}-libs-git")
#             "${MINGW_PACKAGE_PREFIX}-${_realname}-libs"

  mkdir -p "${pkgdir}${MINGW_PREFIX}"
  cd "${srcdir}${MINGW_PREFIX}"
  _files_cp="$(find bin -type f -and -name "*.dll")"
  [[ -z "${_files_cp}" ]] || cp --parents -r ${_files_cp} --target-directory="${pkgdir}${MINGW_PREFIX}"
  cp --parents -r share     --target-directory="${pkgdir}${MINGW_PREFIX}"
}

# Wrappers for package functions

# 32-bit wrappers
package_mingw-w64-i686-gcc-mcf() {
  package_mingw-w64-gcc-mcf
}
package_mingw-w64-i686-gcc-mcf-libs() {
  package_mingw-w64-gcc-mcf-libs
}

# 64-bit wrappers
package_mingw-w64-x86_64-gcc-mcf() {
  package_mingw-w64-gcc-mcf
}
package_mingw-w64-x86_64-gcc-mcf-libs() {
  package_mingw-w64-gcc-mcf-libs
}
