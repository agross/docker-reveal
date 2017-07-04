FROM ubuntu:15.04

RUN mkdir /myvol
RUN echo "hello world" > /myvol/greeting

VOLUME /myvol

# Equal to the above.
# VOLUME ["/myvol"]

# Use volumes from another container.
#
# 1. Create container with new volume.
# docker create -v /dbdata --name dbstore training/postgres /bin/true
#
# 2. Spin up containers using the volumes from the dbstore container.
# docker run -d --volumes-from dbstore --name db1 training/postgres
# docker run -d --volumes-from dbstore --name db2 training/postgres
#
# 3. Create a backup.
# docker run --rm --volumes-from dbstore -v $PWD:/backup ubuntu:15.04 tar cvf /backup/backup.tar /dbdata
#
# 4. Restore to a new volume.
# docker volume create dbstore2
# docker run --rm -v dbstore2:/dbdata -v $PWD:/backup ubuntu:15.04 bash -c 'cd /dbdata && tar xvf /backup/backup.tar --strip 1'
#
# Use volume drivers:
# https://docs.docker.com/engine/extend/legacy_plugins/#volume-plugins
