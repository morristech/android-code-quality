# Sensorberg Android Code Quality Script

## Preface

This, as a repo, is a live document of the standard code checks to apply on Sensorberg Android projects.
A lot of the configs presented on the initial commit are just defaults from the analysis tools and will be changed as developers discuss which ones should be kept and which ones should go. This idea for this repo is slightly inspired from [this blog post](http://continuousdev.com/2015/08/checkstyle-vs-pmd-vs-findbugs/).

## Implementation

Made to be as easy as possible. On the module `build.gradle` add the following line after android plugin

```groovy
apply from: 'https://raw.githubusercontent.com/sensorberg-dev/android-code-quality/master/checks.gradle'
```

This one line includes:

 - config for AndroidStudio code format (auto format)
 - config and execution for [lint](https://developer.android.com/studio/write/lint.html)
 - config and execution for [pmd](https://pmd.github.io/)
 - config and execution for [findbugs](http://findbugs.sourceforge.net/)
 - config and execution for [checkstyle](http://checkstyle.sourceforge.net/)
