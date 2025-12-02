- hosts slave-node
  become true
  tasks
    - name update ubuntu repo and cache
      apt
        update_cache yes
        cache_valid_time 360
 
    - name Install Java Version 17
      apt
        name openjdk-17-jdk
        state present
 
    - name Download Maven Packages
      get_url
        url httpsarchive.apache.orgdistmavenmaven-33.9.11binariesapache-maven-3.9.11-bin.tar.gz
        dest opt
 
    - name Extract Maven Packages
      unarchive
        src optapache-maven-3.9.11-bin.tar.gz
        dest opt
        remote_src yes