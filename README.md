```
arch -arm64 brew install ios-deploy
ios-deploy --justlaunch  --debug --bundle XCUIAutomationScriptsUITests-Runner.app
```


```
1. Go to xcode => prefernces => Location => derived data path => <app_name>-<random_characters> => Build
=> Products => Debug-iphoneos => -Runner.app
2. Create a new payload directory and place the Runner.app file inside that
3. Rename that as .ipa and select use .ipa option
```

```
ideviceinstaller -u 00008101-000164922669001E -i Payload.ipa
ideviceinstaller -l

./go-ios --udid=00008101-000164922669001E launch com.browserstack.Sample-iOS
./go-ios --udid=00008101-000164922669001E launch com.bsstack.SampleXCUITests.xctrunner

./go-ios runwda --bundleid com.bsstack.SampleXCUITests.xctrunner --testrunnerbundleid 
com.bsstack.SampleXCUITests.xctrunner --xctestconfig SampleXCUITests.xctest --udid 
00008101-000164922669001E
```
