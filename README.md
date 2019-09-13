# APP-Connect-handson

### Overview
In this lab, you will create a simple application flow using IBM App Connect. You will create a basic application flow for both event driven flows and flows for API.
### Steps to register for IBM Cloud
Go to [IBM Cloud](https://cloud.ibm.com/login)
If you are a existing user, login using your credentials. If you are new user, register for IBM cloud and login.
![](img/picture1.png)
### Setup an APP Connect service
1. Lets go to [IBM Cloud Catalog](https://cloud.ibm.com/catalog) and search for App Connect.

![](img/picture2.png)

2. Click on the service App Connect to instantiate it on IBM cloud.

![](img/picture3.png)

3. Click on ```create```

![](img/picture4.png)

4. Launch the service by clicking ```Launch App Connect```

![](img/picture5.png)

### Creating event driven flows

1. After launching the dashboard, click on New. (Rename your flow, if needed)
To create a new event driven flow, ```New -> Event-driven flow```

![](img/picture6.png)

2. To add applications to your flow, Click on '+' and select applications that you want to add to your flow. Here, we are creating a simple flow to send emails at some interval of time.

![](img/picture7.png)

3. To be able to schedule events, there is a tool called scheduler in the toolbox. To add this to your flow, ```+ -> Toolbox -> Scheduler```

![](img/picture8.png)

4. Configure the scheduler component according to your preferences. Here I am creating a flow that sends email for every one minute.

![](img/picture9.png)

5. To add the next node to the flow, click on '+'. Here, we are adding email component so that we will be able to send emails at scheduled time. To do this, ```+ -> Applications -> Gmail -> Create email```

![](img/picture10.png)

6. Connect the account using which you want to automate this task(preferably your gmail account).
To connect your account, ```Click on gmail node -> Connect```. This will redirect you to gmail login page, finish the login and permissions and refresh the IBM App connect page, then you should be able to see your account in the drop down.

![](img/picture11.png)

7. Configure the email node with your details and content.

![](img/picture12.png)

8. To start the flow, click start from the right corner of the screen.

![](img/picture13.png)

9. Once the flow starts and the dashboard shows the status 'Running' that means the event flow has started. To cross check, go to your email and see if there is a new email.

![](img/picture14.png)

This is how event driven flows work, scroll down to see some sample flows in Sample flows section.

### Creating flows for API

1. To create flows for API, launch the App Connect dashboard and click on new then select flows for API. ``` Launch dashboard -> New -> Flows for API ```

![](img/picture15.png)

2. On creating, it will take you to the service page. Rename the flow(if needed). Give a name to the flow and click on Create model. ```Enter a model name -> create model```

![](img/picture16.png)

3. Add the properties that you want to add to the model that you are creating. Here, I am creating a simple flow that sends emails on sending a API request.

![](img/picture17.png)

4. After defining the properties, operations have to be added. Click on operations and select the operation that you want to perform. Here, I am selecting Create demo as operation. ``` Operations -> (scroll down) Create Demo```

![](img/picture18.png)

5. Wait for the model to load and then start adding nodes to your flow. I have added a POST method which automatically generated Request and Response nodes. Make sure that the request node has sample data configured in it which is auto-generated. Refresh the page if you are not able to see the changes.

![](img/picture19.png)

6. To add nodes to your flow, click on '+' which is in between request and response nodes. Then, add nodes to your flow. Here, I am adding a Gmail node to the flow. ``` + -> Applications -> Gmail -> Create email ```

![](img/picture20.png)

7. Configure the email node. If its not connected, click on connect and give access to your account/default account that you want to set up. Check if your node is connected to your account. Refresh the page to see changes and make sure you see your account details when you click on the node.
You can auto match the node fields or add them manually. Here, I am adding auto matched fields which are the node properties that we have added to the flow in the beginning.

![](img/picture21.png)

8. Now configure the response node as well. We can either auto match the node details or give them manually. Here we have given them manually, based on requirement we can auto-match.

![](img/picture22.png)

9. Once when all the nodes of the flow are configured, click ```Done``` on the right corner of the screen. This will take you to the previous screen and you can see properties and operations on the screen.
![](img/picture23.png)

10. Now that the flow creation is done, we have to create an API to call the flow. To do this go to manage section of the dashboard.

![](img/picture24.png)

11. ``` Manage -> Scroll```

![](img/picture25.png)

12. On the end of screen, click on create API under Sharing outside of cloud foundry organization. ```Manage -> Sharing Outside Cloud Foundry organization -> Create API```

![](img/picture26.png)

13.
Give the deatils required for API creation in the pop-up generated on clicking Create API. ```Create API -> Fill details -> Done```

![](img/picture27.png)

14. Refresh the page. Start the flow by clicking Start from right corner of the screen.```Manage -> Start API``` and then click on the API link from ```Manage -> Sharing Outside Cloud Foundry organization -> Click API link```. This will redirect you to the API page.

![](img/picture28.png)

15. CLick on ```Try it``` from the right corner which will generate automatic data.

![](img/picture29.png)

16. To test the API call, click on ```Call Operation```.

![](img/picture30.png)

17. To check if the API is working, go the email that you have set in the configuration flow. It will look something like this:

![](img/picture31.png)

### Integration servers with APP connect

### Import and export flows

### Sample flows
1. Use the For Each node and JSONata to process high-priority issues.
![](img/sf1.png)
2. Create new leads in ```Marketo``` by capturing lead names and details in ```Slack```
![](img/sf2.png)
3. For large ```Salesforce``` opportunities, send an email and create an ```Asana``` task
![](img/sf3.png)
4. At regular intervals, extract ```Salesforce lead details``` and upload ```Box files``` with CSV output.
![](img/sf4.png)
5. Create ```NetSuite ERP``` and Stripe products from ```Asana tasks``` to launch a ```Salesforce Pardot campaign```.
![](img/sf5.png)
6. Build an API to create or update leads in ```Salesforce``` based on a ```Google Sheets spreadsheet```.
![](img/sf6.png)
