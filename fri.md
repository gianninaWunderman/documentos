# documentos
#
#
#

#ANDROID
####reemplazar en FIRMessagingModule.java

public void onActivityResult(Activity activity, int requestCode, int resultCode, Intent data) {
}

@Override
public void onActivityResult(int requestCode, int resultCode, Intent data) {
}

public void onNewIntent(Intent intent){
    sendEvent("FCMNotificationReceived", parseIntent(intent));
}


#
####Borrar de app > src > java > MainApplication

import com.leblaaanc.RNStreamingKitManager.RNStreamingKitManagerPackage;
import com.tanguyantoine.MusicControl.MusicControlPackage;

new RNStreamingKitManagerPackage(),
new MusicControlPackage(),

#
####borrar de app/build.gradle 
compile project(':react-native-streamingkit')
compile project(':react-native-music-control')
