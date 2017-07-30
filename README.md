# DonaldSays (branched from setcoins-native) - iOS only 
DonaldSays - an "augmented reality" parody game intended to help combat racism and prevent the apocalypse

Currently no support for Android, but there is a separate native Java repo for the Android version (https://github.com/otech47/donaldsays) 

## Setup
1. `git clone https://github.com/otech47/react-native-donaldsays` and `cd` into the directory
2. `npm install`
3. Read through https://facebook.github.io/react-native/docs/getting-started.html to install the React Native CLI for your OS
4. `react-native start`
5. Open Xcode and run the app

6. If you are running xCode Version 8.3.3 (8E3004b) you may get this error.


        `https://github.com/facebook/react-native/issues/9920`
        
        Follow these steps:
        
        1. Open Xcode in the project navigator panel open:
        `DonaldSays\Libraries\React.xcodeproj\React\Views\RCTScrollView.m`
        
        Change code to:
        - (void)setRefreshControl:(RCTRefreshControl *)refreshControl
            {
             if (refreshControl) {
                [refreshControl removeFromSuperview];
              }
              self.refreshControl = refreshControl;
              [self addSubview:refreshControl];
            }


Required Manual Packages
1. https://github.com/pwmckenna/react-native-motion-manager

If any errors come up with any dependencies, check their documentation and you'll likely find the answer.

Please create an issue if you run into problems so we can document them and add them to this mildly helpful README.

Thanks!

Feel free to email: oscar@setdev.io
