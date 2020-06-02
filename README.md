# kotlina
Android kotlin project. Connects with nodeapi. Use it as quick start

# config
Create ./config/app.gradlew file with the following content
Create keystore file and save it inside .config
Remember .config folder is ignored by git

```
ext {
        // application
        applicationId = ?
        versionCode = ?
        versionName = ?
        appName = ?
    
        // remote api
        applicationKey = ?
    
        // signing
        keyAlias = ?
        keyPassword = ?
        storeFile = file(".config/?") // keystore file name
        storePassword = ?
    
        development = [
                // app
                appName            : "$appName Development",
    
                // remote config
                configFetchInterval: 30,
    
                // server
                baseServerURL      : ? // eg: https://api.example.com/
        ]
    
        staging = [
                // app
                appName            : "$appName Staging",
    
                // remote config
                configFetchInterval: 60,
    
                // server
                baseServerURL      : ?
        ]
    
        production = [
                // app
                appName            : "$appName",
    
                // remote config
                configFetchInterval: 3600,
    
                // server
                baseServerURL      : ?
        ]
}
```