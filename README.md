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
| `latest` | `sha256:7aafa62271988a7ce81b715981b9213b93354b06508c295071cec77042563fd2`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:7aafa62271988a7ce81b715981b9213b93354b06508c295071cec77042563fd2) | `amd64` |



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
        "docker-manifest-digest": "sha256:7aafa62271988a7ce81b715981b9213b93354b06508c295071cec77042563fd2"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "a2a26179c927fcb3d5ef29e868169295444a4a62",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/glibc-dynamic",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEQCICYwXdwssiT6PVdyX57Nai6ur4bCjYJO5MJEGGUHt5ByAiBirdFQu7ehA7COFHZ4GaXZAeYoJLxgUdBR16HSN7+NIw==",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI3MTk3NWM0OTE0OGY4ZmRjMWMyMzhiNmIzNjM4M2MxYmY3ZjA5NzliMmExYzdhZWNmNjkyYzQ3ZmI1YmFmNGUxIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUUROS3FUbU01Qkdjb3lPcUFhanVTWkxyN3YzckE5THBVNXhlWjU4Ykh6Vm5RSWdROEJsSEhFbFVSajFNZEpodk9zMEFHQytzNlNxem5ZSWNacWhEeURVcGVZPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjFla05EUVRCRFowRjNTVUpCWjBsVlREQjRNVXgwY25NNEsycGpSMEZRWnpOUU9VeG1UbEpWWkhscmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFFU1hwTlJFa3dUa1JGTkZkb1kwNU5ha2w0VFVSSmVrMUVTVEZPUkVVMFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZJUmtzNFVtaDNhSGc1Y1U1RlUxRjBaMGR2ZURac1QyTktUa3R6ZEc5TlJYbzVTMUlLYVhoT1pUbDBla2t5WTBNMlFsRjZlbVpJYUhSV2ExQlRLMkpNZFRKVVMwYzFVSEpJWnpoeFltZzNkV05xVGsxRU1UWlBRMEZzT0hkblowcGlUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZxV0dOaUNtbHBXbFk0WjFCYWJuVlBZM1poUzBGSFpHRkVlbkJWZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJKM1dVUldVakJTUVZGSUwwSkhWWGRaTkZwb1lVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5WkhOaFYwcHFURmRTTldKdFJuUmhWMDEyVEcxa2NHUkhhREZaYVRrellqTktjbHB0ZUhaa00wMTJZMjFXYzFwWFJucGFVelUxQ2xsWE1YTlJTRXBzV201TmRtRkhWbWhhU0UxMllsZEdjR0pxUVRWQ1oyOXlRbWRGUlVGWlR5OU5RVVZDUWtOMGIyUklVbmRqZW05MlRETlNkbUV5Vm5VS1RHMUdhbVJIYkhaaWJrMTFXakpzTUdGSVZtbGtXRTVzWTIxT2RtSnVVbXhpYmxGMVdUSTVkRTFDV1VkRGFYTkhRVkZSUW1jM09IZEJVVWxGUTBoT2FncGhSMVpyWkZkNGJFMUVXVWREYVhOSFFWRlJRbWMzT0hkQlVVMUZTMGRGZVZsVVNUSk5WR00xV1hwcmVVNHlXbXBaYWs1clRsZFdiVTFxYkd4UFJGazBDazFVV1RWTmFtc3hUa1JSTUZsVVVtaE9ha2wzU0VGWlMwdDNXVUpDUVVkRWRucEJRa0pCVVU5Uk0wcHNXVmhTYkVsR1NteGlSMVpvWXpKVmQweFJXVXNLUzNkWlFrSkJSMFIyZWtGQ1FsRlJabGt5YUdoaFZ6VnVaRmRHZVZwRE1YQmlWMFp1V2xoTmRsb3llSEJaYlUxMFdraHNkVmxYTVhCWmVrRmtRbWR2Y2dwQ1owVkZRVmxQTDAxQlJVZENRVGw1V2xkYWVrd3lhR3haVjFKNlRESXhhR0ZYTkhkbldYTkhRMmx6UjBGUlVVSXhibXREUWtGSlJXWlJVamRCU0d0QkNtUjNRVWxaU2t4M1MwWk1MMkZGV0ZJd1YzTnVhRXA0UmxwNGFYTkdhak5FVDA1S2REVnlkMmxDYWxwMlkyZEJRVUZaVVVOMVp6RlVRVUZCUlVGM1Fra0tUVVZaUTBsUlJHRkxWV0ZRWjNjd1drNUVXbEpLU0hCTVkxaEtZVnAyZEhCRWNrVlROM1V4UjNKUFNVTnpiRFpaZVhkSmFFRlFiMmhqV0djck1HaEVaZ3BQUWsxTFNWRlpjRGxSWTBOVVdrUlRXR3N5V1RsalltNHllVEpDY1VGdlVrMUJiMGREUTNGSFUwMDBPVUpCVFVSQk1tdEJUVWRaUTAxUlEyMDFaRFJSQ2pNMVpUZ3dMMlJTVFU5TE1saFVXR00wVkdJMWJrYzVaa1JVV0V4U2NpczJXSEZpWjBKRVZFNU9jazlxWldWclFXYzBTRFZMZHpoSmVWZFpRMDFSUTBNS1NIYzVaV1l3VEVNM1dpczVTVEpqUzAxc1dXMTNRbHBpTjJVM1pWaG5NRkpyUVVKRldEVXJXVTl1TTNOalQwbHNaVXB4TmxaM1JXOHJUVzFpY1ZkSlBRb3RMUzB0TFVWT1JDQkRSVkpVU1VaSlEwRlVSUzB0TFMwdENnPT0ifX19fQ==",
          "integratedTime": 1666493063,
          "logIndex": 5674579,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/glibc-dynamic/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/glibc-dynamic",
      "githubWorkflowSha": "a2a26179c927fcb3d5ef29e868169295444a4a62",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3305557131",
      "sha": "a2a26179c927fcb3d5ef29e868169295444a4a62"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

