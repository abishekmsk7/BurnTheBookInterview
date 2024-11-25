This is a read me file

Burn The Book Interview: Local Setup Guide
This guide provides instructions for setting up and running the project locally using Docker and DDEV.

Prerequisites
Install Docker
Ensure you have Docker installed on your system. You can use any Docker environment of your choice, such as Orbstack or Lima.
Refer to the installation guide here: Docker Installation Guide.
Install DDEV
Install DDEV, a Docker-based local development tool.
The installation guide is available here: DDEV Installation Guide.

Setup Instructions
1. Clone the Repository
Clone the project to your local machine using the following command:

git clone https://github.com/abishekmsk7/BurnTheBookInterview.git

After cloning, the folder BurnTheBook will contain the complete Craft CMS site named testsite, along with all required files and a database backup.

2. Configure the Project
Copy the testsite folder from the cloned repository to your local machine.
Open a terminal/command prompt and navigate to the testsite directory:


3. Set Up the DDEV Environment
Configure the DDEV project:

ddev config --project-type=craftcms


Start the project and install dependencies:

ddev start
ddev composer install



4. Import the Database and Launch the Site
Import the provided database backup:

ddev import-db --file=/path/to/db.sql.gz

Replace /path/to/db.sql.gz with the actual path to the database backup file.

Open the site in your browser:

ddev launch
