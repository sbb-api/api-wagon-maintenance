---
layout: default
title: Home
nav_order: 0
permalink: /
---
# SBB Cargo API for the Measurement Value Acquisition

---
## Overview
This API is used to transfer milage and operating hours measurement values of locomotives and wagons to the SBB SAP ERP system.

The API creates measurement documents in SAP ERP with the entered values. These documents ultimately control maintenance planning.

Contact: [xg041@sbbcargo.com](mailto:xg041@sbbcargo.com)

## Functionality
Currently, only measured values of locomotives are transmitted to this API. The locomotives are managed as functional locations in SAP ERP.

## Sign-up
In order for you to use the API, sign-up is required. Result of signing up is an application which provides you a token endpoint URL, a client ID and a client secret. With these information you can obtain an OAuth v2 token which is needed for the authorization of the API call.

Sign-up is done here:
* Production environment: https://developer.sbb.ch/apis/sap_apim_wagonmaintenance/information
* Integration environment: https://developer-int.sbb.ch/apis/sap_apim_wagonmaintenance/information

For sign-up the following information is needed:
* An application name (required): a meaningful name.
* MEGA ID (required): the SBB MEGA process ID which is attached to your system or alternatively your SBB account name.
* Description (required): the purpose of your application.

The authentication provider and the OAuth flow of this API are fixed and cannot be changed.
The application has to be assigned to a SBB developer portal account. If you do not have an account yet, you have to add it before you can create the application.

New applications for the Measurement API have to approved by the API Owner or one of the API providers. As soon as approval is done you will be informed by email.
After approval, it may take up to 15 minutes until the credentials are available.

## Example Data
Functional locations which can be used for testing:
* 843057-1
* 923005-3
* 482042-9

Depending on the type of the locomotive, different measurement values are recorded.

## Success/Error
If the service call is performed successfully, the corresponding measurement documents for the functional location are displayed in SAP ERP.

Application errors can have different causes:
* Functional location is not known.
* Measuring point is not available.
* Connection issues to the SAP ERP system.