Getting the patches
===================

>> Get Contiki (if you havn't)
clone git://contiki.git.sourceforge.net/gitroot/contiki/contiki

>> Get the patches
git init patches
cd patches
git remote add origin -t patches git://i4git.informatik.uni-erlangen.de/contiki.git
git pull 
cd ..


Using Quilt
===========
>> Apply the patches
quilt push -a


Using stgit
===========
>> Init stgit
stg init

>> import patches 
stg import -s patches/series

>> Get and apply new patches
cd patches
git pull
cd ..
stg sync -s patches/series

