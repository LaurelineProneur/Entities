# Entities
Android Studio project

Download AndroidStudio
Download Entitiesv2
Unzip Entitiesv2
Open AndroidStudio
Click file -> Open Project
Choose Entitiesv2

You can either choose to download it on your phone or on a virtual phone

/********************** You need in gradle.build (Entitiesv2_5): ****************************/

    dependencies {
        classpath 'com.android.tools.build:gradle:3.3.1'
        
        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }

/***********************  You need in gradle.build (Module app) :  ***************************/

apply plugin: 'com.android.application'

android {
    compileSdkVersion 28
    defaultConfig {
        applicationId "com.example.entitiesv2"
        minSdkVersion 15
        targetSdkVersion 28
        versionCode 1
        versionName "1.0"
        testInstrumentationRunner "android.support.test.runner.AndroidJUnitRunner"
    }
    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
        }
    }
}

dependencies {
    implementation fileTree(dir: 'libs', include: ['*.jar'])
    implementation 'com.android.support:appcompat-v7:28.0.0'
    implementation 'com.android.support.constraint:constraint-layout:1.1.3'
    testImplementation 'junit:junit:4.12'
    androidTestImplementation 'com.android.support.test:runner:1.0.2'
    androidTestImplementation 'com.android.support.test.espresso:espresso-core:3.0.2'
}


