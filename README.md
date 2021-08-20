![banner](logo/banner.png)
![Build badge](https://img.shields.io/github/workflow/status/Iltotore/EntityMetadataAPI/Java%20CI/master)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/9af1fd09f7514581a0c2d900c176d50c)](https://www.codacy.com/manual/Iltotore/ManaDrop?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Iltotore/ManaDrop&amp;utm_campaign=Badge_Grade)
[![Known Vulnerabilities](https://snyk.io/test/github/Iltotore/ManaDrop/badge.svg?targetFile=build.gradle)](https://snyk.io/test/github/Iltotore/ManaDrop?targetFile=build.gradle)
![License Badge](https://img.shields.io/github/license/Iltotore/ManaDrop)
![Release badge](https://img.shields.io/github/v/release/Iltotore/ManaDrop?include_prereleases)

This is a fork of the [original ManaDrop project](https://www.github.com/Iltotore/ManaDrop).

It fixes the generation of permission section in plugin.yml and updated Gradle to 7.2. 
However, these was done in a rather agressive way (since Java does not support extension functions)
so there is no plan to merge this fork into the master repository.

It has been given another plugin name to avoid confusion.

### How to use this variant of plugin
The binary was published with GitLab Package Registry.

In gradle.settings.kts
```kotlin
pluginManagement {
    repositories {
        gradlePluginPortal()
        maven("https://gitlab.com/api/v4/projects/28955808/packages/maven")
    }
}
```

- In build.gradle.kts
```kotlin
plugins {
    id("com.metricv.ManadropFix") version "0.5-SNAPSHOT"
}
```
