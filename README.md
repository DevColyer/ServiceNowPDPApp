# ServiceNowPDPApp

## Introduction

This is personal development plan application implemented in ServiceNow, designed to allow students and trainers to agree a development plan consisting of high-level objectives that can be broken down into tasks. Students can define their own objectives and tasks, while trainers can monitor their students' progress with their development plans. Users who are part of the resourcing group can view the progress of all students. All groups defined in the application have access to user-friendly dashboards that collate all the information they need in an intuitive manner.

## Prerequisites

Access to a ServiceNow instance. If you do not have access to an instance, free personal developer instances can be obtained by creating a developer account at https://developer.servicenow.com and requesting an instance. This application was created using the Washington DC release of ServiceNow.

## Set-up

- Fork or clone this Github repository.
- Create a [fine-grained access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-fine-grained-personal-access-token) with read write permissions. Make sure to copy the token.
- In your ServiceNow instance, navigate to **All > Connections & Credentials > Credentials**.
- Create a **New** credential and select **Basic Auth Credentials** from the list.
- Enter a name for the credential, your github username in the appropriate field and paste the token into the password field. **Submit**.
- Navigate to **All > System Applications > Studio**, which will open the Studio application in a new tab.
- Select **Import from source control** in the overlay window.
- Ensure the HTTPS protocol is selected, then enter the URL for your Github repository and select the credential you just created. All other fields can be left with default values.
- Click **Import**.

This process should set up the bulk of the application. However, some data is not backed up to source control automatically in ServiceNow so it is necessary to apply this data, which is found in the [**data directory**](data/). For each XML file in that directory, apply the data to the instance as follows:

- Ensure you are logged in as System Administrator and in the **Personal Development Planner** application scope.
- With any list view open, open the context menu for any column and select **Import XML**.
- In choose file to upload, select the XML file to be applied.
- Click **Upload**

## Contributors

The following people contributed to this application:

- @DevColyer
- @Alastair-F-Smith
