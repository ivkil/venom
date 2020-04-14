# Venom

[![](https://jitpack.io/v/YarikSOffice/lingver.svg)](https://jitpack.io/#YarikSOffice/lingver)

<img src="preview/header.png" width="300">

**Venom** is a lightweight tool that simplifies testing of the process death scenario for your android application. 

Venom makes it possible to kill the app process from the notification drawer making the testing easier and more straightforward in comparison with the traditional ways (via Developer Options or Terminate button in Android Studio), especially for a QA team.

## Setup

The setup is pretty simple:

1. Initialize the library in Application.onCreate:

``` kotlin
val venom = Venom.createInstance(this)
venom.initialize()
```

2. Call `start`/`stop` whenever you need:

``` kotlin
venom.start()
// or
venom.stop()
```
See the sample app for an example.

## Download

``` groovy
repositories {
    maven { url 'https://jitpack.io' }
}

dependencies {
    implementation "com.github.YarikSOffice:venom:0.1.0"
}
```

## License

```
The MIT License (MIT)

Copyright 2020 Yaroslav Berezanskyi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```