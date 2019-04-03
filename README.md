# Rust 2018 Networking Working Group

This repo is for coordinating the Rust Networking Working Group. 

- [Background on the 2018 working groups is here.][working-groups]
- [Come chat with us on #wg-net!][discord]

The [issue tracker] on this repo is a primary point of coordination. If you have a networking-related topic you'd like to raise, please feel free to open an issue!

[working-groups]: https://internals.rust-lang.org/t/announcing-the-2018-domain-working-groups/6737
[discord]: https://discord.gg/rust-lang
[issue tracker]: https://github.com/rustasync/team/issues

# Goals and structure

The WG is focused on three major areas for 2018, each of which has a dedicated subgroup, pair of leaders, and Discord channel for discussion. If you want to get involved in one or more of these efforts, hop on [Discord][discord] and say hello, or take a look at the [issue tracker].

## Async foundations

- **Leads**: @cramertj and @MajorBreakfast
- [Vision document and roster](https://rustasync.github.io/team/async-foundations)

Our goal is to bring async/await onto a path to stabilization and to provide documentation for asynchronous programming:

  - **Futures 0.3 and async/await** should be vetted, well-documented, well-integrated, future-proof, and on a clear path to stabilization.
  - **[The futures-rs blog](https://rust-lang-nursery.github.io/futures-rs/)** aims to give regular updates on the latest changes to `async`/`await` and the futures library.
  - **The [Asynchronous Programming in Rust book](https://github.com/rust-lang/async-book)** should have a complete draft, covering async/await, core futures concepts, Tokio, and enough of the ecosystem to give good examples and guidance. It should also explicitly talk about the stabilization situation, including how to bridge between stable 0.1 and unstable 0.3 worlds.

## Embedded networking foundations 

- **Leads**: @Nemo157 and @levex
- [Vision document and roster](https://rustasync.github.io/team/embedded-foundations)

Our goal is to support IoT development in Rust by:

  - **Building reusable components for `no_std` asynchronous IO and hardware access**. While `std` based projects have the great `tokio` async IO stack to build off `no_std` projects don’t have much at this point. We should provide basic prototype implementations to kickstart this area of development, then see how production ready we can get stuff.
  - **Prototyping an asynchronous IoT stack** from the hardware to the application, with a focus on ensuring portability and ease of integrating alternative layers. This should be examples of how to combine the components from the previous point into an actual IoT application, preferably based on easy to acquire development kits. The ultimate goal of this could be a guide to putting together the existing components and how to integrate your own custom components.

## Web foundations

- **Leads**: @aturon and @yoshuawuyts
- [Vision document and roster](https://rustasync.github.io/team/web-foundations)

Our goal is to improve web programming in Rust by:

  - **Bolstering web components**, i.e. assessing the state of foundational crates for web programming (like `http` and `url`), and working to improve it by writing documentation and examples, making API improvements, standardizing interfaces, and in some cases writing whole new crates.
  - **Building _Tide_**, which is a combination of a simple, modular web framework built on the above components, and extensive documentation on what the components are, how to use them directly, and how they integrate into a framework. The name "Tide" refers to "a rising tide lifts all boats", conveying the intent that this work is aimed to improve sharing, compatibility, and improvements across *all* web development and frameworks in Rust.
