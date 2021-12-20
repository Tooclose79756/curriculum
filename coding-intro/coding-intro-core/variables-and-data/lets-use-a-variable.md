---
author: kapnobatai136
type: normal
category: must-know
practiceQuestion:
  formats:
    - fill-in-the-gap
    - type-in-the-gap
  context: standalone
revisionQuestion:
  formats:
    - fill-in-the-gap
  context: standalone
---

# Let's Use a Variable


---

## Content

To get us started, let's say that we have the text `"Enki"` as our data, and we want to store it in a variable named `study_buddy`:

![variable-mental-model](https://img.enkipro.com/6a73febee2278fa231f490f200282192.png)

> 💡 Unlike human names, variable names cannot hold spaces. Common naming conventions for multi-word variable names are to use *snake case* (`study_buddy`) or *camelCase* (`studyBuddy`).

In programming, putting data into a variable is usually done with the `=` sign:

```plain-text
study_buddy = "Enki"
```

> 💡 Don't worry about the quotation marks around `"Enki"` for now. We'll explain them in the insights coming up.

Putting data into a variable is called **an assignment**.

> 💡 Assignment is usually done right to left. Using `"Enki" = study_buddy` will not work.


---
apply plugin: 'com.android.library'
apply plugin: 'kotlin-android'

project.group 'com.facebook.android'

project.ext.name = 'Facebook-Login-Android-SDK'
project.ext.artifactId = "facebook-login"
project.ext.description = 'Facebook Login Android SDK'
project.ext.url = 'https://github.com/facebook/facebook-android-sdk'

dependencies {
    def kotlin_ver = project.ext.kotlinVersion
    // Facebook Dependencies
    api project(':facebook-core')
    api project(':facebook-common')
    // Support Dependencies
    implementation "androidx.appcompat:appcompat:${project.ext.androidxVersion}"

    implementation "org.jetbrains.kotlin:kotlin-stdlib-jdk7:$kotlin_ver"
}

android {
    compileSdkVersion project.ext.compileSdk
    buildToolsVersion project.ext.buildTools

    defaultConfig {
        minSdkVersion project.ext.minSdk
        targetSdkVersion project.ext.targetSdk
        consumerProguardFiles 'proguard-rules.pro'
        vectorDrawables.useSupportLibrary = true
    }

    buildTypes {
        debug {
            debuggable true
        }
    }

    aaptOptions {
        additionalParameters "--no-version-vectors"
    }

    lintOptions {
        abortOnError false
    }

    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_7
        targetCompatibility JavaVersion.VERSION_1_7
    }

    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
    }
}

if (file("${rootDir}/internal/safekit-build.gradle").exists()) {
    project.apply from: "${rootDir}/internal/safekit-build.gradle"
}

apply from: "${rootDir}/maven.gradle"

## Practice

Define a variable named `best_user` that stores `"You"`:

```plain-text
??? ??? ???
```

- best_user
- =
- "You"
- best user
- ==
- You


---

## Revision

In programming, putting data into a variable is usually done with the ??? sign:

- =
- ==
- <-
- <=
