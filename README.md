# tklog

A C & Obj-c logging library, inspired by LCL.

[![CI Status](http://img.shields.io/travis/Taras Kalapun/tklog.svg?style=flat)](https://travis-ci.org/xslim/tklog.c)
[![Version](https://img.shields.io/cocoapods/v/tklog.svg?style=flat)](http://cocoadocs.org/docsets/tklog)


## Usage

``` c
#define log_component "App"
#import "tklog.h"

adylog_add_component("App");
adylog_add_component("App.utils");

adylog_configure_by_name("App*", tklog_vInfo);
log_info("Initialized version: %s", "0.1.1");

```

Or in `Objective-C`, it will automatically use `NSString`

``` obj-c
log_info(@"Initialized version: %@", @"0.1.1");
```

## Installation

`tklog` is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

    pod "tklog"

## Embedding

You can embed the library with custom name. To do so, run

``` sh
sh <(curl -sL https://github.com/xslim/tklog.c/raw/master/embed.sh) myprefix Libs/mylog
```

This will download the latest version and replase `tklog` with `myprefixlog`

Or in a script, Ex `update_embedded_libs.sh`

``` shell
#!/bin/sh
curl -sL https://github.com/xslim/tklog.c/raw/master/embed.sh | \
  bash /dev/stdin ady Classes/Public
```

## Author

Taras Kalapun, t.kalapun@gmail.com

## License

tklog is available under the MIT license. See the LICENSE file for more info.

