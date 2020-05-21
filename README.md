# GIF*t*

A Rust library for encoding and decoding GIF images.

## Documentation
[https://docs.rs/gift](https://docs.rs/gift)

## Decoding example

```rust
use gift::Decoder;
use std::fs::File;

let gif = File::open("example.gif")?;
for raster in Decoder::new(gif) {
    // was there a decoding error?
    let raster = raster?;
    // ... work with raster
}
```

## Utility

The library comes with a `gift` command-line utility, which can show the blocks
within GIF files.
```
cargo install gift --features=cmd
```
