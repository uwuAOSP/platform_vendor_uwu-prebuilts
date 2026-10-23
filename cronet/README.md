<!--
SPDX-FileCopyrightText: The uwuAOSP Project
SPDX-License-Identifier: Apache-2.0
-->

# Cronet prebuilts

These artifacts were built from the stable Cronet tree at:

```text
external/cronet @ e184145f12ee023d07372bd6db33341b671cee27
```

## Build configuration

arm64 `armv8-a` with 32-bit ARM secondary architecture. 

## Prebuilt notes

The native libraries are the stripped outputs staged in the `com.android.tethering` APEX. 

The API source files are retained only for framework-connectivity SDK stub generation. 

The prebuilt path is selected for the stable Cronet build. This prebuilt set does not support the ToT Cronet release flag; use of ToT requires restoring its source integration and source checkout.
