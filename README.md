# Ore CLI with Nvidia GPU Support

A command line interface for the Ore program to utilize Nvidia GPU's. 

## Building

To build the Ore CLI, you will need to have the Rust programming language installed. You can install Rust by following the instructions on the [Rust website](https://www.rust-lang.org/tools/install).

You must have CUDA installed [NVIDIA Cuda Download](https://developer.nvidia.com/cuda-downloads)

You Must have access to an RPC server like [Helius](dev.helius.xyz) (user referral code "aE9l0R4LPx" for extras) or Quicknode (there are others. these are best IMO)

You must have a (or several) solana keypair(s). Save these in the same directory as the one created by the git clone as "id.json", "id2.json", "id3.json", etc.

1. Git Clone this Repo
2. See Windows Users or Linux Users below

Windows users

```sh
nvcc windows.cu -o windows -ccbin <path_to_MSVC \bin\Hostx64\x64>
```

Linux users

```sh
nvcc linux.cu -o linux
```

3. Take the path to the executable that was just created (windows.exe or 'linux') and replace the PATH_TO_EXE with the path to the .exe in "/src/mine.rs".

4. Once you have Rust installed, you can build the Ore CLI by running the following command:

```sh
cargo build --release
```


```sh
/Users/[username]/ore-gpu/target/release/ore.exe --rpc "" --priority-fee 100000 --keypair "path to keypair" mine --threads 4
```

You will now run your hashing on the GPU instead of the CPU!

Donations in ORE or SOL: 7ER4M6X6wLxzYwnFWfRdA1XhEreMzKDhQx1VJ7XgSJ49

## Credits

[ORE Miner](https://github.com/tonyke-bot/ore-miner)

[ORE CLI](https://github.com/HardhatChad/ore-cli)
