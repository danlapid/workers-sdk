---
"miniflare": patch
---

fix: fix the magic proxy no longer disposing of the `dispose` and `asyncDispose` symbol properties of `RpcProperty`s

Fix the fact that from https://github.com/cloudflare/workers-sdk/pull/5670 the magic proxy no longer disposes the
`dispose` and `asyncDispose` properties found on `RpcProperty` objects causing serialization issues when trying
to proxy plain objects
