 PROJECT 4 - STEP 10

 MEAN STACK IMPLEMENTATION

 MEAN STACK DEPLOYMENT TO UBUNTU IN AWS.

* STEP 0
PREPARING PREREQUISITES

The first step to take in order to complete this project is to launch an AWS EC2 instance of t2.nano with ubuntu server 20.04 LTS (HVM)image.
- The task is to implement a simple book register web form using MEAN stack.

STEP 1: INSTALL NODE JS
- Node.js is a javascript runtime built on chrome's V8 JavaSript engine. Node.js is used in the project to set up the Express routes and AngularJS controllers
- To install Node.js, we will need to update and upgrade Ubuntu, then add certificates by coping and pasting the command given.
- We then go ahead to Install Nodejs by running the command "sudo apt install -y nodejs"

<img width="1440" alt="Screenshot 2022-11-11 at 11 13 33 PM" src="https://user-images.githubusercontent.com/115854902/201494495-ff19ab92-740b-4206-901b-df1559b783ba.png">

<img width="1440" alt="Screenshot 2022-11-11 at 11 16 16 PM" src="https://user-images.githubusercontent.com/115854902/201494624-504144ff-f57d-4d9b-ad3f-7a5cf08f1fdc.png">

<img width="1440" alt="Screenshot 2022-11-11 at 11 22 41 PM" src="https://user-images.githubusercontent.com/115854902/201494649-7f5e703b-3491-4b02-8199-f7e0ba3f2b9d.png">

STEP 2: INSTALL MONGODB
- MongoDB stores data in flexible, JSON- like documents.
- Before we go ahead to install MONGODB we need to add book records to MONGODB that contain book name, Isbn number, author, and number of pages by running the codes given on our terminal.
- The next step is to Install -y MongoDB, then start the server and then we go ahead to verify that the service is up and running.

<img width="1440" alt="Screenshot 2022-11-11 at 11 28 16 PM" src="https://user-images.githubusercontent.com/115854902/201526235-23f92b49-d774-48c9-9871-5b3467b59cb8.png">

- Next, we Install npm - Node package manager
<img width="1440" alt="Screenshot 2022-11-11 at 11 32 37 PM" src="https://user-images.githubusercontent.com/115854902/201526376-b2be0e9b-f84f-4ad0-b9c5-7f922e7301e7.png">

- We will also install body-parser package, this is important because it will help us process JSON files passed in request to the server.
- We will now create a folder named Books and in the books directory , we will initialize npm project.
<img width="1440" alt="Screenshot 2022-11-11 at 11 44 17 PM" src="https://user-images.githubusercontent.com/115854902/201526643-2ec04d1c-eb16-41ae-bc9e-9e8f51149615.png">

- Then also add a file to it called server.js
- We will copy and paste the web server code given into the server.js file.
- Save and close file and cat server.js to be sure of the file's content.

<img width="487" alt="Screenshot 2022-11-11 at 11 48 14 PM" src="https://user-images.githubusercontent.com/115854902/201526738-a3d7f8c3-9de2-4a1f-b362-e4f67c2ef0d4.png">

STEP 3: INSTALL EXPRESS AND SET UP ROUTES TO THE SERVER.
- Express is a minimal and flexible Node.js web application framework that provides features for web and mobile applications .
- We will also use Express to pass book information to and from our MongoDB database .
- The first step is to install express mongoose 

<img width="1440" alt="Screenshot 2022-11-11 at 11 51 08 PM" src="https://user-images.githubusercontent.com/115854902/201527233-02a8cd32-ff5d-42ee-82ee-2380f7fc1067.png">

<img width="1440" alt="Screenshot 2022-11-11 at 11 52 40 PM" src="https://user-images.githubusercontent.com/115854902/201527275-8940738b-7234-4b71-900c-69fe71873566.png">

- In the Books folder, i created a folder named apps.
- Also created a file named routes.js, saved and closed the file, also verified using the cat command.
<img width="1440" alt="Screenshot 2022-11-11 at 11 54 28 PM" src="https://user-images.githubusercontent.com/115854902/201527466-89165f11-06b5-40b3-821f-cb15bc6071a5.png">

- In the apps folder, i will create a folder named models and cd into it.
- I will also create a file named Books.js, copy and paste the code given into the book.js file , save, close and cat to verify/confirm it's content.
<img width="601" alt="Screenshot 2022-11-11 at 11 57 08 PM" src="https://user-images.githubusercontent.com/115854902/201527734-d7082667-bc7a-430e-a864-ab14f2727ead.png">

STEP 4: ACCESS THE ROUTES WITH ANGULAR JS 
- AngularJS provides a web framework for creating dynamic views in your web applications. In this project, we will use Angular JS to connect our web page with Express and perform actions on our book register .

- Now, we will gom back to our Books directory.
- Then create a folder named public and cd into it.
- I also created a file named script.js, copied and pasted the code given (Controller configuration defined) into the script.js file, save and close, cat to verify.
- In public folder, create a file named index.html, copy and paste code given into the file, save and close. Verify content using the cat command.

<img width="824" alt="Screenshot 2022-11-12 at 12 01 20 AM" src="https://user-images.githubusercontent.com/115854902/201528284-8c926756-625c-48bd-a3bd-8485202a5fa1.png">

<img width="735" alt="Screenshot 2022-11-12 at 12 27 34 AM" src="https://user-images.githubusercontent.com/115854902/201528308-6dcfcf69-ac2c-4daa-b060-2ccc82cb2d64.png">

Next, we will cd back into books directory
- Then start the server by running this command "node server.js". It will show the server is up and running and can connect via port 3300.

<img width="1440" alt="Screenshot 2022-11-13 at 4 08 55 PM" src="https://user-images.githubusercontent.com/115854902/201529048-3a412cd1-8942-4513-829f-71a2257225d6.png">

- We will use a seperate ssh console to test what the curl command returns locally. It will return an HTML page that is hardly readable in the CLI but we will access it from the internet using our public IP address:3300
- Now, we will go into our AWS Web Console to open TCP port 3300 and then go ahead to access our Book register web application  
from the internet with a browser using our Public IP address:3300


<img width="1440" alt="Screenshot 2022-11-12 at 12 13 53 AM" src="https://user-images.githubusercontent.com/115854902/201529422-843904c6-1f53-4965-994c-c3c24d85f46a.png">

<img width="1440" alt="Screenshot 2022-11-12 at 11 36 14 AM" src="https://user-images.githubusercontent.com/115854902/201529446-3229a14d-e505-421d-8e05-225f8e224551.png">







