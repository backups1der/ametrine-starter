+++
title = "Blog"
description = "Love myself some description here"
sort_by = "date"
template = "article_list.html"
page_template = "article.html"
paginate_by = 4
generate_feeds = true
[extra]
no_header = true
+++

```crt=true
*        *                 *      ## ## ## #### #    *               *
                                  `######""`          *            ___
                        *         /##/                       |     | |
  *               *               .*                        / \    | |
        *              _________##                 *       |--o|   | |
                      @\\\\\\\\\##    *     |              |---|===|-|
  *                  @@@\\\\\\\\##\       \|/|/           /     \  | |
                    @@ @@\\\\\\\\\\\    \|\\|//|/     *  |  S    | | |
             *     @@@@@@@\\\\\\\\\\\    \|\|/|/         |  N    | | |
                  @@@@@@@@@----------|    \\|//          |  U    |=| |
       __         @@ @@@ @@__________|     \|/           |  G    | | |
  ____|_@|_       @@@@@@@@@__________|     \|/           |_______| |_|
=|__ _____ |=     @@@@ .@@@__________|      |             | | | |  | |
____0_____0__\|/__@@@@__@@@__________|_\|/__|___\|/__\|/___________|_|_
```

# Blog

Hi, welcome to the demo blog, filled to the brim <small>(not really)</small> with all kinds of "different" exciting demo posts.

Blog page itself works a little bit different compared to other pages:
- It has a list of articles (or <abbr title="BLOg poST">*blost*s</abbr> in the context of blogging) below the content of the page, which are sorted by date and dynamically tiled according to width of this tab. 
- This page disables the header, so that the title gets hidden and only controls the small title up on the top and social medis embeds. Then we put a H1 header for nicer look.
- The articles are paginated. You can change the number of articles per page by changing `paginate_by` variable in this file's frontmatter. We recommend setting this to a even value so posts just don't get "cut off".