# Local Manifests #
Just grab the manifest and sync to get device sources
### LineageOS R ###


# Grab Local Manifest
curl -o .repo/local_manifests/local_manifests.xml https://raw.githubusercontent.com/aetherAF/local_manifests/eleven/eleven.xml --create-dirs

# Sync
repo sync --current-branch --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$( nproc --all )
### LineageOS S ###

Required patches for IMS: https://gerrit.pixelexperience.org/q/topic:%22mediatek-ims%22+(status:open%20OR%20status:merged)


# Grab Local Manifest
curl -o .repo/local_manifests/local_manifests.xml https://raw.githubusercontent.com/aetherAF/local_manifests/master/twelve.xml --create-dirs

# Sync
repo sync --current-branch --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$( nproc --all )
