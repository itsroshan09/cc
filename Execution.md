#Practical 2
Flask Web Application Practical
Subject: Cloud Computing


Aim
To create and run a simple web application using Flask.


Program Code
from flask import Flask app = Flask(  name  )
@app.route('/') def home():
return "Hello Everyone"

if  name	== ' main ': app.run(debug=True)


Code Explanation
Line	Explanation
from flask import Flask Imports Flask module app = Flask( name ) Creates Flask application @app.route('/')	Defines home URL
home()	Function executed on homepage return "Hello Everyone" Displays output
app.run(debug=True)	Starts server in debug mode


Steps to Execute Practical Step 1: Install Python
Download and install Python: Python Official Website
 
During installation:
✔ Check:
Add Python to PATH


Step 2: Install Flask
Open:
Command Prompt Run command: pip install flask

Step 3: Create Python File
Create file: app.py
Paste Flask code.


Step 4: Run Application
Open terminal in project folder. Run:
python app.py


Step 5: Output
Terminal shows:
Running on http://127.0.0.1:5000/ Open browser:
http://127.0.0.1:5000/


Final Output
Hello Everyone
 
#Practical 3


Salesforce Practical: Create Application Using Apex Programming
Subject: Cloud Computing – Salesforce Apex Programming


Aim
To create an application in Salesforce using Apex Programming Language and Visualforce Page.


Step 1: Create Salesforce Developer Account
Open:
Salesforce Developer Signup

 
Fill:
 

•	Name
•	Email
•	Username
•	Company
 
Then verify email.


Step 2: Login to Salesforce
Open:
Salesforce Login
Login with:
•	Username
•	Password


Step 3: Open Developer Console Steps:
Profile Icon
↓
Developer Console
This opens coding environment.
 

Step 4: Create Apex Class Steps:
File
↓ New
↓
Apex Class
Class Name:
CreateAccount


Step 5: Paste Apex Code
Apex Class Code (Short & Updated)
public class CreateAccount {

public String accName {get; set;} public String phone {get; set;} public String website {get; set;}
public PageReference saveAccount() { Account acc = new Account(
Name = accName,
Phone = phone, Website = website
);

insert acc;

PageReference pg = new PageReference('/' + acc.Id); pg.setRedirect(true);
return pg;
}
}
Save using:
Ctrl + S


Step 6: Create Visualforce Page Steps:
 
File
↓ New
↓
Visualforce Page
Page Name:
CreateAccountPage


Step 7: Paste Visualforce Code Visualforce Page Code (Short Version)
<apex:page controller="CreateAccount">

<apex:form>

<apex:pageBlock title="Create Account">

<apex:pageBlockSection columns="1">

<apex:inputText value="{!accName}" label="Account Name"/>

<apex:inputText value="{!phone}" label="Phone"/>

<apex:inputText value="{!website}" label="Website"/>

</apex:pageBlockSection>

<apex:pageBlockButtons>

<apex:commandButton value="Save"
action="{!saveAccount}"/>

</apex:pageBlockButtons>

</apex:pageBlock>

</apex:form>

</apex:page> Save file.

Step 8: Run the Application Steps:
 
Preview
↓
Open Visualforce Page OR
Open from browser:
https://yourdomain.visualforce.com/apex/CreateAccountPage


Step 9: Enter Details Example:
Account Name : ABC Company Phone	9876543210
Website	: www.abc.com Click:
Save


Step 10: Output
After saving:
•	Account record gets created
•	Salesforce opens created Account page
 
#Practical 4


Salesforce Mini Project Practical Execution Steps (Latest Salesforce UI) Title: Design and Develop Custom Application using Salesforce Cloud Using Salesforce Lightning Experience

Aim
To design and develop a custom application using Salesforce Cloud.


Step 1: Login to Salesforce
Open:
Salesforce Login
Login using:
•	Username
•	Password


Step 2: Open Lightning Experience
After login:
Profile Icon
↓
Switch to Lightning Experience


Step 3: Open Setup Steps:
Gear Icon ⚙
↓ Setup


Step 4: Create Custom Object Steps:
Object Manager
↓
 
Create
↓
Custom Object


Step 5: Fill Object Details Enter Details
Field	Value
Label	Comment Plural Label	Comments
Record Name Comment Name Data Type	Text
Enable:
✔ Allow Reports Click:
Save


Step 6: Create Custom Tab Steps:
Quick Search
↓ Tabs
↓
Custom Object Tabs
↓ New


Step 7: Select Object Choose:
Object = Comment Choose any tab icon. Click:
Next → Next → Save
 
Step 8: Create Custom App Steps:
Quick Search
↓
App Manager
↓
New Lightning App


Step 9: Enter App Details Field	Value
App Name Comment Box App Click:
Next


Step 10: Add Navigation Items
Add:
•	Contacts
•	Comments
Move them to selected items. Click:
Next


Step 11: Assign Profiles
Select:
System Administrator Move to selected profiles. Click:
Save & Finish


Step 12: Open the Application Steps:
 
App Launcher
↓
Comment Box App
Your custom app opens.


Step 13: Create New Comment Record Steps:
Comments Tab
↓ New
Enter: Comment Name Click:
Save
