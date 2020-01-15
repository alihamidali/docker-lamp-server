# docker-LAMP

*Directory Structure*
    
    .
    ├── apache                            # apache config folder
    │   ├── 000-default.conf              # vhost file
    │   └── wait-for.sh                   # scripts for waiting for other containers to be ready
    ├── app                               # application folder
    │   ├── Dockerfile                    # webserver container
    |   └── ...                           # project files
    ├── mysql                             # mysql config folder
    │   ├── Dockerfile                    # mysql container
    │   └── dump.sql                      # place your SQL DDL and SQL DML here
    ├── docker-compose.yml                # docker-compose up
    └── README.md
    
