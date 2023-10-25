We have created an application that we can store node modules. A user can interact with our system through RESTful API requests and responses. We also have a database that we can upload and download such packages using a previously implemented rating application. Our system will screen packages and test them to make sure that they are trustworthy enough to be used in enterprise-level projects. The project is built to be scalable, fast, efficient, and robust.

const creators = [`Ishaan Jain`, `Kahaan Patel`, `Kevin Mi`, `Jamie Laster`];
See https://app.swaggerhub.com/apis/JAIN343_1/ece-461_spring_2023_project_2/2.0.0 for information about our project and access the openAPI spec.

Security requirements.

Confidentiality Only authorized users can access the packages and data. Only authorized users can access the history of packages, when they were updated, downloaded, created, or rated. Only individuals authorized to access the GCP platform can see the users on the database

Integrity Only authorized users can update, create, or delete packages. Only users with admin-level authorizations can create or delete users.

Availability An authorization key lasts only for 1000 requests and 10 hours, mitigating DDOS attacks if a malicious party gets access to a key. Only users with admin level access can reset the whole registry.

Authentication Every request (except the authentication request) is authorized using their authorization key. Only hashes of the passwords are stored in the database to protect the server in case of data leaks. An authorization key lasts only for 1000 requests and 10 hours if the key is leaked

Authorization There are different levels of authorization and only admin-level access allows a user to create or delete new users

Nonrepudiation Package creation, rating, deletion, and update are logged in the database.


