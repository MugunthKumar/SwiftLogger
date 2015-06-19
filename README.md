# SwiftLogger
This is version 0.1 of SwiftLogger, A Logging framework written Swift

###Features
* Simple, clean and elegant log framework written in Swift
* Automatically prefixes function name and line number
* Uses emoji 😀 for easier reading of console log
* Supports [XcodeColors] (https://github.com/robbiehanson/XcodeColors)

###Installation
As easy as copying ```Log.swift``` into your project and start using it.

###How to use
You just start calling the methods ```info```, ```warn``` or ```error``` to log a message onto the console.

####Example
```
Log.error("Error")
Log.warn("Warning")
Log.info("Information")
```
displays
```
application(_:didFinishLaunchingWithOptions:) [20] 🚫Error🚫
application(_:didFinishLaunchingWithOptions:) [21] ⚠️Warning⚠️
application(_:didFinishLaunchingWithOptions:) [22] ✅Info✅
```
on your Xcode Console

Version 0.1 ships with two logs, an emoji log and a Xcode Colors log. Emoji log is set to default.
If you are using Xcode Colors plugin, use the following code
```
Log.xcodeColorsLog.info("Error")
Log.xcodeColorsLog.warn("Warning")
Log.xcodeColorsLog.error("Info")
```

###Setting the default behaviour
By setting the ```defaultLog``` property, you can customize the way your logs are formatted. 
```
Log.defaultLog = Log.xcodeColorsLog
```
Once you set the default log, ```Log.info```, ```Log.warn``` and ```Log.error``` methods will use ```xcodeColorsLog```.

###Custom Logging

You can also create your own custom loggers 

```
let customLog = Log(
  infoPrefix: "~~~ ", infoSuffix: " ~~~",
  warnPrefix: "!!!", warnSuffix: " !!!",
  errorPrefix: "XXX ", errorSuffix: " XXX")
  
customLog.info("Info")
customLog.warn("Warning")
customLog.error("Error")
```
displays
```
application(_:didFinishLaunchingWithOptions:) [20] ~~~ Info ~~~
application(_:didFinishLaunchingWithOptions:) [21] !!! Warning !!!
application(_:didFinishLaunchingWithOptions:) [22] XXX Error XXX
```
on your Xcode Console

Custom logging can be used in more powerful ways. 
For example, you can use different loggers for different builds within your application

---
###Licensing

SwiftLogger is licensed under MIT License
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

---
###Attribution free licensing
In case you need attribution free licensing for SwiftLogger, 
you can buy one from [my license store](http://blog.mugunthkumar.com/license-store/) 
or email me @ mugunth.kumar@gmail.com
