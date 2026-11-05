# Charcoal instrumentation window

Dexmaker is a headless bytecode library. Its library manifests, compiler, Mockito behavior, public APIs and user consumers receive no cosmetic policy change. The one declared EmptyActivity belongs to the existing instrumentation-test APK. That app-owned diagnostic window now explicitly chooses Theme.Charcoal, including dark startup/background/system bars independent of system night mode.

The seven resources are exact copies of android-NDK38d6899706d855201239d86e1629e2620c0e8821 and are checked by ai-ci's canonical vendor guard. The existing minSDK28, compileSDK32, Gradle build and Java test architecture remain unchanged. No Java/Kotlin code or new framework is introduced. The Activity remains non-exported. No new launcher, behavior, signing identity or application data is introduced.

The normal Merge checks remain required. Separate CI assembles the existing instrumentation APK; current results and actual API29/34 window observations are pending. This empty test window deliberately has no text or controls; a populated-app ink sampler would be inapplicable. The artifact is a test fixture with the inherited debug signer, not a C67 application upgrade. No release or installed application is changed.
