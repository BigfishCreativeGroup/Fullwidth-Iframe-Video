# Fullwidth Iframe Video 
A code snippet used for displaying a fullwidth iframe video within a content area. For a full explanation read <a href="http://www.alistapart.com/articles/creating-intrinsic-ratios-for-video/" target="_blank">Creating Intrinsic Ratios for Video</a> by Thierry Koblentz.

<a href="http://biz4riz.com/development/github-projects/fullwidth-iframe-video/">View Demo</a>

<h3>Styles</h3>
```html

// The Container

.video.full {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 aspect ration */
  padding-top: 25px;
  height: 0;
}

// The Iframe

.video.full iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
```

The .video.full container is positioned relative to proportionally resizes itself depending on the width of its parent. The classes .video and .full are separated in case there is are video elements within the same site or webpage that may share like styles without being fullwidth.

The iframe is positioned absolute and given a height and width of 100% to fill the content area of the parent .video.full element.

<h3>HTML</h3>
```html
<div class="video full">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/XQu8TTBmGhA" frameborder="0" allowfullscreen></iframe>
</div>
}
```
The height and width attributes of the iframe will be overwritten by the iframe height and width declarations within the styles.

