# Circular-Progress-Bar

A simple circular progressbar library for android.

<img src="https://drive.google.com/uc?id=1Cd8wgVeAjeNstWUHp98jV0Yi39OdSWB8" width="300" >

### Version
[![](https://jitpack.io/v/shrikanth7698/Circular-Progress-Bar.svg)](https://jitpack.io/#shrikanth7698/Circular-Progress-Bar)

### Installation

* **Gradle**

  Add it in your root build.gradle at the end of repositories:
  ```gradle
  allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  ```
  
  Add the dependency in your app build.gradle
  ```gradle
  dependencies {
	        compile 'com.github.shrikanth7698:Circular-Progress-Bar:v0.1.0'
	}
  ```
  
* **Maven**

  Add the JitPack repository to your build file
  ```groovy
  <repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>
  ```
   Add the dependency
  ```groovy
  <dependency>
	    <groupId>com.github.shrikanth7698</groupId>
	    <artifactId>Circular-Progress-Bar</artifactId>
	    <version>v0.1.0</version>
	</dependency>
  ```
  
### Usage

  Drop the Collapsible CalendarView in your XML layout as is shown below:
  ```xml
          <com.shrikanthravi.circularprogressbar.CircularProgressBar
              android:layout_width="150dp"
              android:layout_height="150dp"
              android:layout_centerVertical="true"
              android:layout_centerHorizontal="true"
              app:Thickness="10dp"
              app:Color="@color/colorPrimary"
              app:max="100"
              android:id="@+id/circularProgressBar"/>

  ```
  
  And then in your Activity or fragment
```java
final CircularProgressBar circularProgressBar = findViewById(R.id.circularProgressBar);
        SeekBar seekBar = findViewById(R.id.seekbar);

        seekBar.setMax(100);
        seekBar.setOnSeekBarChangeListener(new SeekBar.OnSeekBarChangeListener() {
            @Override
            public void onProgressChanged(SeekBar seekBar, int progress, boolean fromUser) {
                circularProgressBar.setProgressWithAnimation(progress);
            }

            @Override
            public void onStartTrackingTouch(SeekBar seekBar) {

            }

            @Override
            public void onStopTrackingTouch(SeekBar seekBar) {

            }
        });
```

### Customization
* `app:Thickness="10dp"`                      
* `app:progress="10"`             
* `app:min="5"`  
* `app:Color="@color/colorPrimary"`             
* `app:max="100"`

## License 

```
MIT License

Copyright (c) 2018 Shrikanth Ravi

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

  

