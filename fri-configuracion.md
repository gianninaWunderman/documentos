# CONFIGURACION
## ANDROID
#### reemplazar en FIRMessagingModule.java
```
public void onActivityResult(Activity activity, int requestCode, int resultCode, Intent data) {
}

@Override
public void onActivityResult(int requestCode, int resultCode, Intent data) {
}

public void onNewIntent(Intent intent){
    sendEvent("FCMNotificationReceived", parseIntent(intent));
}
```

#
#### Borrar de app > src > java > MainApplication
```
import com.leblaaanc.RNStreamingKitManager.RNStreamingKitManagerPackage;
import com.tanguyantoine.MusicControl.MusicControlPackage;

new RNStreamingKitManagerPackage(),
new MusicControlPackage(),
```
#
#### borrar de app/build.gradle 
```
compile project(':react-native-streamingkit')
compile project(':react-native-music-control')
```

#
#
## IOS
#### Modificar Imports sacar <'/React/......h' >
##### node_modules/react-native-firebase-crash-report/ios/RNFirebaseCrashReport/RNFirebaseCrashReport.m
```
#import "RNFirebaseCrashReport.h"
#import "RCTBridge.h",
#import "RCTConvert.h",
#import "RCTEventDispatcher.h",
#import "RCTUtils.h",
```

##### /node_modules/react-native-firebase-crash-report/ios/RNFirebaseCrashReport/RNFirebaseCrashReport.m:9:
```
#import <Foundation/Foundation.h>
#import "RCTBridgeModule.h"
```
