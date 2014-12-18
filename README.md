Android ActionBarCompat-Basic Sample
===================================
该实例展示了如何使用ActionBarCompat创建一个基本的具有action item的Activity。包含了从menu的布局文件中加载
和通过代码添加Action item。

介绍
------------

由于在大多数APP里面都需要一个ToolBar，从Android3.0 开始引入ActionBar操作。这种操作
识别用户（在程序中）的位置，并提供用户的行为和导航模式。

使用ActionBar将为用户提供一个在不同应用程序熟悉的界面，并优雅地适应不同的屏幕配置。
在11以上的Android版本中，可以通过[ActionBar][1]的API实例化一个ActionBar。
支持比较旧的设备可以使用[support library’s ActionBar][2] 来实现（向下兼容到7）。
该示例使用Support Library里面的API。

使用Support Library中的Actionbar需要以下的步骤：
1. 通过extend 扩展库里面的ActionBarActivity创建一个Activity
2. 使用（或extend）一个 Theme.AppCompat 中定义的主题到你的Activity上。

遵从以上步骤后，所有的Action items 就会被创建，或者是在`[onCreateOptionsMenu()][3]`方法被调用时候
创建。

关键代码（by StormGens）
---------
在代码中为ActionBar添加菜单项：

    MenuItem locationItem = menu.add(0, R.id.menu_location, 0, R.string.menu_location);
 
          locationItem.setIcon(R.drawable.ic_action_location);
          MenuItemCompat.setShowAsAction(locationItem, MenuItem.SHOW_AS_ACTION_IF_ROOM);
          

在布局文件中声明菜单：

    <menu xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:support="http://schemas.android.com/apk/res-auto" >
        <item
            android:id="@+id/menu_settings"
            android:icon="@drawable/ic_action_settings"
            android:title="@string/menu_settings"
            support:showAsAction="never"/>
            
     </menu>


Android ActionBarCompat-Basic Sample
===================================

This sample shows you how to use ActionBarCompat to create a basic Activity
which displays action items. It covers inflating items from a menu resource,
as well as adding an item in code.

Introduction
------------

Android 3.0 introduced the “action bar” control, a toolbar that is expected
to be present in most types of applications. This control identifies the user
location, and provides user actions and navigation modes.
Using the action bar offers your users a familiar interface across applications
that the system gracefully adapts for different screen configurations.

Instantiating an action bar can be done by using the [ActionBar][1] API provided
in API 11 or above. Support for older devices is provided by the
[support library’s ActionBar][2] implementation, compatible back to API 7.
This sample demonstrates using the support library APIs.

Using an ActionBar with the support library requires the following steps:

1. Create your activity by extending ActionBarActivity.
2. Use (or extend) one of the Theme.AppCompat themes for your activity.

Once this is done, action items will be created for any options menu items that
would otherwise be created during when `[onCreateOptionsMenu()][3]` is called.

[1]: http://developer.android.com/reference/android/app/ActionBar.html
[2]: http://developer.android.com/reference/android/support/v7/app/ActionBar.html
[3]: http://developer.android.com/reference/android/app/Activity.html#onCreateOptionsMenu(android.view.Menu)

Pre-requisites
--------------

- Android SDK v21
- Android Build Tools v21.1.1
- Android Support Repository

Screenshots
-------------

<img src="screenshots/screenshot1.png" height="400" alt="Screenshot"/> <img src="screenshots/screenshot2.png" height="400" alt="Screenshot"/> 

Getting Started
---------------

This sample uses the Gradle build system. To build this project, use the
"gradlew build" command or use "Import Project" in Android Studio.

Support
-------

- Google+ Community: https://plus.google.com/communities/105153134372062985968
- Stack Overflow: http://stackoverflow.com/questions/tagged/android

If you've found an error in this sample, please file an issue:
https://github.com/googlesamples/android-ActionBarCompat-Basic

Patches are encouraged, and may be submitted by forking this project and
submitting a pull request through GitHub. Please see CONTRIBUTING.md for more details.

License
-------

Copyright 2014 The Android Open Source Project, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
