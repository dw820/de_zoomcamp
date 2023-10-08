## Docker & SQL
1. Install Docker
2. run `docker run hello-world` to test if docker is installed correctly. You should see `Hello from Docker!` & a new hello-world image was downloaded
3. Create the `Dockerfile` for the Docker Image. The image is for python to run (the pipeline)
4. Use `docker-compose.yaml` to create multiple images for the PostgreSQL database with pgAdmin. Run `docker-compose up` to start. The volume will be mounted at `./ny_taxi_postgres_data` folder, so the first time when creating the image, we will see more files been added this folder.
5. Open pgAdmin on `http://localhost:8080/` 
6. Connect with the database server: 
   
   - Host name: pgdatabase
   - Username: root
   - Password: root

7. 



## GCP
# Connect to GCP locally through SSH
1. Run `ssh-keygen -t rsa -f ~/.ssh/ssh-key-1 -C weitu -b 2048` to generate public/private key
2. Add ssh key to the instance
3. Run `ssh -i ~/.ssh/ssh-key-1 weitu@104.154.142.8` to connect to the intance