<h1>AIM:</h1> <h3>To deploy this node.js application in AWS</h3>

<hr>

<h1>To start the project locally<h1/>
<h2>1. Clone this application</h2>

<pre>git clone https://github.com/opsshubam/Node.js-Deploy.git </pre>

<h2>2. Setting Environment Variables</h2>

<pre>DOMAIN= "http://localhost:3000"
PORT=3000
STATIC_DIR="./client"

PUBLISHABLE_KEY=""
SECRET_KEY=""
</pre>

A .env file is often used in Node.js applications to store configuration variables such as API keys, database URLs, and other sensitive information.

<h2>3. Run the Project</h2>
<pre>npm install</pre>
<pre>npm run start</pre>

<hr>

<h1>To deoploy the Project on AWS</h1>
<h2>1. Set up an EC2 instance in AWS</h2>
  <h3> Create an IAM User:
  <h4> - Give Administrative Access to the new user</h4>
  <h4> -Login as IAM user</h4>
    
  <h3> Create an EC2 instance</h3>
  <h4>  - Select an OS image: UBUNTU</h4>
  <h4>  - select t2.micro instance type</h4>
  <h4>  - Create a key pair (.pem file)</h4>

<h2>2. Connect to instance using SSH</h2>

<pre> ssh -i .pemFilePath ubuntu@public_ip</pre>

<hr>

<h1> Configureing Ubuntu on remote VM </h1>

<pre> sudo apt update</pre>
<pre> sudo apt install git</pre>
<pre> sudo apt install nodejs</pre>

<h1>Deploying on AWS</h1>

<h3>1. Clone this project</h3>
<pre> git clone https://github.com/opsshubam/Node.js-Deploy.git </pre>
<h3>2. Set up environment variables</h3>
<pre>DOMAIN= ""
PORT=3000
STATIC_DIR="./client"

PUBLISHABLE_KEY=""
SECRET_KEY="" 
</pre>

<h3>Initialize and start the project</h3>
<pre> npm install</pre>
<pre> npm run start</pre>

<hr>

<h2>The application is running inside the remote vm successfully but we want to access it through the open internet
</h2>
<h3>so we have to expose this 3000 port in the open internet</h3>

<h3> Edit Inbound Rules</h3>
<h4>we are allowing the inbound traffic that is we are allowing our ec2 instance to connect with the open internet</h4>
<pre>0000.0</pre> <h3>put this in the inbound rules which means the project can be accessed from anywhere</h3>






 





