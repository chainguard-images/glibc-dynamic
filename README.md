# glibc-dynamic

<!---
Note: Do NOT edit directly, this file was generated using https://github.com/chainguard-images/readme-generator
-->

[![CI status](https://github.com/chainguard-images/glibc-dynamic/actions/workflows/release.yaml/badge.svg)](https://github.com/chainguard-images/glibc-dynamic/actions/workflows/release.yaml)

Base image with just enough to run arbitrary glibc binaries.<br/><br/>This image is meant to be used as just a base image only. It does not contain any programs that can be run, other than `/sbin/ldconfig`.<br/><br/>You must bring your own artifacts to use this image, e.g. with a Docker multi-stage build. If you want locale support other than `C.UTF-8`, you must bring your own locale data as well. This may change in the future based on user feedback.<br/><br/>See also [musl-dynamic](https://github.com/chainguard-images/musl-dynamic) which is an equivalent image for running dynamically-linked musl binaries.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/glibc-dynamic:latest
```

## Supported tags

| Tag | Digest | Arch |
| --- | ------ | ---- |
| `migration-20221120` | `sha256:df46c5684211201b44996a42fe8a2782ebcb5a00165c7909ca46048b8cdd3a21`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:df46c5684211201b44996a42fe8a2782ebcb5a00165c7909ca46048b8cdd3a21) | `amd64` |
| `migration-20221125` | `sha256:9ded401def16a41465ccff18a376172df566c319a601801c1cfbddd03c882433`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:9ded401def16a41465ccff18a376172df566c319a601801c1cfbddd03c882433) | `amd64` |
| `migration-20221123` | `sha256:d4dba60fd9881742e59ad9df77409de64271f5a5b7c198cf52e519b6294219f2`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d4dba60fd9881742e59ad9df77409de64271f5a5b7c198cf52e519b6294219f2) | `amd64` |
| `migration-20221124` | `sha256:7f8e4f7f782210c0b610db299a9dd3b7ba5329b81171b56558a492e3ff1afb32`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:7f8e4f7f782210c0b610db299a9dd3b7ba5329b81171b56558a492e3ff1afb32) | `amd64` |
| `latest` | `sha256:1f20b60bd291e7542bdcb4fa707f418201b03ce93fd3db9f2fc40bab51e04a6c`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:1f20b60bd291e7542bdcb4fa707f418201b03ce93fd3db9f2fc40bab51e04a6c) | `amd64` |
| `migration-20221118` | `sha256:cf9690c4cc99d81adbadd64683c82c2eb3ec778cab279b5eff793b93774e19fa`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:cf9690c4cc99d81adbadd64683c82c2eb3ec778cab279b5eff793b93774e19fa) | `amd64` |
| `migration` `migration-20221127` | `sha256:ab479eb1378b1f98dd5a7653db45830bc85144bff516ce3ca5bd893dceb7dc20`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ab479eb1378b1f98dd5a7653db45830bc85144bff516ce3ca5bd893dceb7dc20) | `amd64` |
| `migration-20221119` | `sha256:dc022e6e10500cb7e49c2bf7af59b3ae14d57f49fae32152fc62b4bc97167be6`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:dc022e6e10500cb7e49c2bf7af59b3ae14d57f49fae32152fc62b4bc97167be6) | `amd64` |
| `migration-20221121` | `sha256:f441a9228beedbbdd562081ca0a64041254b2339b40e5b4b7b7c9c16d3808363`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:f441a9228beedbbdd562081ca0a64041254b2339b40e5b4b7b7c9c16d3808363) | `amd64` |
| `migration-20221122` | `sha256:b10469c16061d6d941a8fb63b6b90277f37599e9030ff7515aeff813c6fa70f0`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:b10469c16061d6d941a8fb63b6b90277f37599e9030ff7515aeff813c6fa70f0) | `amd64` |
| `migration-20221126` | `sha256:9446420eb0a15c558110a6e4b7631f34cd489c6d557246c18075d3ec63b80d5d`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:9446420eb0a15c558110a6e4b7631f34cd489c6d557246c18075d3ec63b80d5d) | `amd64` |



## Signing

All Chainguard Images are signed using [Sigstore](https://sigstore.dev)!

<details>
<br/>
To verify the image, download <a href="https://github.com/sigstore/cosign">cosign</a> and run:

```
COSIGN_EXPERIMENTAL=1 cosign verify cgr.dev/chainguard/glibc-dynamic:latest | jq
```

Output:
```
Verification for cgr.dev/chainguard/glibc-dynamic:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - Any certificates were verified against the Fulcio roots.
[
  {
    "critical": {
      "identity": {
        "docker-reference": "ghcr.io/chainguard-images/glibc-dynamic"
      },
      "image": {
        "docker-manifest-digest": "sha256:1f20b60bd291e7542bdcb4fa707f418201b03ce93fd3db9f2fc40bab51e04a6c"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "93bafcb8aedeb622256b84b19699a40e6fc6895d",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/glibc-dynamic",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIEZiNA5MERb/0MZKhk92brVxcVXCRGRYUjmUv4V1wPIJAiEA6kxHbjjANqQGIFy1zgUFda70UMPNI9YLumQJStY66Z0=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiJhNzY1ZmJmNzJkNWFjNTIyMTBjMTAzMjMyN2U0ZTQ1ZWJjZDNkZGRkNzBkOThkN2NjNjdlYjY1NjkwZGJhN2QwIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJSHp1K3hnWmZUV1JScTk5V3dOYUltc3dWR0U3TE9Hc0toNXRJTWllNDVjWUFpRUEwcWJEaDJVTW5OQUNSdUJVR0tuQzAxNllaMXhRT0hrbTQ3UTh6clpBSzBFPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjFWRU5EUVhvclowRjNTVUpCWjBsVlFsQnRlVGRRVjFscVZVTk9kM280WTA5MFZWVTBNbXROVVhOWmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1ROTlJFRjVUbXBGZDFkb1kwNU5ha2w0VFZSSk0wMUVRWHBPYWtWM1YycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZNUkVaQmJuSjJZMG9yTm05eU1YbzRiRXBPZFRKWVdVUXhWSFEwWjFOdVJWRnZZbUlLV205a01GSlpkR2sxZVRoR01EZDVhbmxJVkdsTlIxaHpaa2xvVERWWk5IQjZVbFZwZUdRcmVUVXpiRkZ6U1cxc1FVdFBRMEZzTkhkblowcGhUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlU0V2tjMkNqRlRUVVpYVGpKc1ZucEdiakpYWkc1NFdWUXdlbUkwZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJKM1dVUldVakJTUVZGSUwwSkhWWGRaTkZwb1lVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5WkhOaFYwcHFURmRTTldKdFJuUmhWMDEyVEcxa2NHUkhhREZaYVRrellqTktjbHB0ZUhaa00wMTJZMjFXYzFwWFJucGFVelUxQ2xsWE1YTlJTRXBzV201TmRtRkhWbWhhU0UxMllsZEdjR0pxUVRWQ1oyOXlRbWRGUlVGWlR5OU5RVVZDUWtOMGIyUklVbmRqZW05MlRETlNkbUV5Vm5VS1RHMUdhbVJIYkhaaWJrMTFXakpzTUdGSVZtbGtXRTVzWTIxT2RtSnVVbXhpYmxGMVdUSTVkRTFDV1VkRGFYTkhRVkZSUW1jM09IZEJVVWxGUTBoT2FncGhSMVpyWkZkNGJFMUVXVWREYVhOSFFWRlJRbWMzT0hkQlVVMUZTMFJyZWxsdFJtMVpNa2swV1ZkV2ExcFhTVEpOYWtsNVRsUmFhVTlFVW1sTlZHc3lDazlVYkdoT1JFSnNUbTFhYWs1cVp6Vk9WMUYzU0VGWlMwdDNXVUpDUVVkRWRucEJRa0pCVVU5Uk0wcHNXVmhTYkVsR1NteGlSMVpvWXpKVmQweFJXVXNLUzNkWlFrSkJSMFIyZWtGQ1FsRlJabGt5YUdoaFZ6VnVaRmRHZVZwRE1YQmlWMFp1V2xoTmRsb3llSEJaYlUxMFdraHNkVmxYTVhCWmVrRmtRbWR2Y2dwQ1owVkZRVmxQTDAxQlJVZENRVGw1V2xkYWVrd3lhR3haVjFKNlRESXhhR0ZYTkhkbldXOUhRMmx6UjBGUlVVSXhibXREUWtGSlJXWkJValpCU0dkQkNtUm5SR1JRVkVKeGVITmpVazF0VFZwSWFIbGFXbnBqUTI5cmNHVjFUalE0Y21ZclNHbHVTMEZNZVc1MWFtZEJRVUZaVXpKbGFYSldRVUZCUlVGM1FrZ0tUVVZWUTBsUlJERTNXblUwZFZZNFFYSjZPSEJUWVRaTFduRkZla3hNUWxCck5UQlNOV3RzVDJKWVVHTkJXRkJUUzJkSloxZDRjemRQY0hGc2JYVTNid3AwTUVGMk5qVmxaMjB6TkZZelRFUjBWVlJWYTJSbmNXZEJla3d2UTI5dmQwTm5XVWxMYjFwSmVtb3dSVUYzVFVSaFFVRjNXbEZKZUVGT2FWZG9RMVY2Q25sek1XTkVRMHAxTWtZek4yODBaVzFJUVdwbksyZ3JhMVZIUTFaWGRVWjJaWGREWWxCRlVtaEVLMHdyT1dKc1JrRlRUalp1WjBwVU0wRkpkMDRyU21zS1MzRkRSMHBGYm1ONmIwTXZjRk53Y1dKeEx6UXJNeTlIYjJWdFYxQnpNV05oY1dsMlQycEZPR1pZTW5ONGQwVjRVMGRsUlhSQ0wzUnpkME5WQ2kwdExTMHRSVTVFSUVORlVsUkpSa2xEUVZSRkxTMHRMUzBLIn19fX0=",
          "integratedTime": 1669508773,
          "logIndex": 7918060,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/glibc-dynamic/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/glibc-dynamic",
      "githubWorkflowSha": "93bafcb8aedeb622256b84b19699a40e6fc6895d",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3555987847",
      "sha": "93bafcb8aedeb622256b84b19699a40e6fc6895d"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

