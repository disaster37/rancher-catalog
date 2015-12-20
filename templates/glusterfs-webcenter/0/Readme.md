# How to use

This service provide 4 containers:
  * 2 dedicated for the storage
  * 2 dedicated to run Glusterfs and manage the cluster


When it's start for the first time, it create the new cluster and then create the volume that you need.
If you scale this, it extend the cluster but doesn't touch to the existing volume. If you should extend them, you must enter in container and lauch the right glusterfs command.


# Note

The current service not support the following enhance:
  * The upgrade service doesn't work. When rancher upgrade, it create new container and so the cluster setting is lost. When it recreate the cluster, the creation of volume failed because folder already exist.
  * To extends the volumes, you must run some manual command.
  * Remove container (minus scale) is not supported. 
