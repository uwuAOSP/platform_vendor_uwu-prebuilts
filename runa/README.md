<!--
SPDX-FileCopyrightText: The uwuAOSP Project
SPDX-License-Identifier: Apache-2.0
-->

# Runa Linux x86_64 prebuilt

`runa` is the Linux x86_64 host executor used by `uwuCLI/uni`. It includes the
runtime control socket interface (`--control-socket`), file-based job admission
(`--parallelism-file`), and API-safe `-d assumeexisting` behavior.

- Source project: `external/runa`
- Source revision: `ec2a20576ebac608bc527ccb0fa9571221cd47d7`
- SHA-256: `7aab8d67e0bfcf3423c0dddaaaf54fe3a3a178d9b08701bde887bc8c47ce667d`
- Runtime: Linux x86_64 with glibc and the standard C++ runtime

Refresh this prebuilt when the Runa source or its runtime-control protocol
changes. Keep the artifact and source revision metadata in the same change.
This artifact was built with AOSP's clang-r584948b host
toolchain using `configure.py --bootstrap`, then stripped with `llvm-strip`.

Runtime job limits affect new commands only. They never cancel running commands
and cannot exceed the initial `-j` limit. Missing or invalid control-file values
retain the last valid limit. Uni's recovery, signing, reporting and graph-reuse
options are handled by Uni; they are not forwarded as Runa command-line flags.
