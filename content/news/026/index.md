+++
title = "This Month in Rust GameDev #26 - September 2021"
transparent = true
date = 2021-10-04
draft = true
+++

<!-- no toc -->

<!-- Check the post with markdownlint-->

Welcome to the 26th issue of the Rust GameDev Workgroup's
monthly newsletter.
[Rust] is a systems language pursuing the trifecta:
safety, concurrency, and speed.
These goals are well-aligned with game development.
We hope to build an inviting ecosystem for anyone wishing
to use Rust in their development process!
Want to get involved? [Join the Rust GameDev working group!][join]

You can follow the newsletter creation process
by watching [the coordination issues][coordination].
Want something mentioned in the next newsletter?
[Send us a pull request][pr].
Feel free to send PRs about your own projects!

[Rust]: https://rust-lang.org
[join]: https://github.com/rust-gamedev/wg#join-the-fun
[pr]: https://github.com/rust-gamedev/rust-gamedev.github.io
[coordination]: https://github.com/rust-gamedev/rust-gamedev.github.io/issues?q=label%3Acoordination

[Rust]: https://rust-lang.org
[join]: https://github.com/rust-gamedev/wg#join-the-fun

- [Rust GameDev Podcast](#rust-gamedev-podcast-6)
- [Game Updates](#game-updates)
- [Learning Material Updates](#learning-material-updates)
- [Engine Updates](#engine-updates)
- [Tooling Updates](#tooling-updates)
- [Library Updates](#library-updates)
- [Popular Workgroup Issues in Github](#popular-workgroup-issues-in-github)
- [Meeting Minutes](#meeting-minutes)
- [Requests for Contribution](#requests-for-contribution)
- [Jobs](#jobs)
- [Bonus](#bonus)

<!--
Ideal section structure is:

```
### [Title]

![image/GIF description](image link)
_image caption_

A paragraph or two with a summary and [useful links].

_Discussions:
[/r/rust](https://reddit.com/r/rust/todo),
[twitter](https://twitter.com/todo/status/123456)_

[Title]: https://first.link
[useful links]: https://other.link
```

If needed, a section can be split into subsections with a "------" delimiter.
-->

## Rust GameDev Meetup

![Gamedev meetup poster](../025/gamedev-meetup.png)

The ninth Rust Gamedev Meetup happened in September. You can watch the recording
of the meetup [here on Youtube][gamedev-meetup-video]. The meetups take place on
the second Saturday every month via the [Rust Gamedev Discord
server][rust-gamedev-discord] and are also [streamed on
Twitch][rust-gamedev-twitch]. If you would like to show off what you've been
working on at the next meetup on [October 9th][rust-meetup-oct-time], fill out
[this form][gamedev-meetup-form].

[gamedev-meetup-form]: https://forms.gle/BS1zCyZaiUFSUHxe6
[gamedev-meetup-video]: https://youtu.be/TH3AErcNcTY
[rust-gamedev-discord]: https://discord.gg/yNtPTb2
[rust-gamedev-twitch]: https://twitch.tv/rustgamedev
[rust-meetup-oct-time]: https://everytimezone.com/s/aa44ac42

## Rust Graphics Meetup \#1

![logo](graphics-meetup.png)

The Rust Graphics Meetup is an online gathering where rustaceans share
technical details of their work related to graphics and compute,
not affiliated to any particular stack.
The pilot edition has happened on Oct 2nd! Check out the talks:

- [gfx-rs Lessons Learned][rgm1-video] - [@kvark], [slides][rgm1-slides].
- [rend3 Architecture: Efficient, Customizable Rendering][rgm2-video] -
  [@cwfitzgerald], [slides][rgm2-slides].
- [Blub - Interactive GPU Fluid Solver][rgm3-video] - [@wumpf], [slides][rgm3-slides].

Learn more at the [gfx meetup repo].
Thanks everyone for tuning in and helping to make this happen!

_Discussions:
[/r/rust](https://reddit.com/r/rust/comments/q08byh/videos_from_rust_graphics_meetup_1),
[Twitter](https://twitter.com/rust_gamedev/status/1444326130035666953)_

[rgm1-video]: https://youtube.com/watch?v=m0JgF5Wb-dA
[rgm1-slides]: https://github.com/gfx-rs/meetup/blob/main/Meeting01/GfxLessonsLearned.pdf
[rgm2-video]: https://youtube.com/watch?v=F0wGz5UJTrY
[rgm2-slides]: https://github.com/gfx-rs/meetup/blob/main/Meeting01/rend3s_Architecture_-_Efficient_Customizable_Rendering.pdf
[rgm3-video]: https://youtube.com/watch?v=Yzr9va5UtiE
[rgm3-slides]: https://github.com/gfx-rs/meetup/blob/main/Meeting01/Blub_-_Quick_tour_through_a_GPU_fluid_solver.pdf
[gfx meetup repo]: https://github.com/gfx-rs/meetup
[@kvark]: https://github.com/kvark
[@cwfitzgerald]: https://github.com/cwfitzgerald
[@wumpf]: https://github.com/wumpf

## [Rust GameDev Podcast #6][podcast-6]

![text logo](podcast.jpeg)

[The sixth episode][podcast-6] is an interview with Remco and Basz, creators of
[Mun][mun]. Programming language creation is discussed, along with challenges
and what future developments are incoming from the [Mun project][mun].

Listen and Subscribe from the following platforms:
[Rust GameDev Podcast (simplecast)][gamedev-podcast-site],
[Apple Podcasts][gamedev-podcast-apple],
[Spotify][gamedev-podcast-spotify],
[RSS Feed][gamedev-podcast-rss],
[Google Podcasts][gamedev-podcast-google].

[podcast-6]: https://rustgamedev.com/episodes/interview-with-remco-and-basz
[mun]: https://mun-lang.org/
[gamedev-podcast-site]: https://rustgamedev.com/
[gamedev-podcast-apple]: https://podcasts.apple.com/gb/podcast/rust-game-dev/id1526304768
[gamedev-podcast-spotify]: https://open.spotify.com/show/7HRfGnTcXkLkQd9fxJbDGj
[gamedev-podcast-rss]: https://feeds.simplecast.com/C6NQglnL
[gamedev-podcast-google]: https://podcasts.google.com/feed/aHR0cHM6Ly9mZWVkcy5zaW1wbGVjYXN0LmNvbS9DNk5RZ2xuTA

## Game Updates

### [BITGUN][bitgun-steam]

[![Gameplay screenshot with lots of zombies and a zombie boss](bitgun.jpeg)][bitgun-steam]

BITGUN ([Steam][bitgun-steam], [Twitter][bitgun-twitter],
[Discord][bitgun-discord]) by [@LogLogGames][bitgun-twitter] is an action
roguelike zombie shooter with lots of blood and guns, similar to games like
Hotline Miami, Nuclear Throne and Heat Signature. The game is built using Godot
and Rust (via [godot-rust][bitgun-godot-rust]).

They recently re-worked the in-game UI using [egui][bitgun-egui] with
[godot-egui][bitgun-godot-egui], allowing much easier custom widgets such as
[drag & drop on items between inventory slots][bitgun-inventory].

_Discussions: [Twitter][bitgun-inventory]_

[bitgun-steam]: https://store.steampowered.com/app/1673940/BITGUN/
[bitgun-twitter]: https://twitter.com/logloggames
[bitgun-discord]: https://discord.gg/XrGZQkq
[bitgun-godot-rust]: https://godot-rust.github.io/
[bitgun-egui]: https://github.com/emilk/egui
[bitgun-godot-egui]: https://github.com/setzer22/godot-egui
[bitgun-inventory]: https://twitter.com/LogLogGames/status/1444072221681635333

### [Weegames][weegames-itch]

![Handful of minigames including hedgehogs and raspberries](weegames.jpg)

[Weegames][weegames-itch] is a fast-paced minigame collection.
The Windows version of the game has been rewritten to use Macroquad,
so now the web and downloadable versions of the game share the same codebase.
Development for the web version has moved to the
[Weegames Github][weegames-github] repository.

[weegames-itch]: https://yeahross.itch.io/weegames
[weegames-github]: https://github.com/yeahross0/weegames

### [Veloren][veloren]

![An odd structure in the woods](veloren.jpg) _An odd structure in the woods_

[Veloren][veloren] is an open world, open-source voxel RPG inspired by Dwarf
Fortress and Cube World.

In September, Veloren hosted its larges release party ever! At peak, 181 players
were playing on the server together. You can read about all the changes to 0.11
in [the release blog][veloren-011-release-blog], and be sure to watch the
[release trailer][veloren-011-trailer]! During the release party, several devs
spoke about the changes, which you can watch [here][veloren-011-dev-chats]. This
release party was the first one to handle the high player load with no issues,
and give hope for much larger servers in the future.

Shaderc was replaced with Naga early on in the month. This was the result of
over a year of work. Hitboxes are in the process of being overhauled to handle
non-cylidrical targets better. Improvements were made to how the cursor selects
objects in game. As always, lots of experiemental work is being done to the
economic system. Cultist raiders were added, which mean that raiding parties
will now attack nearby settlements. This is a great example of how the realtime
simulation is starting to become more visible to players.

September's full weekly devlogs: "This Week In Veloren...":
[#136][veloren-136],
[#137][veloren-137],
[#138][veloren-138],
[#139][veloren-139].

[veloren]: https://veloren.net
[veloren-136]: https://veloren.net/devblog-136
[veloren-137]: https://veloren.net/devblog-137
[veloren-138]: https://veloren.net/devblog-138
[veloren-139]: https://veloren.net/devblog-139
[veloren-011-trailer]: https://www.youtube.com/watch?v=l1oOjvaWJlw
[veloren-011-dev-chats]:https://www.youtube.com/watch?v=J5Xz-vbE27Q
[veloren-011-release-blog]: https://veloren.net/release-0-11/

### [Harvest Hero Origins][hho] @ PAX West 2021

![hho @ pax](hho_pax.jpg)
_Gemdrop Games booth at PAX West 2021_

[Harvest Hero Origins][hho]
([Discord](https://discord.gg/CJRbxQn3d9),
[Twitter](https://twitter.com/GemdropGames))
is an arcade wave defense game by [Gemdrop Games][gemdrop],
built in Rust on top of [Emerald].

Gemdrop Games recently took Harvest Hero Origins to [PAX West 2021][hho_pax]
and had a very positive response from most of the players!
Being able to watch people play the game was extremely valuable,
the developers were able to see pain points in UI/UX design
and can now fix them without worry.
They were also able to see what players find fun about controlling each hero,
which helps with the next hero planning in the full release of the game.

Harvest Hero Origins is still planned to release by the end of 2021,
please wishlist it on [Steam][hho]!

[Emerald]: https://github.com/Bombfuse/emerald
[gemdrop]: https://twitter.com/GemdropGames
[hho]: https://store.steampowered.com/app/1651500/Harvest_Hero_Origins
[hho_pax]: https://twitter.com/GemdropGames/status/1433819047481659394

### Molecoole

![Connecting to different atoms](molecoole_first.gif)

Molecoole is a topdown action roguelite where you connect with different atoms
to create the strongest Molecoole to defeat the baddies! Molecoole was created
by two brothers: [Márton] and [Dániel].

In Molecoole the strongest focus is about making different combos by connecting
atoms. The original version was made in Unity for a game jam, but they decided
to make an actual game out of it using the Bevy engine. It currently includes
their own implementation for 2D animation, collision detection, and particles.
In September, one of the main development areas was making the game nicer to
play, so they introduced the [ezing] crate and also implemented slowing the
[game time]. They are using the [LDtk] editor to make the level sections for the
procedural generation.

[Márton]: https://twitter.com/kiss_mrton
[Dániel]: https://twitter.com/FrenetiqDan
[ezing]: https://github.com/michaelfairley/ezing
[game time]: https://twitter.com/kiss_mrton/status/1434189320865341444
[LDtk]: https://ldtk.io

## Engine Updates

### [good-web-game]

![supported platforms](supported_platforms.svg)

[`good-web-game`] has been released on crates.io, together with [`ggez`] 0.6.1!
`ggez` is a lightweight cross-platform game framework for making 2D games
with minimum friction, with an API inspired by Love2D. `good-web-game` is a
subset of ggez, which is based upon [`miniquad`] and can therefore run natively
on the web, mobile and of course desktop as well.

`good-web-game` was originally created to run [Zemeroth] on the web. However,
as Zemeroth switched from using `ggez` to [`macroquad`] the project was
discontinued, until recently. In search of [a new graphics backend for ggez]
the ggez team now picked up development again and released a massive update,
updating `good-web-game` for compatability to `ggez` 0.6, expanding its
functionality.

With only [a single change in boilerplate code] many `ggez` 0.6 games can now be
directly ported to `good-web-game`. Yet, it's no drop in replacement for `ggez`
as [several key differences remain].

[good-web-game]: https://github.com/ggez/good-web-game
[`good-web-game`]: https://github.com/ggez/good-web-game
[`ggez`]: https://github.com/ggez/ggez
[`miniquad`]: https://github.com/not-fl3/miniquad
[Zemeroth]: https://ozkriff.itch.io/zemeroth
[`macroquad`]: https://github.com/not-fl3/macroquad/
[a new graphics backend for ggez]: https://github.com/ggez/ggez/issues/962
[a single change in boilerplate code]: https://github.com/PSteinhaus/PSteinhaus.github.io/blob/main/ggez/web-examples/README.md#ggez-animation-example
[several key differences remain]: https://github.com/ggez/good-web-game#differences

### [godot-rust](https://github.com/godot-rust/godot-rust)

![godot-rust logo](godot-rust.png)

godot-rust ([GitHub][gd-github], [Discord][gd-discord], [Twitter][gd-twitter])
is a Rust library that provides bindings for the Godot game engine.

In the last month, a lot of documentation has been added to the book. The new
entries in [FAQ][gd-faq], [Recipes][gd-recipes] and [Game Architecture][gd-arch]
don't focus on specific APIs, but put them into a bigger context and highlight
typical challenges encountered in practice.

Besides smaller bugfixes, the library itself added support for `serde`
serialization of core types ([#743][gd-743], thanks to Waridley).

In terms of automation and tooling, September was a very productive month:

- Translation of Godot's documentation based on `[bbcode]` to RustDoc with
  intra-doc links, making Godot APIs much more readable and discoverable.

- Refactoring of GitHub Actions CI, allowing quick and precise feedback for
  contributors.

- Automation of latest documentation, now hosted under
  [godot-rust.github.io/docs][gd-docs].

As the godot-rust community keeps growing, the project can now be found
[on Twitter][gd-twitter] with the GodotRust handle.

[gd-faq]: https://godot-rust.github.io/book/faq.html
[gd-recipes]: https://godot-rust.github.io/book/recipes.html
[gd-arch]: https://godot-rust.github.io/book/gdnative-overview/architecture.html
[gd-743]: https://github.com/godot-rust/godot-rust/pull/743
[gd-docs]: https://godot-rust.github.io/docs
[gd-github]: https://github.com/godot-rust/godot-rust
[gd-discord]: https://discord.com/invite/FNudpBD
[gd-twitter]: https://twitter.com/GodotRust

### [Emerald]

![hotreload](emd_texture_hotreload.gif)
_Built in texture hot reloading, just call `emd.loader().hotreload()`_

[Emerald] by [@bombfuse][bombfuse_twi]
is a 2D game engine focused on being super portable and easy-to-use.

Currently supported platforms are:
Windows, Linux (WIP gamepad support), macOS (WIP gamepad support),
Web, Android (WIP audio, gamepad Support),
[GameShell](http://imgur.com/a/8cWxOPs),
and even [WearOS](https://twitter.com/bombfuse_dev/status/1444100458260299778)!

Recently added features include:

- Texture hot reloading (sound hot reloading is coming soon!).
- Cross-platform file saving/loading.
  This is essential for games, basically allows the user to save
  their files to the platform specific save directory.

[Emerald] has slowly been growing, both in contributor size and feature sets
recently. If any of this interests you and you'd like to contribute,
[feel free to grab a task](https://github.com/Bombfuse/emerald/issues),
fork and PR!

[Emerald]: https://github.com/Bombfuse/emerald
[bombfuse_twi]: https://twitter.com/bombfuse_dev

### [Starframe]

![physically-connected groups of primitives are framed with rectangles](starframe-islands.jpeg)
_Grouping bodies into disjoint "islands"_

[Starframe] by [@moletrooper] is a work-in-progress game engine for physics-y
sidescrolling 2D games.

This month, a lot of work was done on optimizing the physics engine.
Most importantly, [spatial partitioning was added][sf-grid-tweet] to speed up
collision detection. Also notably, [a graph algorithm was
implemented][sf-island-tweet] to divide the world into disjoint islands,
enabling some parallelism and skipping of computations.

Starframe's physics is now very close to game-ready, and it no longer makes
sense to work on the engine without a concrete project to use it.
Thus, work has begun on a platformer based around connecting things with ropes.
More details to be shown soonish!

[Starframe]: https://github.com/MoleTrooper/starframe/
[@moletrooper]: https://twitter.com/moletrooper
[sf-grid-tweet]: https://twitter.com/moletrooper/status/1432441648890449920
[sf-island-tweet]: https://twitter.com/moletrooper/status/1438877808412008450

## Learning Material Updates

## Tooling Updates

## Library Updates

### [wgpu]

![Deno with wgpu crown](deno-wgpu.png)
_deno-wgpu_

[wgpu] is a cross-platform, safe, pure-rust graphics API that runs natively
on Vulkan, Metal, D3D12, D3D11, and OpenGLES; and on top of WebGPU on wasm.

wgpu has set up the infrastructure to run WebGPU proper tests on its CI,
via [Deno]. This will ensure correctness down the road when we reach a
decent level of coverage. Read more on [gfx-rs blog].

Aside from that, wgpu team has been pumping out patches. In fact, wgpu-0.10 is
easily the most patched release of all!

_Discussions:
[/r/rust](https://reddit.com/r/rust/comments/ppgb2l/wgpu_alliance_with_deno),
[Twitter](https://twitter.com/deno_land/status/1438573126670028801)_

[wgpu]: https://github.com/gfx-rs/wgpu
[Deno]: https://github.com/denoland/deno
[gfx-rs blog]: https://gfx-rs.github.io/2021/09/16/deno-webgpu.html

### [Matchbox]

![matchbox demo screenshot: Waiting for 3 more players](matchbox.png)

Matchbox by [@jkhelsing] is a new peer-to-peer networking project for
establishing unreliable, unordered connections between peers on the internet.
The goal is to enable low-latency multiplayer games written in Rust WASM.

Matchbox consists of:

- A tiny signalling server, [`matchbox_server`], which acts as a rendezvous
  point. It helps peers discover each other and deal with NAT traversal in order
  to establish more direct ways of communication.
- A crate, [`matchbox_socket`], which handles connecting to a signalling server
  and establishing a WebRTC data channel between each connected peer.
- A [demo/template project][matchbox_demo] using [Bevy](https://bevyengine.org)
  and [GGRS] to implement a web game with peer-to-peer rollback netcode. A live
  version is hosted [here][helsing_box_game].

More info is available in the [repository][Matchbox] and
[introductory blog post][matchbox_intro].

_Discussions:
[/r/rust](https://reddit.com/r/rust/comments/pmsynh/introducing_matchbox_painless_peertopeer_webrtc),
[twitter](https://twitter.com/jkhelsing/status/1437044006068830215)_

[Matchbox]: https://github.com/johanhelsing/matchbox
[matchbox_intro]: https://johanhelsing.studio/posts/introducing-matchbox
[`matchbox_socket`]: https://crates.io/crates/matchbox_socket
[`matchbox_server`]: https://crates.io/crates/matchbox_server
[matchbox_demo]: https://github.com/johanhelsing/matchbox/tree/main/matchbox_demo
[helsing_box_game]: https://helsing.studio/box_game
[@jkhelsing]: https://twitter.com/jkhelsing
[GGRS]: https://gschup.github.io/ggrs

### [Sparsey]

[Sparsey] by [@LechintanTudor] is a new sparse set-based Entity Component System
(ECS) with component storage grouping, granular component change detection,
fallible systems and beautiful syntax.

The goal of [Sparsey] is to provide a sparse set-based ECS which fully takes
advantage of its core data structure. An example of this is component storage
grouping, a feature which allows getting the best performance possible when
iterating over queries which match certain patterns described by the user, at
the cost of a performance penalty when inserting or removing components from
these storages.

To get started with [Sparsey], check out the [Sparsey Cheat Sheet] and the
[examples on GitHub]!

[Sparsey]: https://github.com/LechintanTudor/sparsey
[@LechintanTudor]: https://github.com/LechintanTudor
[Sparsey Cheat Sheet]: https://github.com/LechintanTudor/sparsey/blob/master/guides/cheat_sheet.md
[examples on GitHub]: https://github.com/LechintanTudor/sparsey/tree/master/examples

### [bevy_verlet]

![bevy_verlet](bevy_verlet.gif)

[bevy_verlet] is a lib for projects using [Bevy Engine][bv_bevy]
providing a plugin to use [verlet Integration][bv_wikipedia]
physics. Very useful for Cloth simulation and joints, and less expensive than
complex physics engine, it is a nice addition to 2D or 3D projects. Making good
use of the Entity-Component-System architecture of the bevy engine, any entity
can become a `VerletPoint` and have physics applied to it.

The crate also provides *sticks* which constrains the points in order to create
strings or cloth. With its modularity, you may customize the physics precision
(iterations), the gravity, and the physics time step to use.

Not yet available on crates.io, the lib will be released after a few missing
features are provided:

- Primitive collision
- Object batching (optimization)
- Global documentation

You may contact the author on Twitter [@ManevilleF][ManevilleF] or join the
[discussion][bv_discussion].

[bevy_verlet]: https://github.com/ManevilleF/bevy_verlet
[bv_discussion]: https://twitter.com/ManevilleF/status/1437350669858611202?s=20
[ManevilleF]: https://twitter.com/ManevilleF
[bv_bevy]: https://bevyengine.org/
[bv_wikipedia]: https://en.wikipedia.org/wiki/Verlet_integration

## Popular Workgroup Issues in Github

<!-- Up to 10 links to interesting issues -->

## Meeting Minutes

<!-- Up to 10 most important notes + a link to the full details -->

[See all meeting issues][label_meeting] including full text notes
or [join the next meeting][join].

[label_meeting]: https://github.com/rust-gamedev/wg/issues?q=label%3Ameeting

## Requests for Contribution

<!-- Links to "good first issue"-labels or direct links to specific tasks -->

## Jobs

<!-- An optional section for new jobs related to Rust gamedev -->

## Bonus

<!-- Bonus section to make the newsletter more interesting
and highlight events from the past. -->

<!-- TODO: browse previous newsletter coord-issues and select some cool section
that wasn't written. -->

------

That's all news for today, thanks for reading!

Want something mentioned in the next newsletter?
[Send us a pull request][pr].

Also, subscribe to [@rust_gamedev on Twitter][@rust_gamedev]
or [/r/rust_gamedev subreddit][/r/rust_gamedev] if you want to receive fresh news!

<!--
TODO: Add real links and un-comment once this post is published
**Discuss this post on**:
[/r/rust_gamedev](TODO),
[Twitter](TODO),
[Discord](https://discord.gg/yNtPTb2).
-->

[/r/rust_gamedev]: https://reddit.com/r/rust_gamedev
[@rust_gamedev]: https://twitter.com/rust_gamedev
[pr]: https://github.com/rust-gamedev/rust-gamedev.github.io