<<<<<<< HEAD
# LowpolyRxJava Android

An android library to convert your dull normal images into awesome ones with a crystallized lowpoly effect.
<br>
This is a feature of the WallR android app. Check it out at - https://play.google.com/store/apps/details?id=zebrostudio.wallr100&hl=en

## Samples

<div>
  <img src="app/src/main/res/mipmap-xxxhdpi/sample1.jpeg" alt="Original" width=400 height=300>
  <img src="Outputs/output1.jpeg" alt="Lowpoly" width=400 height=300>
</div>
<br>
<div>
  <img src="app/src/main/res/mipmap-xxxhdpi/sample2.jpeg" alt="Original" width=400 height=300>
  <img src="Outputs/output2.jpeg" alt="Lowpoly" width=400 height=300>
</div>
<br>
<div>
  <img src="app/src/main/res/mipmap-xxxhdpi/sample3.jpeg" alt="Original" width=400 height=300>
  <img src="Outputs/output3.jpeg" alt="Lowpoly" width=400 height=300>
</div>
<br>
<div>
  <img src="app/src/main/res/mipmap-xxxhdpi/sample4.jpeg" alt="Original" width=400 height=300>
  <img src="Outputs/output4.jpeg" alt="Lowpoly" width=400 height=300>
</div>
<br>
<div>
  <img src="app/src/main/res/mipmap-xxxhdpi/sample5.jpeg" alt="Original" width=400 height=300>
  <img src="Outputs/output5.jpeg" alt="Lowpoly" width=400 height=300>
</div>

# Installation

Step 1. Add the JitPack repository to your build file

Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  
  Step 2. Add the dependency

	dependencies {
	        implementation 'com.github.abhriyaroy:LowpolyRxJava:1.0.1'
	}

That's it!!


# Example

###### Kotlin way - <br>

	private fun generateLowpoly(originalBitmap: Bitmap): Single<Bitmap> {
		return LowPoly.generate(originalBitmap)
		 // Observe on thread according to your need
      		.observeOn(AndroidSchedulers.mainThread())
	}
	
###### Java way - <br>
  
	private Single<Bitmap> generateLowpoly(Bitmap originalBitmap){
	   	 return LowPoly.generate(originalBitmap)
	    	 // Observe on thread according to your need
      		.observeOn(AndroidSchedulers.mainThread())
	}
	
<br>

###### A full implementation is in the app module of this repo.

### Please feel free to download the debug apk and try it out yourself!

Please note that using this library, it is assumed that RxJava and RxAndroid are already added as dependencies in your project.

If you do like my work, please hit the star button.
If you have any ideas to improve upon my work feel free to raise a PR and let's learn together. :)
=======
# LowpolyRxJava Android

An android library to convert your dull normal images into awesome ones with a crystallized lowpoly effect.
<br>

## Table of Contents
- [Introduction](#introduction)
- [Samples](#samples)
- [Insights](#insights)
- [Installation](#installation)
- [Usage Example](#usage-example)
- [How to Contribute](#how-to-contribute)

## Introduction
This library serves as an improvement over this <a href="https://github.com/xyzxqs/XLowPoly">repository</a> by 
 - providing better qualityresults
 - wider choice of input sources like file path, bitmap or drawable resource.
 - natively using Rx java for background processing thereby reducing boilerplate code on the developer's end.

## Samples

<div>
  <img src="app/src/main/res/mipmap-xxxhdpi/sample1.jpeg" alt="Original" width=400 height=300>
  <img src="Outputs/output1.jpeg" alt="Lowpoly" width=400 height=300>
</div>
<br>
<div>
  <img src="app/src/main/res/mipmap-xxxhdpi/sample2.jpeg" alt="Original" width=400 height=300>
  <img src="Outputs/output2.jpeg" alt="Lowpoly" width=400 height=300>
</div>
<br>
<div>
  <img src="app/src/main/res/mipmap-xxxhdpi/sample3.jpeg" alt="Original" width=400 height=300>
  <img src="Outputs/output3.jpeg" alt="Lowpoly" width=400 height=300>
</div>
<br>
<div>
  <img src="app/src/main/res/mipmap-xxxhdpi/sample4.jpeg" alt="Original" width=400 height=300>
  <img src="Outputs/output4.jpeg" alt="Lowpoly" width=400 height=300>
</div>
<br>
<div>
  <img src="app/src/main/res/mipmap-xxxhdpi/sample5.jpeg" alt="Original" width=400 height=300>
  <img src="Outputs/output5.jpeg" alt="Lowpoly" width=400 height=300>
</div>

## Insights


## Installation

Step 1. Add the JitPack repository to your build file

Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  
  Step 2. Add the dependency

	dependencies {
	        implementation 'com.github.abhriyaroy:LowpolyRxJava:1.0.1'
	}

That's it!! <br>

Please note that using this library, it is assumed that RxJava and RxAndroid are already added as dependencies in your project but incase, you don't have these dependencies, please add the following dependencies to your `app/build.gradle` file :-
	
	dependencies{
		...
		// Rx java
  		implementation "io.reactivex.rxjava2:rxjava:$LATEST_RX_JAVA_VERSION"
  		// Rx android
  		implementation "io.reactivex.rxjava2:rxandroid:$LATEST_RX_ANDROID_VERSION"
	}

## Usage Example

##### Kotlin way - <br>

	private fun generateLowpoly(originalBitmap: Bitmap): Single<Bitmap> {
		return LowPoly.generate(originalBitmap)
		 // Observe on thread according to your need
      		.observeOn(AndroidSchedulers.mainThread())
	}
	
##### Java way - <br>
  
	private Single<Bitmap> generateLowpoly(Bitmap originalBitmap){
	   	 return LowPoly.generate(originalBitmap)
	    	 // Observe on thread according to your need
      		.observeOn(AndroidSchedulers.mainThread())
	}
	
<br>

###### A full implementation is in the app module of this repo.

## How to Contribute

Please feel free to raise an issue incase you come across a bug or even if you have any minor suggestion. Also please raise a Pull Request if you've made any improvements which you feel should be incorporated into this library.

## About the Author
### Abhriya Roy

Android Developer with 2 years of experience in building apps that look and feel great. 
Enthusiastic towards writing clean and maintainable code.
Open source contributor.

<a href="https://www.linkedin.com/in/abhriya-roy/"><img src="https://i.imgur.com/toWXOAd.png" alt="LinkedIn" width=40 height=40></a> &nbsp;
<a href="https://twitter.com/AbhriyaR"><img src="https://i.imgur.com/ymEo5Iy.png" alt="Twitter" width=42 height=40></a> 
&nbsp;
<a href="https://stackoverflow.com/users/6197251/abhriya-roy"><img src="https://i.imgur.com/JakJaHP.png" alt="Stack Overflow" width=40 height=40></a> 
&nbsp;
<a href="https://angel.co/abhriya-roy?public_profile=1"><img src="https://i.imgur.com/TiwMDMK.pngg" alt="Angel List" width=40 height=40></a>

<br>

## License

    Copyright 2019 Abhriya Roy

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
>>>>>>> Add introduction
