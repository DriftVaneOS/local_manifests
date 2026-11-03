# DriftVaneOS local manifests

    repo init -u https://github.com/LineageOS/android.git -b lineage-24.0 --git-lfs
    git clone https://github.com/DriftVaneOS/local_manifests .repo/local_manifests
    repo sync -c -j8

Then add your device tree, kernel and vendor blobs (TheMuppets) for your
device, and run `breakfast <device>` and `m bacon`.

Build env (put in ~/.bashrc):

    export CC_WRAPPER=/usr/bin/ccache SKIP_ABI_CHECKS=true USE_THINLTO_CACHE=true BUILD_USERNAME=android-build

Make your OWN signing keys (vendor/lineage-priv/keys). Never use someone else's.
Never flash firmware older than your phone's bootloader.
