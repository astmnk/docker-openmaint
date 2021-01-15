### Deploy by docker run

OpenMAINT version 2.1 with CMDBUILD version 3.3

**openMAINT with demo database**  
```bash
docker run --name openmaint_db -p 5432:5432 -d postgis
docker run --name openmaint_app --restart unless-stopped -e CMDBUILD_DUMP="demo.dump.xz" --link openmaint_db  -p 8090:8080 -d openmaint
```  

or use docker-compose:
```bash
docker-compose up file/location
```

#### CMDBUILD_DUMP values
* demo.dump.xz
* empty.dump.xz
