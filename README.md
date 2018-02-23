It is a docker boilerplate used for running applications with PHP7 and Oracle 10 InstantClient.

Instructions:

1. Install Docker
2. Install Symfony 2/3 standard edition using composer **composer create-project symfony/framework-standard-edition my_project_name**
3. Clone this repository to your newly created application
4. Run docker-compose up -d
5. Enter localhost:8080 to your browser and start developing!

NOTE: **oci8** driver must be used for making a successfull Oracle InstantClient connection

NOTE: Add IP 172.17.0.1 to your app_dev.php in order to dev environment to work.