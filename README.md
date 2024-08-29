# NodeInject
An inject tools for injecting js code into electron application

more nodeinject information: [NodeInject](https://github.com/DiamondHunters/NodeInject)

## Prepare

 Ubuntu22.04:

```bash
# install rust:
curl https://sh.rustup.rs -sSf | sh
. "$HOME/.cargo/env"

# install windows package for rust
sudo apt-get install mingw-w64
rustup target add x86_64-pc-windows-gnu

# fetch code
git clone git@github.com:iEchoxu/NodeInject.git
```



# Build
1. inject
```shell
# for linux
cargo build --bin node-inject --release
mv target/release/node-inject <Your Typora root dir>
cd <Your Typora root dir>
./node-inject

# for windows
cargo build --bin node-inject --target x86_64-pc-windows-gnu --release
mv /root/NodeInject/target/x86_64-pc-windows-gnu/release/node-inject <Your Typora root dir>
```
2. generator a license
```shell
cargo run --bin license-gen --release
```
3. open typora and input your license.



> [!NOTE]
>
> Also can build binary with Github workflows. see **Action**



## Compatibility test

- Windows / Typora 1.9.5          PASSED
- Ubuntu / Typora 1.9.5             PASSED

Since macos may adopt different packaging methods and webkit as the execution environment, this tool does not support applications under macos.



## Links

[NodeInject_Hook_example ](https://github.com/DiamondHunters/NodeInject_Hook_example) ：Use NodeInject to realize specific functions in Typora

[DiamondHunters/NodeInject](https://github.com/DiamondHunters/NodeInject) ： source code
