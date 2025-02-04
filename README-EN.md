# Swifty - Make swift code swifty

[中文](README.md) | English

[![CI Status](https://img.shields.io/travis/RyukieSama/RyukieSwifty.svg?style=flat)](https://travis-ci.org/RyukieSama/RyukieSwifty)
[![Version](https://img.shields.io/cocoapods/v/RyukieSwifty.svg?style=flat)](https://cocoapods.org/pods/RyukieSwifty)
[![License](https://img.shields.io/cocoapods/l/RyukieSwifty.svg?style=flat)](https://cocoapods.org/pods/RyukieSwifty)
[![Platform](https://img.shields.io/cocoapods/p/Swifty.svg?style=flat)](https://cocoapods.org/pods/RyukieSwifty)

## 1. Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## 2. All install

```ruby
pod 'RyukieSwifty'
```

## 3. Subspec install

### 3.1 UIKit Extension

```ruby
pod 'RyukieSwifty/UIKit'
```

### 3.2 CloudKit Extension

```ruby
pod 'RyukieSwifty/CloudKit'
```

### 3.3 Foundation Extension

```ruby
pod 'RyukieSwifty/Foundation'
```

### 3.4 FullScreen Extension

```ruby
pod 'RyukieSwifty/FullScreen'
```

### 3.5 Router Protocol

```ruby
pod 'RyukieSwifty/Router'
```

### 3.6 Service Protocol - MoyaStyleProtocol

Make network request code more `Moya` style more `Swifty`. Didn`t depend on any framework, easy to change and extend.

```ruby
pod 'RyukieSwifty/SwiftyServiceProtocol'
```

### 3.7 ScreenShield (>= iOS13) - 截屏防护

Light way to protect content in view form screenshort and record. Add contents you want to protect in `ScreenShieldView`, they will be hide during screenshort and record.

![ScreenShield](ScreenShield.gif)

```ruby
pod 'RyukieSwifty/ScreenShield'
```

Swift - Demo: 

```Swift
import UIKit
import RyukieSwifty

class ViewController: UIViewController {
    override func loadView() {
        view = ScreenShieldView.create()
    }
    ...
}
```

OC - Demo:

```C++
#import "OCScreenShieldViewController.h"
@import RyukieSwifty;

@interface OCScreenShieldViewController ()

@end

@implementation OCScreenShieldViewController

- (void)loadView {
    self.view = [ScreenShieldView createWithFrame:UIScreen.mainScreen.bounds];
}

- (void)viewDidLoad {
    [super viewDidLoad];
    
    UIView *cubeView = [[UIView alloc] initWithFrame:CGRectMake(100, 100, 100, 100)];
    cubeView.backgroundColor = [UIColor redColor];
    [self.view addSubview:cubeView];
    
    self.view.backgroundColor = [UIColor grayColor];
}

@end
```

## 4. Author

RyukieSama, ryukie.sama@gmail.com

## License

Swifty is available under the MIT license. See the LICENSE file for more info.


