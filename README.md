Android-Bazaar-RateThisApp
===================

Android-Bazaar-RateThisApp is a library to show "Rate this app" dialog, based on [Android-RateThisApp](https://github.com/kskkbys/Android-RateThisApp) by Keisuke Kobayashi.

![Screen shot](https://raw.githubusercontent.com/thesoulless/Android-Bazaar-RateThisApp/master/screenshot_resized.png)

The library monitors the following status

* How many times is the app launched
* How long days does it take from the app installation

and show a dialog to engage users to rate the app in [CafeBazaar](http://getbazaar.com) or Google Play.

## How to use

### Download
```sh
git clone git@github.com:thesoulless/Android-Bazaar-RateThisApp.git
```

### Implementation
Call `RateThisApp.onStart(Context)` and `RateThisApp.showRateDialogIfNeeded(Context)` in your launcher activity's onStart() method.
```java
@Override
protected void onStart() {
    super.onStart();

    // Monitor launch times and interval from installation
    RateThisApp.onStart(this);
    // If the criteria is satisfied, "Rate this app" dialog will be shown
    RateThisApp.showRateDialogIfNeeded(this);
}
```

### Custom criteria
The default criteria to show the dialog is as below:

* App is launched more than 10 times
* App is launched more than 7 days later than installation.

If you want to use your own criteria, please edit constants in RateThisApp.java.

## License
This software is licensed under [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

## Author
Keisuke Kobayashi - k.kobayashi.122@gmail.com
