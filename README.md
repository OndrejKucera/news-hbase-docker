# docker-hbase

Apache HBase docker image based on alpine (will be change for debian)

https://www.tutorialspoint.com/hbase/hbase_overview.htm

## Small setup
  ```
  # network 
  docker network create vnet

  # hadoop+hbase startup
  docker-compose up -d

  # tail logs for a while
  docker-compose logs -f

  # check ps
  docker-compose ps

  # check stats
  docker ps --format {{.Names}} | xargs docker stats

  # hbase shell
  docker exec -it -u hbase regionserver-1 hbase shell

  # hadoop/hbase shutdown  
  docker-compose stop

  # cleanup container
  docker-compose rm -v
  ```
