# Mail Engine 
###### Mail Engine is a tool that sends emails. It is beginner-friendly and can send Plane Text and Rich Text (RTF) mails easily. It can also send One Time Password (OTP). 

## Functions
`genrator.num(6)`
Generate a number and can be used for sending  One Time Password (OTP) on email
we can put any number 

`sendmail.genscript('rtf','main.py')`
Generates Rich Text Formate (RTF) script. 
In case you don't want to write code

`sendmail.genscript('rtf','main.py')`
Generates Plane Text Formate script. 
In case you don't want to write code

`sendmail.mail(port,server,send_mail,receive_mail,password,message)`
Send Plane Text Email

`sendmail.sendmailrtf(port,server,send_mail,receive_mail,password,message,subject>`
Send Rich Text Mail. Use HTML only 
 

## Usage :
#### For Generating Script Use: 

    from mailengine import sendmail
 
    # genrate script with rich text formate 
    sendmail.genscript('rtf','main.py')
	
	

##### Sending Plain Text Mail:
```python
from mailengine import sendmail


port = 587 
send_mail= "sender email"
receive_mail = "receiver email"
password = "password"
server = "smtp.gmail.com" #server

message = """\
Subject: Subject

This mail was sent using mailengine (python). Add your content here, this tool >
"""
sendmail.mail(port,server,send_mail,receive_mail,password,message)
```

##### Sending Rich Text  Mail:
````python

from genOTP import sendmail


port = 465 
send_mail= "sender email"
receive_mail = "receiver email"
password = "password"
server = "smtp.gmail.com" #server

subject= "subject"
message = """
<html>
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Montserrat">
    <style type="text/css" media="screen">
        
        body {
        font-family: "Montserrat", sans-serif;
        }
        hr {
            width: 935px;
            color: rgb(80, 61, 61);
            margin: 0px 0px 0px 105px;
            opacity: 0.25
            
            
        }
    </style>
</head>
<body>
    <h1 style="color:#00466a; margin:91px 0px 15px 101px;">Test Mail</h1>
    <hr>
    <div style="margin: 31px 0px 0px 105px;">
        <p>
            Hi,
            <br>
            This mail was sent using mailengine (python).Add your content here, this tool can send mail and OTP 
        </p>
        <br>
        Regards,
        <br>
        Your Brand
    </div>

    <div style="margin: 91px 0px 0px 800px; font-size: 80%; opacity: 0.50;">
        <p>Your Brand Inc</p>
        <p>8010 Somewhere</p>
        <p>InTheWorld</p>
    </div>

</body>
</html>
"""

sendmail.sendmailrtf(port,server,send_mail,receive_mail,password,message,subject)


````
