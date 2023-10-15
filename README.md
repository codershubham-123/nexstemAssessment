# nexstemAssessment
A service in Node.js using Express.js that can be deployed to AWS/GCP which exposes an API and can be consumed from any client.


1. Set up your development environment:
       Install Node.js and npm on your local machine.
   
2. Create a new Node.js project:
       Create a new directory for project.
       Initialize your project with 'npm init' to create a 'package.json' file.

3. Install required dependencies:
       You'll need Express.js as well as WebSocket. Install these packages using npm:
       npm install express
       npm install ws

4. Implement the REST Endpoints:
       Create an Express.js app and define routes for the following endpoints:
       POST /streams: Create a new stream.
       POST /streams/:id/start: Start a stream.
       POST /streams/:id/stop: Stop a stream.
       DELETE /streams/:id : Destroy a stream.
    You can use Express.js middleware to handle request and response data.

5. Implement the Stream Management:
       Maintain a data structure (map) to manage multiple streams.
       Implement a WebSocket server to send data from each stream to connected clients.

6. Testing:
       Use Postman or any other API testing tool to test your endpoints.
       Verify that the WebSocket functionality is working as expected.

7. Deployment to AWS/GCP:
   1. Prerequisites:
          You need an AWS account.
          Install the AWS Command Line Interface (CLI) on your local machine.
          Make sure your code is compatible with AWS Lambda's Node.js runtime.
   
   2. Create Your Lambda Function:
       1. Log in to the AWS Management Console.
       2. Open the Lambda service.
       3. Click the "Create function" button.
       4. Choose "Author from scratch."
       5. Configure your function:
              Name: Give your function a name.
              Runtime: Select "Node.js" (choose a compatible version).
              Role: Create a new role with the necessary permissions, or select an existing role.
       6. Click "Create function."

   3. Create a deployment package of your code with the help of npm.

   4. Upload Your Deployment Package:
       In the Lambda function configuration, under the "Function code" section, you can upload your deployment package directly or provide an S3 URL where the package is stored.

