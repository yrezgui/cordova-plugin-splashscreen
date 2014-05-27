<!---
 license: Licensed to the Apache Software Foundation (ASF) under one
         or more contributor license agreements.  See the NOTICE file
         distributed with this work for additional information
         regarding copyright ownership.  The ASF licenses this file
         to you under the Apache License, Version 2.0 (the
         "License"); you may not use this file except in compliance
         with the License.  You may obtain a copy of the License at

           http://www.apache.org/licenses/LICENSE-2.0

         Unless required by applicable law or agreed to in writing,
         software distributed under the License is distributed on an
         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
         KIND, either express or implied.  See the License for the
         specific language governing permissions and limitations
         under the License.
-->

# org.apache.cordova.splashscreen

Plugin documentation: [doc/index.md](doc/index.md)

This plugin is a fork from the official one. It has only one line changed which remove completely the white damn splash screen. It's working only on iOS (for now).

So to fix the problem, add this plugin :

```
cordova plugin add https://github.com/yrezgui/cordova-plugin-splashscreen.git
```

Add this line on your ```config.xml``` :

```
<preference name="AutoHideSplashScreen" value="false" />
```

And a ```<script>``` in the ```<body>``` of your ```index.html``` with this content :
```
document.addEventListener('deviceready', function ready() {
  navigator.splashscreen.hide();
}, false);
```