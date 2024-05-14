### SNTPClient for Android
Simple SNTP Client class for retrieving network time on Android (SNTPClient)

<img width="250" src="https://i.imgur.com/y9AODqW.png" />

#### Copy-Paste
Copy the `NtpTime.kt` into your project, there you go. It's ready.

#### Usage

1. Retrieve the time of a specific time zone.

```kotlin
 NtpTime{ date, e ->
     date?.let {
         Log.i("dateInfo", "Success: $it")
     }
     e?.let {
         android.util.Log.i("error", "Error ${it.message}")
     }
 }
```
<hr>

2. Default time zone is `TimeZone.getDefault()` You can use different timezone.
```kotlin
 NtpTime( TimeZone.getTimeZone("US/Eastern")){ date, e ->
 }
```

#### About more

* The output time is formatted according to <a href="https://en.wikipedia.org/wiki/ISO_8601">ISO 8601</a> format.
> yyyy-MM-dd'T'HH:mm:ssZ

* Time server host is Google
> time.google.com
