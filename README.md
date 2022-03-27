# build.gradleapply plugin: 'com.android.application'

/* ironsource */ /* repositories {
    maven {
        url "https://dl.bintray.com/ironsource-mobile/android-sdk"
    }
} */ /* ironsource */

0 android {
    compileSdkVersion 31
    buildToolsVersion '31.0.0 rc5'

    defaultConfig {
        applicationId "com.udaftpunkburak.appkhjgvhj"
        minSdkVersion 16
        targetSdkVersion 31
        multiDexEnabled true

        ndk {
            moduleName "BBRuntime_shared"
        }
        versionCode 1.0
        versionName '1.1'
    }

    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.txt'
        }
    }


    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }

    dexOptions {
        javaMaxHeapSize "4g"
    }
}

dependencies {
    implementation 'com.google.android.gms:play-services-base:17.3.0'
    implementation 'com.google.android.gms:play-services-games:19.0.0'
    implementation 'androidx.multidex:multidex:2.0.1'
    implementation "androidx.preference:preference:1.1.1"
    implementation 'androidx.appcompat:appcompat:1.1.0'
    implementation 'androidx.constraintlayout:constraintlayout:1.1.3'
    implementation fileTree(dir: 'libs', include: ['*.jar'/*, '*.aar'*/])
    implementation project(':aob_sessionreporting')
    implementation project(":aob_admon_shared")
    /* ironsource */ /* implementation 'com.ironsource.sdk:mediationsdk:7.1.1'
    implementation 'com.google.android.gms:play-services-ads-identifier:17.0.0'
    implementation 'com.google.android.gms:play-services-basement:17.1.1' */ /* ironsource */
    /* admob */ /* implementation 'com.google.android.gms:play-services-ads:19.7.0' */ /* admob */
    /* applovin */
    implementation 'com.applovin:applovin-sdk:10.1.1'
    implementation 'io.reactivex.rxjava2:rxjava:2.2.21'
    implementation 'com.squareup.retrofit2:retrofit:2.9.0'
    implementation 'com.squareup.retrofit2:converter-gson:2.9.0'
    implementation 'com.squareup.retrofit2:adapter-rxjava2:2.9.0'
    implementation project(':aob_applovin')
    /* applovin */
    /* facebook-analytics */ /* implementation 'com.facebook.android:facebook-android-sdk:7.1.0' */ /* facebook-analytics */
    // More deps here //

}
