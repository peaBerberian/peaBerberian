### Hi there 👋, I'm Paul Berberian

I'm a senior software developer mostly working on libraries implementing technical aspects needed by front-end web applications.

Right now, I'm the lead developer of the open-source [RxPlayer](https://github.com/canalplus/rx-player) project at Canal+, a featureful adaptive media player library targeted to important streaming actors. It implements the technical core building block of a streaming media player (particularly media standards, such as the DASH and Smooth streaming protocols) and can then be integrated into a separate player UI, which is generally directly developed by the various companies freely relying on the project.<br>

My current languages of choice are: <img height="15px" src="https://upload.wikimedia.org/wikipedia/commons/4/4c/Typescript_logo_2020.svg"></img> TypeScript, <img height="15px" src="https://upload.wikimedia.org/wikipedia/commons/9/99/Unofficial_JavaScript_logo_2.svg"></img> Javascript, <img height="15px" src="https://upload.wikimedia.org/wikipedia/commons/0/0f/Original_Ferris.svg"></img>  Rust and <img height="15px" src="https://cdn.worldvectorlogo.com/logos/golang-gopher.svg"></img> Go.<br>
I also like combining several of those languages on the web by relying on <img height="15px" src="https://upload.wikimedia.org/wikipedia/commons/1/1f/WebAssembly_Logo.svg"></img> WebAssembly.

Besides the RxPlayer, I work on multiple other open-source projects: some big some very small and many of which are available here on GitHub. Among which (all of those listed projects are functional):

  - :honeybee: [Wasp-hls](https://github.com/peaBerberian/wasp-hls): A WebAssembly-based, in-worker, HLS media player.<br>
     This is an ambitious personal project where I attempt to use the latest API and technologies (MSE-In-Worker, WebAssembly) to construct an optimal adaptive media player: not blocked by main thread interactions, low-on-memory, performant, low-latency.<br>
     This is still heavily in development. Most live and VoD contents can be played but there's still a lot of features to come!

  - :chart_with_upwards_trend: [RxPaired](https://github.com/peaBerberian/RxPaired): A lightweight remote debugger.<br>
	I wrote it to simplify debugging sessions observing the RxPlayer's behavior. It works on any device with a very minimal performance imprint and is used daily by several teams at Canal+.

  - :eyeglasses: [MSESpy](https://github.com/peaBerberian/MSESpy.js) and [EMESpy](https://github.com/peaBerberian/EMESpy.js), spying libraries used for reverse engineering what [MSE](https://www.w3.org/TR/media-source-2/) and [EME](https://www.w3.org/TR/encrypted-media/) web APIs any webpage is calling, when, and with which parameters.<br>
    Those tools were written to reverse engineer how other streaming actors' own players were behaving in different situations, in turn to improve our own. My team and I still use it for that same usage. 
   
  - 📹 [AISOBMFFWVDFBUTFAII](https://github.com/peaBerberian/AISOBMFFWVDFBUTFAII): Basically an inspector of MP4 files (more technically, it tries to inspect all [ISOBMFF](https://en.wikipedia.org/wiki/ISO/IEC_base_media_file_format)-compatible formats).<br>
    Written initially as a personal project to improve my understanding of the format, it is now actually used at my work by different teams to easily inspect those files.
    
  - 🏇 [gif-renderer.rs](https://github.com/peaBerberian/gif-renderer.rs): A gif decoder written in Rust.<br>
    I wrote it to continue improving my Rust skills, it is finished and functional and is able to efficiently display all (87a and 89a) GIF files.

  - :page_facing_up: [str-html](https://github.com/peaBerberian/str-html): A simple JS UI tool generating `HTMLElement` by relying on tagged template literals.<br>
    This tool can be used as a fairly simple UI lib for JS applications, leading to very readable component code without having to bring e.g. JSX into the picture. I wrote this one as a nice spot for when whole UI frameworks like React were overkill yet using "vanilla" HTML API became unreadable.

  - ⌨️ [RKeyboard](https://github.com/peaBerberian/RKeyboard): A functional proof of concept to provide a new way to handle complex keyboard and/or remote control interactions.<br>
    It was written while creating the initial skeleton of the next Canal+ front-end application for its set-top boxes. At its core, it creates a hierarchy of key handlers, a stack on which you can push and pop to respectively catch a key or let the parent catch it again. 
     
  - 🐭 [morora.js](https://github.com/peaBerberian/morora.js): A sister project to `RKeyboard`, `morora.js` is a small library which handle spatial navigation for devices without a mouse.<br>
    This project was written like `RKeyboard` when working on proof of concepts for a new set-top-box's user interface, where no pointer/mouse is available. It allowed experimentations on which strategy to adopt for page navigation: closest selectable element first? What if the next elements are not aligned? What if multiple elements are at the same distance? etc.

  - 🖼️ [BIF-Inspector](https://github.com/peaBerberian/bif-inspector): A simple tool to parse and inspect BIF files, the archive file format used by most streaming actors for preview thumbnails (e.g. to preview video content before a seek in a media).<br>
    This was initially written to help teams working with us to produce spec-compliant BIF files.

  - 🗒️ [quick-xml](https://github.com/peaBerberian/quick-xml): A fork of the rust crate of the same name updated to handle temporary [BufRead](https://doc.rust-lang.org/std/io/trait.BufRead.html) starvation (temporary Eof events).<br>
    This was done for WebAssembly-related reasons, while we were doing Proof Of Concepts for heavily improving the RxPlayer performance on devices which needs it.

  - ⏯️ [player-inspector](https://github.com/peaBerberian/player-inspector): Yet another reverse-engineering tool for media players on the web.<br>
    This one notably allows, by using it as an [userscript](https://en.wikipedia.org/wiki/Userscript), to visually inspect in real time what is pushed on the lower-level video buffers of most websites with video streaming (YouTube, Netflix, Amazon Prime Video, Twitch, Canal+, Disney+ and so on...).
    
  - 📖 [README](https://github.com/peaBerberian/README): A simple (in a KISS way) documentation generator taking as input fully CommonMark-compatible Markdown files.

    The goal is to keep the original documentation files readability in a text-editor (as intended by the Markdown format) as well as on Github's interface, without any specific modification on them, while still providing a richer web version with minimal efforts, here by adding simple `.docConfig.json` JSON files alongside documentation files.
    
  - :key: [passgen](https://github.com/peaBerberian/passgen): A very simple online client-side password generator.
    
  - 🎮 [roguelike_test.rs](https://github.com/peaBerberian/roguelike_test.rs): As its name subtly suggest, this is a very simple roguelike (following the [Berlin interpretation](http://www.roguebasin.com/index.php/Berlin_Interpretation) of the genre) implementation in Rust.<br>
    It was is written with the help of the [tcod](https://github.com/tomassedovic/tcod-rs) library to handle inputs, graphics and window management. Graphics are ASCII-based and minimal as they very often are in those traditional roguelikes, the main work being on the core logic and gameplay, here principally: procedural map generation, AI, field of view and interactions between objects.
         
   - 🐍 [Steve6502](https://github.com/peaBerberian/Steve6502): A snake implementation done in [6502](https://en.wikipedia.org/wiki/MOS_Technology_6502) assembly (used by the Atari 2600, the NES and the Commodore 64) with memory-mapped graphics.<br>
     This was done by initially following [the _Easy 6502_ tutorial](https://skilldrick.github.io/easy6502/) and then improving on it such as creating different apple colors, bringing more or less points.
     
  - 📦 [ZipDown.js](https://github.com/peaBerberian/zipdown.js): A simple server allowing to easily download directories zipped on-the-fly through HTTP.<br>
    I wrote it as a quick and simple personal project (the zipping logic itself is actually done by [archiver](https://www.npmjs.com/package/archiver), a npm module) to easily transfer a large number of files in a local network between devices with a browser.
    
   - 🦀 [isobmff-inspector.rs](https://github.com/peaBerberian/isobmff-inspector.rs): A Rust re-implementation of the `AISOBMFFWVDFBUTFAII` tool (higher on the list).<br>
     I wrote it to continue to learn Rust. It works as well as the other one, but is much less used due to not being web-based like the other.
     
   - ⚙️  [booth-mult](https://github.com/peaBerberian/booth-mult.rs): A very simple and minimal implementation of the [Booth's multiplication algorithm](https://en.wikipedia.org/wiki/Booth%27s_multiplication_algorithm).<br>
    This is a very small project in Rust, mainly done while learning the language.
    
   - 📁 [directory-list.php](https://github.com/peaBerberian/directory-list.php): A very minimal PHP script to list files and directories in the current directory.<br>
     This was written as a personal project to quickly allows loading files through HTTP from a server of mine.

   - 🚀 [wasm-game-of-life](https://github.com/peaBerberian/wasm-game-of-life): A straightforward [game of life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) implementation by using Rust and WebAssembly.<br>
     I wrote it while beginning to experiment with WebAssembly, by following the [wasm-game-of-life tutorial](https://rustwasm.github.io/docs/book/game-of-life/introduction.html).
     
   - 🏦 [GoBanks](https://github.com/peaBerberian/GoBanks): An expense manager API I wrote in Go.<br>
     It is functional, but I honestly don't use it anymore due to it missing a lot of features when compared to what is freely available elsewhere.
     
   - 🗞️ [GoFeeds](https://github.com/peaBerberian/GoFeeds): A simple RSS feed parser written in Go.<br>
     Like `GoBanks`, I wrote it to improve my Go skills, and also like it, I don't use it much anymore because others invested much more time on better solutions 😁 
     
   - 🕸️ [peaberberian.github.io](https://github.com/peaBerberian/peaberberian.github.io): A dead simple static site generator for my personal github page: https://peaberberian.github.io.<br>
     The point was to spent the minimum maintenance time on it and avoid using JavaScript at all (quite peculiar for a front-end web developer like me!).
<!--
**peaBerberian/peaBerberian** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
