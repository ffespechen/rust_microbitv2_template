`microbitv2-template`
==================
[`microbitv2-template`] es un template para generar el "esqueleto" de un proyecto en Rust para micro:bit versión 2

## Uso

Si no lo tiene instalado, instalar [`cargo-generate`] y [`ravedude`]

```bash
cargo install cargo-generate
cargo install ravedude
```

Y luego instanciar el template

```bash
cargo generate --git https://github.com/ffespechen/rust_microbitv2_template.git
```


## Instrucciones para el entorno de desarrollo
1. Instalar rustup (por única vez) [https://rustup.rs](https://rustup.rs/) y verificar la instalación

```bash
rustc -V
```

2. Instalar cargo-binutils (por única vez).

```bash
rustup component add llvm-tools-preview
cargo install cargo-binutils --vers 0.3.3
```

3. Instalar cargo-embed (por única vez)

```bash
sudo apt install -y pkg-config libusb-1.0-0-dev libftdi1-dev libudev-dev libssl-dev
cargo install cargo-embed 
```

4. Instalar herramientas adicionales (Linux)

```bash
$ sudo apt-get install \
  gcc-arm-none-eabi \
  gdb-arm-none-eabi \
  minicom \
  openocd
```

Información adicional:

- [Embedded Rust Discovery microbot version](https://docs.rust-embedded.org/discovery/microbit/03-setup/index.html)
- [Verificar si la instalación del entorno fue exitosa](https://docs.rust-embedded.org/discovery/microbit/03-setup/verify.htm)

## Construir el binario

```bash
rustup target add thumbv7em-none-eabihf
cargo build --features v2 --target thumbv7em-none-eabihf
```

## Flashear la placa

```bash
cargo embed --features v2 --target thumbv7em-none-eabihf
```

## Licencia
Con licencia en virtud de

 - Apache License, Version 2.0
   ([LICENSE-APACHE](LICENSE-APACHE) or <http://www.apache.org/licenses/LICENSE-2.0>)
 - MIT license
   ([LICENSE-MIT](LICENSE-MIT) or <http://opensource.org/licenses/MIT>)

a su elección.

## Contribución
A menos que indique explícitamente lo contrario, cualquier contribución que usted envíe intencionadamente para su inclusión en la obra, tal y como se define en la licencia Apache-2.0, tendrá doble licencia, tal y como se ha indicado anteriormente, sin términos ni condiciones adicionales..