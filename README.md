# AutoFitTextView

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/me.grantland/autofittextview/badge.svg?style=flat)](https://maven-badges.herokuapp.com/maven-central/me.grantland/autofittextview)

A TextView that automatically resizes text to fit perfectly within its bounds.

![Example Image](/website/static/autofittextview.gif?raw=true)


## Usage

```cson
dependencies {
    compile 'me.grantland:autofittextview:0.2.+'
}
```

Enable any View extending TextView in code:

```java
AutofitHelper.create(textView);
```

Enable any View extending TextView in XML:

```xml
<me.grantland.widget.AutofitLayout
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    >
    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:singleLine="true"
        />
</me.grantland.widget.AutofitLayout>
```

Use the built in Widget in code or XML:
```xml
<RootElement
    xmlns:autofit="http://schemas.android.com/apk/res-auto"
    ...
```   

```xml
<me.grantland.widget.AutofitTextView
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:singleLine="true"
    android:maxLines="2"
    android:textSize="40sp"
    autofit:minTextSize="16sp"
    />
```

You can add font files inside of your project with following path, you need to add new assests/fonts folder
```java
i.e. YOUR_PROJECT/src/main/assets/fonts
```
after than set font directly as below,
```xml
<me.grantland.widget.AutofitTextView
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:singleLine="true"
    android:maxLines="2"
    android:textSize="40sp"
    autofit:minTextSize="16sp"
    autofit:fontname="FONT_NAME.EXTENSION"/>
```
change fontname with your custom font, 
```java
i.e. autofit:fontname="Roboto-Bold.ttf"
```
![custom_font](https://cloud.githubusercontent.com/assets/13764097/22636444/34da74d2-ec61-11e6-895c-3ac42ce780e7.png)


## License

    Copyright 2014 Grantland Chew

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
