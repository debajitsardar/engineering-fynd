---
layout: post
title:  "GRAVITY VIEW"
date:   2015-01-30 12:00:00
categories: project
description: Introducing Gravity View - Because swiping is so yesterday!
img: pic02.png

---

<p>Gravity View is an Android adaptation of Facebook instant articles. The concept behind the library is to utilize the motion sensors of an Android device and allow the end user to explore the product by rotating his device. It uses gyroscope motion sensor readings to scroll the image.
</p>

<p>You can read more about Gravity View article <a class="post_link" href="https://blog.gofynd.com/introducing-gravity-because-swiping-is-so-yesterday-4aebd89f0e21">here</a></p>

<a href="http://www.youtube.com/watch?v=IrNr-J1s8f8"><img src="http://img.youtube.com/vi/IrNr-J1s8f8/0.jpg" alt="Gravity View video" /></a>
<br>
<br>
<h2 id="demo">Demo</h2>
--------

<p>Install <a href="https://github.com/gofynd/gravity-view/releases/download/v1.0/gravityview-1.0.apk">Demo</a> app or APK from <a href="https://github.com/gofynd/gravity-view/releases">Releases</a> on your device and experience the gravity view.</p>

<h3 id="requirements">Requirements</h3>

<ul>
<li>Android 3.0 or higher</li>
</ul>
<br>
<h2 id="usage">Usage</h2>
--------

<h3 id="gradledependency">Gradle dependency</h3>

<pre><code>dependencies {
    compile 'co.gofynd.library:gravity-view:1.0'
}
</code></pre>

<h3 id="samplecode">Sample Code:</h3>

<h4 id="insidelayoutxmlfile">Inside Layout XML File:</h4>

<pre><code>&lt;?xml version="1.0" encoding="utf-8"?&gt;
&lt;RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/activity_main"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"&gt;
    &lt;HorizontalScrollView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:scrollbars="none"&gt;
        &lt;ImageView
            android:id="@+id/bg"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" /&gt;
    &lt;/HorizontalScrollView&gt;
&lt;/RelativeLayout&gt;
</code></pre>

<h4 id="insideactivityorfragment">Inside Activity or Fragment:</h4>

<pre><code>@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        gravityView = GravityView.getInstance(this)
                .setImage(bg, R.drawable.landingbg)
                .center();
    }
    @Override
    protected void onResume() {
        super.onResume();
        gravityView.registerListener();
    }
    @Override
    protected void onStop() {
        super.onStop();
        gravityView.unRegisterListener();
    }
</code></pre>

<h3 id="checkifdeviceissupported">Check if device is supported:</h3>

<pre><code>boolean is_supported = gravityView.deviceSupported();
</code></pre>
<br>
<h2 id="roadmap">Roadmap</h2>
--------

<ul>
<li>Multiple image support</li>

<li>Support for Non-Gyroscope devices using Accelerometer sensor</li>
</ul>
<br>
<h2 id="contributions">Contributions</h2>
--------
<p>Any contributions are welcome!
Please check the <a href="https://github.com/gofynd/gravity-view/blob/master/CONTRIBUTING.md">contributing guideline</a> before submitting a new issue.</p>
<br>
<h2 id="developedby">Developed By</h2>
--------
<ul>
<li>Fahim Sakri</li>
</ul>
<br>
<h2 id="license">License</h2>
--------
<pre><code>Copyright 2017 Shopsense Retail Technologies Pvt Ltd.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
</code></pre>