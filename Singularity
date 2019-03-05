Bootstrap: library
From: ubuntu:16.04

%files
   pathway-tools-22.5-linux-64-tier1-install /tmp

%environment
    export PATH="$PATH:/programs/pathway-tools:"

%post
     apt-get -y update && \
     apt-get install -y \
     curl \
     csh \
     ncbi-blast+ \
     libxm4 \
     iputils-ping \
     gnome-terminal;\
     mkdir programs;\
     mkdir -p /home/your/external/folder/ptools;\
     chmod u+x /tmp/pathway-tools-22.5-linux-64-tier1-install;\
     ./tmp/pathway-tools-22.5-linux-64-tier1-install --InstallDir /programs/pathway-tools --PTOOLS_LOCAL_PATH /home/your/external/folder/ptools --InstallDesktopShortcuts 0 --mode unattended;\
     mkdir -p /opt/ptools;\
     cp -r /home/your/external/folder/ptools  /opt/ptools;\
     rm /tmp/pathway-tools-22.5-linux-64-tier1-install;\
     curl https://bootstrap.pypa.io/get-pip.py | python3;\
     pip install mpwt