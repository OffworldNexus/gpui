# gpui — Screensight patched mirror

A patched copy of the published `gpui` **0.2.2** crate, derived from the source
published out of [zed-industries/zed](https://github.com/zed-industries/zed)
(`crates/gpui`).

This is a **mirror, not a fork**: gpui has no standalone upstream repository, and
building from the zed monorepo would use its `workspace`/`path` dependency graph
and clone ~520 MB. Screensight therefore consumes this crate through a rev-pinned
git patch in `[patch.crates-io]`.

## Patch

Adds the GPU CRT screen-change transition:

- `Window::paint_crt_transition` in `src/window.rs`.
- `tile_alt`, `crt`, `crt_progress` and `crt_pad` on `PolychromeSprite` in `src/scene.rs`.
- `crt_transition` / `crt_sample` in `src/platform/blade/shaders.wgsl`.
