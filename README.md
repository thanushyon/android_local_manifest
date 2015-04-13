Local manifest addon for JGCAAP Cyanogenmod 12.1

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

Make a build directory:

	mkdir cm (or whatever name you choose)
	cd cm (or the name  you chose)
	mkdir .repo/local_manifests

To initialize your local repository using the Cyanogemod manifest, use commands like these:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-12.1
    
    curl -L -o .repo/local_manifests/roomservice.xml -O -L https://raw.github.com/jgcaap/android_local_manifest/cm-12.1/roomservice.xml

    	( or Download: https://github.com/jgcaap/android_local_manifest/blob/cm-12.1/roomservice.xml
		and place it in ~/cm/.repo/local_manifests/roomservice.xml (or ~/'name you chose'/.repo)

Then to sync up:

    repo sync

    **NOTE: If you can have multiple manifests but if they have the same projects but different branches you
    should go to (your android root)/.repo/local_manifests and rename the one with conflicting projects to .bak**
