<h1>AIM:</h1> <h3>To deploy this node.js application in AWS</h3>

<hr>

<h1>To start the project locally<h1/>
<h2>1. Clone this application</h2>

<pre>git clone https://github.com/opsshubam/Node.js-Deploy.git </pre>

<h2>2. Setting Environment Variables</h2>

<pre>DOMAIN= ""
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

<h2> Connect to instance using SSH</h2>

<pre> ssh -i .pemFilePath ubuntu@public_ip</pre>


 





