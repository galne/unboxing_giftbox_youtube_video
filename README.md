# Unboxing GiftBox YouTube Video Embed

This repository contains a reusable HTML/CSS snippet that embeds a YouTube video  
for the *personalized wooden gift box unboxing*.  

The goal is to maintain the embed code in **one place** and reuse it across multiple blog articles.  
Whenever the YouTube video link changes, you only need to update the code here,  
and all blog posts that load this file via `<iframe>` will automatically show the new video.

---

## How it works
1. The file `giftbox.html` contains the embed code with all required styles.
2. GitHub Pages serves this file as a standalone page.
3. Blog articles include the embed with a simple `<iframe>`.

---

## Example Embed Code for Blog Articles

```html
<div class="fg-embed">
  <iframe
    src="https://galne.github.io/unboxing_giftbox_youtube_video/giftbox.html"
    title="Fairygift Gift Box"
    loading="lazy"
    referrerpolicy="no-referrer-when-downgrade"
    allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
    style="border:0;"></iframe>
</div>
<style>
  .fg-embed{position:relative;width:100%;max-width:680px;margin:0 auto}
  .fg-embed::before{content:"";display:block;padding-top:100%} /* 1:1 ratio */
  .fg-embed>iframe{position:absolute;inset:0;width:100%;height:100%;border-radius:16px;overflow:hidden}
</style>
