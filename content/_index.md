+++
title = "Hoem Paeg"
[extra]
no_header = true
+++

<div class="container-fill">
  <img id="logo" class="has-alpha drop-shadow" src="logo.svg" alt="VTuber-style Ametrine logo.">
  <small class="center">unofficial starter template</small>

  <div class="buttons centered big">
    <a class="suggested" href="https://github.com/backups1der/ametrine-starter-template">Template repository →</a>
    <a href="https://codeberg.org/daudix/ametrine">Theme repository →</a>
  </div>
  
  [Ametrine](https://en.wikipedia.org/wiki/Ametrine) is a "one of a kind" [Zola](https://www.getzola.org) theme made specifically for personal websites and blogs. It provides good defaults and easy configuration, while being somewhat flexible on demand. Its design is unique and made with great care and attention to details, it changes from time to time, and the development pace is rather rapid.

  This unofficial[^1] starter template for Ametrine provides the most basic settings for new people; let it be configuration in `zola.toml` or some example pages to show how to make new pages and use Ametrine's features.
  [^1]: I, [anins1der](https://anins1der.com), made this template for this theme because... no one did it? It was along the lines of that. Good news is that official author of this theme, [Daudix](https://daudix.one), is [making a official starter template](https://codeberg.org/daudix/ametrine/issues/64) because [welpo](https://osc.garden) did so with his theme, [tabi](https://github.com/welpo/tabi-start).
</div>

> [!CAUTION]
> Ametrine is currently in the pre-alpha state and **_SHOULD NOT_** be used in production, it is not ready yet. Version 0.1.0 is on its way and should be released sometime soon, along with a migration guide from [Duckquill](https://duckquill.daudix.one) for people that were on Duckquill theme. See [v0.1.0 To-do](https://codeberg.org/daudix/ametrine/issues/3).

> [!NOTE]
> Ametrine **only targets the latest Zola version** available at a given moment, backwards compatibility might be absent, and issues regarding it will be dismissed. This is to keep Ametrine's code easier to maintain (it's already hard to maintain as is for the author).


Some of Ametrine's features:

- Handwritten CSS (Sass); no Tailwind, React, or anything like that.
- No essential JavaScript; pop-ups, sidebars, and such will work just fine without it.
- Relatively lightweight, weights under 512kB.
- Uses modern CSS.
- Includes Monokai Pro theme for syntax highlighting out of the box.
- Will make you regret using this theme.
  - Maybe. It has made poeple love this theme --- a crazy guy has made this template for a reason.

## What Is This Again

This is a theme for the [Zola](https://www.getzola.org) static site generator; thingy that converts [Markdown](https://www.markdownguide.org) files (which is used by Reddit, Tumblr, Discord, any many others) into a fully functional websites. Zola cannot build websites without a set of templates and styles, and this theme is exactly that. Ametrine also provides some custom functionality that is not present in Zola, such as Mastodon-powered comments, various useful shortcodes for simplifying various tasks, and more.

You can learn more about Zola and its themes at <https://www.getzola.org>.

## Maintenance & References
> [!IMPORTANT]
> I am going to assume that you have enough knowledge to either use Git from CLI or your preferred editor's Git integration, have enough experience to operate your projects on GitHub. You can have Zola set up on your machine to get live previewing; but it's not exactly required to use with this template since the build workflow installs Zola and builds your website automatically, publishing it to current repository's [GitHub Pages](https://docs.github.com/pages) page.
>
> Don't worry, all of these are easy to learn: you don't need to use much brainpower to figure out how to use Git in VSCode/Zed. Zola provides [installation instructions](https://www.getzola.org/documentation/getting-started/installation/), so you should be able to get that on your system pretty easily.

To update Ametrine, simply update the theme submodule to the latest commit:

```bash
git submodule update --remote themes/ametrine
```
> [!IMPORTANT]
> Check the [commit history of Ametrine](https://codeberg.org/daudix/ametrine/commits/branch/main) before updating; there may be breaking changes that require manual involvement.

Ametrine has it's own [demo](https://ametrine.daudix.one/demo) page which shows off some features. You can also check the [CommonMark specification page](https://spec.commonmark.org), where it lists what CommonMark can do.

## Development

There is a `serve.sh` file on root of the project, that sources .env file and serves the website:


```crt=true
rd@lappy ~/Projects/awsum-website (main)> ./dev.sh serve --drafts --open
   _             _       _          
  /_\  _ __  ___| |_ _ _(_)_ _  ___ 
 / _ \| '  \/ -_)  _| '_| | ' \/ -_)
/_/ \_\_|_|_\___|\__|_| |_|_||_\___|
                                    
Building site...
-> Creating 16 pages (2 orphan) and 3 sections
Done in 6.5s.

Listening for changes in /home/rd/Projects/awsum-website/{config.toml,content,sass,static,templates}
Press Ctrl+C to stop

Web server is available at http://127.0.0.1:1111 (bound to 127.0.0.1:1111)
```

## Why It Looks the Way It Does

> Personally, I'm sick of flat, sterile, dead UIs all over the place, and I've always liked skeuomorphism because it's fun, alive, and pleasant to look at. While it's not very feasible to make things look overly realistic, some edge highlights, nice shadows, and a vibrant palette make a big difference. The design system that Ametrine uses is made of slightly frosted colored acrylic, everything is rounded, but the edges are not so rounded, so the edge highlight is rather thin, you can think of it as Lego bricks, fun and nice to touch. The animations are very bouncy to raise the fun level even higher. Still, the balance between fun and not being annoying is maintained. Did I succeed with this premise? I don't know, you tell me :P

-- [Daudix](https://daudix.one), author of [Ametrine](https://codeberg.org/daudix/ametrine)

## To-Do

As of right now, Ametrine is not ready to be used in production and is in active development, here's a roadmap of features that need to be implemented, issues to be fixed, and things to be rewritten before the initial release: <https://codeberg.org/daudix/ametrine/milestone/12016>. <small>(asking daudix "v0.1 when" won't make the process any faster, I want to release it <abbr title="as soon as possible">ASAP</abbr> just like you do)</small>


<style>
  #logo {
    width: min(calc(var(--content-width) / 1.5), 100%);
    
    opacity: 1;
    filter: none;
    scale: 1;
    transform: none;
    
    transition: var(--transition-bezier-longer);

    @starting-style {
      opacity: 0;
      filter: blur(2.5rem);
      scale: 0;
      transform: translateY(-5rem);
    }
  }

  #logo:hover {
    transform: var(--hover) rotate(-3.5deg) translateY(-8px);
  }
</style>