React-Native Monorepo: SimpleAuth
=================
"SimpleAuth" is sample code of authentication for web or app platforms.

This is upgrade work to [another monorepo](https://github.com/og-pr/public_ticket.524). The repos are examples for how to share code between different platforms (Web, Android, & iOS). They can be used as a template or starter-kit for React-Native & React-Native-Web. The key to code sharing is React-Native's [Platform-specific extensions](https://facebook.github.io/react-native/docs/platform-specific-code.html#platform-specific-extensions). The extensions are ```.native.js``` , ```.ios.js``` or ```.android.js``` and when used, the relevant platform file is compiled.

The main benefit of any monorepo is to share application logic. Another benefit is the rendering of individual components unique to each platform. Development is mobile-first AND then webapp.

Installation
============

* Get the repo
* From root directory, do ```yarn```
* Change root/android/local.properties as needed 
* From root/ios directory, do ```pod install``` (if needed)


**Required:** React-Native working per [Getting Started](https://facebook.github.io/react-native/docs/getting-started). If using React-Native ^0.60 , 
make sure    
you review the [blog post](https://facebook.github.io/react-native/blog/2019/07/03/version-60) & use the [upgrade guide](https://react-native-community.github.io/upgrade-helper/?from=0.59.8&to=0.60.4). As notes in those links, update these files
* Change root/android/build.gradle as needed 
* Change root/android/app/build.gradle as needed 
* Change root/android/gradle.properties as needed
* etc

Run
===

For each platform, from the root directory, do

### Web
* ```node_modules/.bin/webpack -p --progress```
* ```node_modules/.bin/webpack-dev-server --content-base public/ --config ./webpack.config.js --port 3001 --inline --hot --colors```
* Manually open a browser to localhost:3001 to see webapp 
* Inspect browser window = open console to see shared code working on button click

### Android
* ```react-native run-android -- --clear-cache```

### iOS
* ```react-native run-ios``` or open ```ios/RandomImage.xcodeproj``` with Xcode

Screenshots
===========
* TBD_1
* TBD_2
* TBD_3



Notes - Development 
===========
* [React Router](https://github.com/ReactTraining/react-router) aka 1 package is used as navigational components 
* Social Logins for [web](https://www.robinwieruch.de/react-firebase-link-social-logins/) & [mobile](https://medium.com/@chrisbianca/getting-started-with-firebase-authentication-on-react-native-a1ed3d2d6d91)  and [Password Resets](https://firebase.google.com/docs/auth/web/manage-users#set_a_users_password) , left as excercise to repo user.


Notes - Miscellaneous 
=====
* Lerna or Yarn Workspaces is not used ; there is only 1 ```node_modules``` folder.
* To make code easy to use & follow, Redux is omitted. React state is used for [web](https://reactjs.org/docs/faq-state.html) / [mobile](https://facebook.github.io/react-native/docs/state).

Inspiration
===========
* [A Firebase in React Tutorial](https://www.robinwieruch.de/complete-firebase-authentication-react-tutorial/)
* [Integrating Firebase with React Native](https://blog.jscrambler.com/integrating-firebase-with-react-native/)
