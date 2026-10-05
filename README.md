# gpui — Screensight fork

Patched copy of `gpui` **0.2.2**, derived from the crate published out of
[zed-industries/zed](https://github.com/zed-industries/zed) (gpui has no
standalone upstream repository).

Screensight consumes this through a rev-pinned git patch in `[patch.crates-io]`.

## Patch

Adds the GPU CRT screen-change transition:

- `Window::paint_crt_transition` in `src/window.rs`.
- `tile_alt`, `crt`, `crt_progress` and `crt_pad` on `PolychromeSprite` in `src/scene.rs`.
- `crt_transition` / `crt_sample` in `src/platform/blade/shaders.wgsl`.
