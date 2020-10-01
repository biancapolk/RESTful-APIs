# README #

Designed, implemented and tested backend platform required for to control and manage the different pipeline services and support scenarios using Raspberry Pi data collection simulating weighted smart shelves for inventory control system and UI with tableau visualizations
• Created and deployed a RESTful API to a DigitalOcean server using Java, Express & Node.js to
• Responsible for employing JSON and URL-encoded parsers as a top-level middleware to parse the bodies of all incoming requests
• Designed and deployed NoSQL database using MongoDB
• Defined application design, development and deployment guidelines & best practices for
Web Services infrastructure

### What is this repository for? ###

* Quick summary
This component of the WeIOT solution for Target store inventory data management is used to send data recieved from inventory sensory arrays (on shelfs) that has been refined towards schema to a RESTful API on the backend in order to be stored and accessed by inventory managers.

• Created and deployed a RESTful API to a DigitalOcean server using Java, Express & Node.js
• Responsible for employing JSON and URL-encoded parsers as a top-level middleware to parse the bodies of all incoming requests
• Designed and deployed NoSQL database using MongoDB
• Defined application design, development and deployment guidelines & best practices for
Web Services infrastructure

### Functionalities of the Command In Control Backend ###
• Recieve, refined sensor array data from Gateway Controller via HTTP, access
and perform system diagnostics to be sent to UI for health updates
• Send, recieve and modify firmware updates to the data sensor array
• Client Recieving and Sending Sensor Data
• API's recieved data is processed line by line and converted in to JSON format corresponding to CIC sensor data schema. Refined data is sent to CIC Rest API via HTTP Post Request
• Request from CIC is sent to Gateway Diagnostics function in GWC via HTTP Get Request
GWD establishes connection to System Diagnostics client via WebSocket connection
• Tests and diagnostics are performed on client side
• GWC Diagnostics client send JSON formatted results to CIC Rest API for documentation and status updates via HTTP Post Request
• Client Recieving and Sending Firmware Update
• Firmware update request from CIC is sent to Gateway Controller via HTTP Post Request

## How to Run ##

CIC designed to run continuously to recieve/process data/requests until a disconnect or timeout occurs
Raspberry Pi can communicates with via the REST API. In this example, the host is located by a port address.The base URL you will use to connect to the REST API is http://{{node}}:{{port}}. Each operation performed against the REST API will use the specific operation name prepended with the base {{url}}. 

