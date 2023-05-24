
# JOBs API


The JOBs API is a backend service that powers the JOBs web application. It provides the necessary endpoints and functionality for job listing aggregation, user authentication . This repository contains the source code and documentation for the JOBs API.

## Features

- Job listing aggregation from multiple sources.
- User authentication .
- CRUD operations for job listings.
- Job application management.


## Installation

To set up the JOBs API on your local machine, please follow these steps:

1. Clone this repository to your local machine using the following command:

   ```shell
   git clone https://github.com/usefsame7/JOBs.git
   ```

2. Navigate to the project directory:

   ```shell
   cd JOBs
   ```

3. Install the project dependencies using the package manager of your choice. Assuming you have Node.js and npm installed, run the following command:

   ```shell
   npm install
   ```

4. Create a `.env` file in the project root directory with the following environment variables:

   ```
   PORT=3000
   DATABASE_URL=<your_database_url>
   SECRET_KEY=<your_secret_key>
   ```

   Replace `<your_database_url>` with the URL of your MongoDB database and `<your_secret_key>` with a secret key of your choice.

5. Start the API server by running the following command:

   ```shell
   npm start
   ```

   The API will be running at `http://localhost:3000`.

## API Endpoints

The JOBs API provides the following endpoints:

- `GET /api/applications` - Retrieving all attempts to apply for the job.
- `POST /api/apply` - Create a new apply for the job.
- `POST /api/register` - Register a new user account.
- `POST /api/login` - Log in to an existing user account.
- `GET /api/all-users` - Retrieve all the registered users.



## Contributing

Contributions to the JOBs API are welcome! If you would like to contribute, please follow these steps:

1. Fork the repository on GitHub.
2. Create a new branch for your feature or bug fix:
   ```shell
   git checkout -b my-new-feature
   ```
3. Make your changes and commit them with descriptive commit messages:
   ```shell
   git commit -am 'Add some feature'
   ```
4. Push your changes to your forked repository:
   ```shell
   git push origin my-new-feature
   ```
5. Open a pull request on the main repository, explaining your changes and why they should be merged.



## Request/Response Ex
Apply for the job:
```http
POST /api/apply
```
 - (the applyer must upload his image befor inserting the information) . request body : 
```json
{ 
 "fullName":"james kattil boar", 
 "email":"james22@gmail.com", 
 "address":"London,bla bla", 
 "dateOfBirth":"1998-02-13" 
}
```

response object:
```json
{
 "_id":"sd9f9sdf9j9jj8j823482j", 
 "fullName":"james kattil boar", 
 "email":"james22@gmail.com", 
 "address":"London,bla bla", 
 "dateOfBirth":"1998-02-13" 
 "userImagePath": "uploaded image path" => (will be extracted from the 'req.file' object)
}
```

## Contact

If you have any questions or suggestions regarding this project, please feel free to contact the project owner:

- Name: Youssef Sameh Elsisy
- Email: yousameh2006@gmail.com
 
 
 
 
 **Regards.Y**
 
 
 
 
 