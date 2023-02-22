# Creating-a-Serverless-Workflow-with-AWS-Step-Functions
This lab walks you through the steps to create a step function, perform get and put requests to DynamoDB and send the status of the operation using SNS notification.

Navigate to DynamoDB on the console - click create table

<img width="1792" alt="Screenshot 2023-02-22 at 13 18 51" src="https://user-images.githubusercontent.com/71371405/220631519-952a19aa-59af-4778-b423-a47e3d380067.png">

Leave the rest as default settings and bottom right of the page, create table.

<img width="1792" alt="Screenshot 2023-02-22 at 13 20 10" src="https://user-images.githubusercontent.com/71371405/220631812-ec24f2fd-5c70-407c-8b44-3069df2967c6.png">

Now on the navigate to Simple Notification service (SNS)

Wthin create topic - Topic name put- Step_function_SNS - then click next.
Leave the type as standard. And display name can stay the same as name.

<img width="1792" alt="Screenshot 2023-02-22 at 13 24 28" src="https://user-images.githubusercontent.com/71371405/220632734-ddf0e964-5326-42e5-8ea6-3fa5a7041ef4.png">

Leave other options as default and hit create bottom right.

Copy the ARN and save it for later. 

Then create subcription 

Protocol - Email
Enter your email underneath
create subscription

Check your email (even junk email) to validate 

<img width="1792" alt="Screenshot 2023-02-22 at 13 29 00" src="https://user-images.githubusercontent.com/71371405/220633724-58c6dfcf-ef8f-4d92-9210-e63b79d9efde.png">

Navigate to Step functions and on the side bar on the left-side, click on state machine. <img width="1792" alt="Screenshot 2023-02-22 at 13 36 38" src="https://user-images.githubusercontent.com/71371405/220635471-cc6ed4ae-6c20-42fd-9df9-50da51e25956.png">

Click state machine 
 
<img width="1792" alt="Screenshot 2023-02-22 at 13 38 34" src="https://user-images.githubusercontent.com/71371405/220636031-8ad5f1c8-71e3-4c3e-97ef-5d3d067dc72c.png">

Select write your workflow in code

Leave type as standard


<img width="1792" alt="Screenshot 2023-02-22 at 13 46 24" src="https://user-images.githubusercontent.com/71371405/220638334-6bdc3b8e-dc1e-4a67-bbbc-012022d43d47.png">

From the drop down you can generate a purpose. Or use the Json provided.
just rember to change your topic ARN for your own ARN which you copied before

Then click next 
<img width="1792" alt="Screenshot 2023-02-22 at 13 51 54" src="https://user-images.githubusercontent.com/71371405/220639824-eea12841-cafe-49fa-b905-668e9bebbb6a.png">

MyStateMachine as the name 
Create new role
Leave the rest as default settings, click create a state machine

<img width="1792" alt="Screenshot 2023-02-22 at 13 54 52" src="https://user-images.githubusercontent.com/71371405/220640610-976a1674-6b5d-4278-8bc0-4219bb507f4a.png">

Now to test - click start execution 
<img width="1792" alt="Screenshot 2023-02-22 at 13 56 42" src="https://user-images.githubusercontent.com/71371405/220641277-12daf046-ea5a-4b03-b3a0-7c548111e0c2.png">
Enter the code as demonstrated by the picture 

This should generate data and validate your service 

<img width="1169" alt="Screenshot 2023-02-22 at 14 09 09" src="https://user-images.githubusercontent.com/71371405/220646561-8e9eebc3-bead-4022-8e9b-7b95f114a3ec.png">


Happy Clouding 
