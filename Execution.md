# Practical 2  
# Flask Web Application Practical  
**Subject:** Cloud Computing  

---

## Aim
To create and run a simple web application using Flask.

---

# Program Code

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Hello Everyone"

if __name__ == '__main__':
    app.run(debug=True)
```

---

# Code Explanation

| Line | Explanation |
|------|-------------|
| `from flask import Flask` | Imports Flask module |
| `app = Flask(__name__)` | Creates Flask application |
| `@app.route('/')` | Defines home URL |
| `home()` | Function executed on homepage |
| `return "Hello Everyone"` | Displays output |
| `app.run(debug=True)` | Starts server in debug mode |

---

# Steps to Execute Practical

## Step 1: Install Python
Download and install Python from:

:contentReference[oaicite:0]{index=0}

During installation:

✔ Check **Add Python to PATH**

---

## Step 2: Install Flask

Open **Command Prompt**

Run command:

```bash
pip install flask
```

---

## Step 3: Create Python File

Create file:

```text
app.py
```

Paste the Flask code into the file.

---

## Step 4: Run Application

Open terminal in project folder.

Run:

```bash
python app.py
```

---

## Step 5: Output

Terminal shows:

```text
Running on http://127.0.0.1:5000/
```

Open browser:

```text
http://127.0.0.1:5000/
```

---

# Final Output

```text
Hello Everyone
```

---

# Practical 3  
# Salesforce Practical: Create Application Using Apex Programming  
**Subject:** Cloud Computing – Salesforce Apex Programming  

---

## Aim
To create an application in Salesforce using Apex Programming Language and Visualforce Page.

---

# Step 1: Create Salesforce Developer Account

Open:

:contentReference[oaicite:1]{index=1}

Fill details:

- Name
- Email
- Username
- Company

Then verify email.

---

# Step 2: Login to Salesforce

Open:

:contentReference[oaicite:2]{index=2}

Login using:

- Username
- Password

---

# Step 3: Open Developer Console

Steps:

```text
Profile Icon
   ↓
Developer Console
```

This opens the coding environment.

---

# Step 4: Create Apex Class

Steps:

```text
File
 ↓
New
 ↓
Apex Class
```

Class Name:

```text
CreateAccount
```

---

# Step 5: Paste Apex Code

## Apex Class Code

```java
public class CreateAccount {

    public String accName {get; set;}
    public String phone {get; set;}
    public String website {get; set;}

    public PageReference saveAccount() {

        Account acc = new Account(
            Name = accName,
            Phone = phone,
            Website = website
        );

        insert acc;

        PageReference pg = new PageReference('/' + acc.Id);
        pg.setRedirect(true);

        return pg;
    }
}
```

Save using:

```text
Ctrl + S
```

---

# Step 6: Create Visualforce Page

Steps:

```text
File
 ↓
New
 ↓
Visualforce Page
```

Page Name:

```text
CreateAccountPage
```

---

# Step 7: Paste Visualforce Code

## Visualforce Page Code

```html
<apex:page controller="CreateAccount">

    <apex:form>

        <apex:pageBlock title="Create Account">

            <apex:pageBlockSection columns="1">

                <apex:inputText value="{!accName}" label="Account Name"/>

                <apex:inputText value="{!phone}" label="Phone"/>

                <apex:inputText value="{!website}" label="Website"/>

            </apex:pageBlockSection>

            <apex:pageBlockButtons>

                <apex:commandButton 
                    value="Save"
                    action="{!saveAccount}"/>

            </apex:pageBlockButtons>

        </apex:pageBlock>

    </apex:form>

</apex:page>
```

Save the file.

---

# Step 8: Run the Application

Steps:

```text
Preview
 ↓
Open Visualforce Page
```

OR open in browser:

```text
https://yourdomain.visualforce.com/apex/CreateAccountPage
```

---

# Step 9: Enter Details

Example:

| Field | Value |
|------|------|
| Account Name | ABC Company |
| Phone | 9876543210 |
| Website | www.abc.com |

Click:

```text
Save
```

---

# Step 10: Output

After saving:

- Account record gets created
- Salesforce opens created Account page

---

# Practical 4  
# Salesforce Mini Project Practical Execution Steps  
## Title: Design and Develop Custom Application using Salesforce Cloud Using Salesforce Lightning Experience

---

## Aim
To design and develop a custom application using Salesforce Cloud.

---

# Step 1: Login to Salesforce

Open:

:contentReference[oaicite:3]{index=3}

Login using:

- Username
- Password

---

# Step 2: Open Lightning Experience

After login:

```text
Profile Icon
   ↓
Switch to Lightning Experience
```

---

# Step 3: Open Setup

Steps:

```text
Gear Icon ⚙
   ↓
Setup
```

---

# Step 4: Create Custom Object

Steps:

```text
Object Manager
   ↓
Create
   ↓
Custom Object
```

---

# Step 5: Fill Object Details

| Field | Value |
|------|------|
| Label | Comment |
| Plural Label | Comments |
| Record Name | Comment Name |
| Data Type | Text |

Enable:

✔ Allow Reports

Click:

```text
Save
```

---

# Step 6: Create Custom Tab

Steps:

```text
Quick Search
   ↓
Tabs
   ↓
Custom Object Tabs
   ↓
New
```

---

# Step 7: Select Object

Choose:

```text
Object = Comment
```

Choose any tab icon.

Click:

```text
Next → Next → Save
```

---

# Step 8: Create Custom App

Steps:

```text
Quick Search
   ↓
App Manager
   ↓
New Lightning App
```

---

# Step 9: Enter App Details

| Field | Value |
|------|------|
| App Name | Comment Box App |

Click:

```text
Next
```

---

# Step 10: Add Navigation Items

Add:

- Contacts
- Comments

Move them to selected items.

Click:

```text
Next
```

---

# Step 11: Assign Profiles

Select:

```text
System Administrator
```

Move to selected profiles.

Click:

```text
Save & Finish
```

---

# Step 12: Open the Application

Steps:

```text
App Launcher
   ↓
Comment Box App
```

Your custom app opens.

---

# Step 13: Create New Comment Record

Steps:

```text
Comments Tab
   ↓
New
```

Enter:

```text
Comment Name
```

Click:

```text
Save
```

---

# Final Output

- Custom Salesforce Application created successfully
- Users can create and manage Comment records
