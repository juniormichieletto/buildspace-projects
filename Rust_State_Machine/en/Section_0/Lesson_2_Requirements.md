# Initialize your Rust Project

In this step, we will initialize a basic rust project, where we can start building our simple Rust state machine.

## cargo init

1. Create a directory where you want your project to live, and navigate to that folder. We will be using a folder named `rust-state-machine`.

	```
	mkdir rust-state-machine
	cd rust-state-machine
	```

2. In that folder, initialize your rust project using `cargo init`:

	```
	cargo init
	```

	This will scaffold a basic Rust executable which we can use to start building.

3. You can verify that your new project is working as expected by running:

	```
	cargo run
	```

	You should see "Hello, World!" appear at the end of the compilation:

	```
	➜  rust-state-machine git:(master) ✗ cargo run
	Compiling rust-state-machine v0.1.0 (/Users/shawntabrizi/Documents/GitHub/rust-state-machine)
		Finished dev [unoptimized + debuginfo] target(s) in 2.19s
		Running `target/debug/rust-state-machine`
	Hello, world!
	```

If we look at what has been generated, in that folder, you will see the following:

- [src/main.rs](src/main.rs) - This is the entry point to your program. We will be building everything for this project in the `src` folder.
- [Cargo.toml](Cargo.toml) - This is a configuration file for your Rust project. Quite similar to a `package.json` that you would see in a Node.JS project. We will modify this in the future when we import crates to use in our project, but We can leave this alone for now.
- [Cargo.lock](Cargo.lock) - This is an autogenerated lock file based on your `cargo.toml` and the compilation. This usually defines the very specific versions of each crate being imported, and should not be manually edited.
- `target/*` - You might also see a target folder if you did `cargo run`. This is a folder where all the build artifacts are placed during compilation. We do not commit this folder into our git history.

All of this should be pretty familiar to you if you have already had some minimal experience with Rust. If any of this is new, I would suggest you first walk through the [Rust Book](https://doc.rust-lang.org/book/) and [Rust by Example](https://doc.rust-lang.org/rust-by-example/), as this is already an indication that this guide might not be targeted at your level of knowledge.

# Rust Tooling

In this step, we will initialize a basic rust project, where we can start building our simple Rust state machine.

## rustfmt

To keep your code clean and easy to read, we use a tool called [`rustfmt`](https://github.com/rust-lang/rustfmt).

1. Create a new file in your project's root directory called `rustfmt.toml`.

	```bash
	touch rustfmt.toml
	```
2. Use the provided `rustfmt.toml` file to configure your formatting preferences.
3. Run the code formatter using the following command:

	```bash
	cargo fmt
	```

You shouldn't see any changes this time around, but as you write more code, you will be able to see `cargo fmt` make everything look pretty, consistent, and easy to read.

> We recommend you run `cargo fmt` after every step!

## Rust Analyzer

Another popular tool in the Rust community is [Rust Analyzer](https://rust-analyzer.github.io/).

It provides many features like code completion and goto definition for code editors like VS Code.

However, to provide the full functionality that it does, Rust Analyzer needs to compile your code. For a small project like this one, this is not a problem, however working with a large project like Substrate / Polkadot-SDK, it is.

It is my personal recommendation that Rust Analyzer is not needed in this workshop, and generally you should not use it for Substrate development. However, this section might be updated in the future to include special configurations of Rust Analyzer which will work well with Polkadot SDK in the future.

However, if you would like to use it anyway, now is the right time to set it up.
ht