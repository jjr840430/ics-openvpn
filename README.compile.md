# How to build

CURR_DIR=$(pwd)

git clone git@github.com:jjr840430/ics-openvpn.git
cd ics-openvpn
git checkout v0.7.18_xor_patch
git submodule update --init --recursive
cd ${CURR_DIR}/main/src/main/cpp/openvpn
patch -p1 < ${CURR_DIR}/patches/openvpn-xor-patch.diff
