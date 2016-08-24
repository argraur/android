## How to build Bliss
<img src="https://raw.github.com/TeamBliss-LP/android/lp5.1/bliss-logo.png">

Getting Started 
---------------

To get started with Android/BlissPop, you'll need to get
familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

To initialize your local repository using the BlissPop trees, use this command:


    repo init -u https://github.com/argraur/android.git -b bliss-5.1

Then to sync up:

    repo sync -j#

This(j#) depends on number of cpu cores - use just "repo sync" if you are unsure.

Next you need to clone N3N repos, use this command:


    git clone https://github.com/argraur/android_.repo_local_manifests_n3n.git -b bliss-lp5.1 .repo/local_manifests
    

Then to sync it:

    repo sync -j# --force-sync

To build for your device.

. build/envsetup.sh

lunch `bliss_hllte-userdebug or bliss_hl3g-userdebug or bliss_hlltezt-userdebug`

brunch `bliss_hllte-userdebug or bliss_hl3g-userdebug or bliss_hlltezt-userdebug`
