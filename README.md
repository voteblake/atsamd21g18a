# ATSAMD21G18A [![Crates.io](https://img.shields.io/crates/v/atsamd21g18a.svg)](https://crates.io/crates/atsamd21g18a)
A board support package for the ATSAMD21G18A chip from Atmel for Rust Embedded projects

## Status
Currently, this crate will build.

Two critical families of peripherals had to be removed, however. Both the SERCOM (serial communications, and TC (timer counter) peripheral definitions rely on `<cluster>` blocks to prevent register name conlficts. This is not supported in [svd](https://github.com/japaric/svd) or [svd2rust](https://github.com/japaric/svd2rust).

I'm following japaric/svd2rust#107 and japaric/svd#33. Once those are closed or I find another workaround I will rebuild to include these peripherals.
