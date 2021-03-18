# react-native-keep-screen-on
Allows for the selective toggling of the KEEP_SCREEN_ON flag (Android) and the setIdleTimerDisabled flag (iOS).

## Installation ##
`npm install react-native-keep-screen-on --save`

## Configuration
### With [rnpm](https://github.com/rnpm/rnpm)
Just run `rnpm link react-native-keep-screen-on`

### Manually

#### In `settings.gradle` add the following lines:

```groovy
include ':KeepScreenOn'
project(':KeepScreenOn').projectDir = new File(rootProject.projectDir, '../node_modules/react-native-keep-screen-on/android')
```

#### < [0.29] : In `MainActivity.java` add the following lines:

```java
import com.gijoehosaphat.keepscreenon.KeepScreenOnPackage;
```

```java
new KeepScreenOnPackage(this)
```
#### >= [0.29] : In `MainApplication.java` add the following lines:

```java
import com.gijoehosaphat.keepscreenon.KeepScreenOnPackage;
```

```java
new KeepScreenOnPackage(this)
```

## Example usage:

```javascript
import KeepScreenOn from 'react-native-keep-screen-on'
...
//Keep screen on...
KeepScreenOn.setKeepScreenOn(true)

//Reset to default behavior...
KeepScreenOn.setKeepScreenOn(false)
```

