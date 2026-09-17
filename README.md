# VeloView 🚀

> A lightning-fast, cross-platform, zero-compromise image viewer built in **Pure Rust**, leveraging GPU hardware acceleration and multi-threaded asynchronous prefetching.

---

## Features ✨

* **Blazing Fast Performance:** Zero-copy memory mapping (`mmap`) combined with multithreaded background prefetching (`rayon`) ensures instant image loading and zero-lag folder browsing.
* **Universal Format Support:** Built-in high-performance decoders for JPEG, PNG, WebP, BMP, and extended support for next-gen codecs and RAW previews.
* **GPU Hardware Accelerated Rendering:** Powered by `wgpu` (Vulkan/Metal/DirectX 12) for buttery-smooth zooming, panning, and rendering.
* **Memory Efficient:** Strict LRU cache management designed to handle massive directories of high-resolution images with minimal memory footprint.
* **Cross-Platform Single Binary:** Native compilation for Windows, macOS, and Linux with zero external runtime dependencies.

---

## Tech Stack 🛠️

* **Language:** Pure Rust (1.80+)
* **Windowing & Events:** `winit`
* **Graphics & Rendering:** `wgpu` / `pixels`
* **Image Decoding:** `zune-image` / `image-rs`
* **Concurrency & Caching:** `rayon` & `lru`
* **File IO:** `memmap2`

---

## Getting Started ⚙️

### Prerequisites

Make sure you have the Rust toolchain installed (via [rustup](https://rustup.rs/?utm_source=gemini)).

```bash
# Install Rust toolchain if you haven't already
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

```

### Building from Source

```bash
# Clone the repository
git clone https://github.com/your-username/veloview.git
cd veloview

# Build in release mode with optimizations
cargo build --release

```

### Running the Application

```bash
# Run directly with an optional image path or directory
cargo run --release -- /path/to/image_or_folder

```

---

## Usage & Shortcuts ⌨️

| Action | Shortcut / Gesture |
| --- | --- |
| **Next / Previous Image** | `Right Arrow` / `Left Arrow` or `Mouse Scroll` |
| **Zoom In / Out** | `Ctrl + Scroll` or `Pinch Gesture` |
| **Reset Zoom / Fit** | `Double Click` or `R` |
| **Toggle Fullscreen** | `F11` or `F` |
| **Quit** | `Esc` or `Ctrl + Q` |

---

## Project Roadmap 🗺️

* [x] Core windowing and GPU rendering pipeline (`winit` + `wgpu`)
* [x] Memory-mapped file I/O and multithreaded decoding (`rayon` + `mmap2`)
* [ ] LRU caching for instant pre-buffering of adjacent files
* [ ] Smooth pan and zoom matrix transformations
* [ ] Support for RAW camera file embedded preview extraction (`libraw`)

---

## License 📄

Distributed under the **MIT License**. See `LICENSE` for more information.
