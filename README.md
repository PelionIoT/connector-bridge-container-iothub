arm PELION Device Shadow bridge for Microsoft IoTHub                  
  
08/28/2018: updated bridge - IoTHub support for connection strings, Watson fixes

08/27/2018: updated bridge - SLF4J integration, scaling fixes in shadow discovery, bug fixes.

08/27/2018: updated bridge - more bug fixes for partial configuration sanity

08/26/2018: updated bridge - fixes for proper reset recovery

08/24/2018: updated bridge - regressed bulk subscription fix

08/23/2018: updated bridge - improved MQTT abrupt disconnect handling + bulk subscriptions reset

08/22/2018: updated bridge - better handling of unconfigured API Key

08/21/2018: updated bridge, properties editor, configuration file structure

08/20/2018: updated bridge and properties editor

08/18/2018: updated bridge - enabled retain for MS IoTHub

07/31/2018: updated bridge - added optional caller_id to the API call passthu

07/30/2018: updated bridge - significant updates for API passthru calling

07/26/2018: updated properties-editor scripts

07/19/2018: updated bridge - fixed major bug in use of long polling with initial device discovery.

06/21/2018: updated bridge - minor update for Google

06/20/2018: updated bridge - major update: support for piggybacking authenticated API calls over the device connection. Additional stability updates and fixes.

05/30/2018: updated bridge - more keystore enhancements

05/29/2018: updated bridge - keystore fixes

05/13/2018: updated bridge - more lifecycle updates. Hopefully final... :-) 

05/12/2018: updated bridge - more stability updates for lifecycle/restarting, quick discovery on boot.

05/10/2018: updated bridge - device shadow lifecycle updates. AWS updates. Google updates.

05/04/2018: updated bridge - yet more fixes for device shadow deletion recovery

05/02/2018: updated bridge - more polish on MQTT recovery

05/01/2018: updated bridge - Shadow deletion and MQTT abrupt disconnect recovery.

04/18/2018: updated bridge - MQTT abrupt disconnection recovery updates.

04/12/2018: updated bridge - fixes for JwT refresh in Google Bridge. Burn in test. 

04/07/2018: updated bridge - significant refactoring of all supported bridge MQTT handlers

04/06/2018: updated bridge - MQTT reconnect fixes

04/04/2018: updated bridge - MQTT ack fixes

04/03/2018: updated bridge - MQTT exception handling updates

04/02/2018: updated bridge - minor bug in MQTT handler (null pointer trap)

03/29/2018: updated bridge - TLV parser, misc fixes

03/25/2018: bridge MQTT configuration tweaks

03/24/2018: updated bridge - Google JwT fixes

03/22/2018: updated bridge - New Google integration functional now. Additional minor bridge updates.

03/20/2018: updated bridge - significant updates for MQTT TLS support and new Google integration paradigm

02/09/2018: updated bridge - fixes for GET CoAP processing requests

01/18/2018: updated bridge - matched semantics of device removal with mbed Cloud API 

01/17/2018: updated bridge - Google API updates and fixes for latest mbed Cloud API

12/05/2017: updated bridge - Google and logging fixes/updates.

11/18/2017: updated bridge - Google and performance fixes. 

10/26/2017: updated bridge - Watson fixes.

9/29/2017: updated bridge - AWS/IoTHub fixes.

7/19/2017: updated bridge

7/12/2017: updated bridge with configurable thread executor sizing parameters.

7/10/2017: minor fix in location of the default keytore.jks file. Updated Bridge

6/29/2017: property editor updates 

6/27/2017: Minor updates 

6/20/2017: Cleanups, updates to properties editor and overall structure

Container Bridge Instance Installation:

1). Clone this repo into a Linux instance that supports docker images

2). cd into the cloned repo and run: ./run-reload-bridge.sh

Once the container instance is live, you must configure the bridge and bind it between your mbed Connector account and your IoTHub Account in Azure. 

1). Please go to your Azure dashboard and create an IoTHub instance. Note your IoTHub name.

2). Please create a SAS Token for your IoTHub Owner ... Make the token good for awhile... 
    Reference: https://azure.microsoft.com/en-us/documentation/articles/iot-hub-sas-tokens/

3). Next go to https://connector.mbed.com and create your mbed Connector Account

4). Once your Connector account is created, you need to "Access Keys" to create an API Key/Token

Now that you have your:

    - IoTHub Name

    - IoTHub Owner SAS Token generated for a suitable length of time

    - Connector API Key/Token generated

Go to:  https://[[your containers public IP address]]:8234

    - username: "admin" (no quotes)

    - password: "admin" (no quotes)

Enter each of IoTHub name, SAS Token, and Connector API Token

    - Please press "SAVE" after *each* is entered... 

    - After all 3 are entered and saved, press "RESTART"

Your Connector bridge should now be configured and operational. 

Copyright 2017. ARM Ltd. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License. 
