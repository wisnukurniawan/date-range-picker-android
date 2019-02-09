Date Time Range Picker for Android
==========================

Standalone Android widget for picking a single date from a calendar view.

![Screenshot](screenshot.png)

## Installation
### Via Gradle
Add it in your root build.gradle at the end of repositories:

```
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```
Add the dependency:

```
dependencies {
	implementation 'com.github.wisnukurniawan:date-time-range-picker-android:1.0.0'
}

```

## Usage
-----

Include `CalendarPickerView` in your layout XML.

```xml
<com.wisnu.datetimerangepickerandroid.CalendarPickerView
    android:id="@+id/calendar_view"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    />
```

Default implementation to show Calendar

```java
calendar.init(today, nextYear.getTime())
    .inMode(RANGE);
```


To show the Calendar

```java
Calendar nextYear = Calendar.getInstance();
nextYear.add(Calendar.YEAR, 1);

CalendarPickerView calendar = (CalendarPickerView) findViewById(R.id.calendar_view);
Date today = new Date();
calendar.init(today, nextYear.getTime())
    .withSelectedDate(today);
```

## Proguard
No configuration needed.
