# Research into delivering video through the web

My research into delivering video through the web. This documentation will go through the various methods and means of
video delivery. With focus on a best delivery method, with good balance on bitrate (data throughput) and quality.

## The basics (HTML5 video tag)

HTML5 introduced the `video` tag where you specify plain ol' video files and they are played by the browser if the
browser supports the format i.e. codec and container.

Example usage:

```html
<video poster="poster.jpg" controls>
    <source src="movie.webm" type="video/webm">
    <source src="movie.mp4" type="video/mp4">
    <p>Your browser does not support the video tag.</p>
</video>
```

[read more](docs/html5-video.md)

## Media queries

Because this research focuses on delivering the appropriate video regarding to size and bandwidth, then we build on top 
of the basic HTML5 video with media queries which does not seem to be all that common usage.

[read more](docs/media-queries.md)

## HTTP Live Streaming (HLS)

Deliver video natively, of multiple resolution variants, "easily" on the web with the `<video>` tag 
or as Apple describes it

> Send live and on‐demand audio and video to iPhone, iPad, Mac, Apple TV, and PC with HTTP Live Streaming (HLS) 
> technology from Apple. Using the same protocol that powers the web, HLS lets you deploy content using ordinary 
> web servers and content delivery networks. HLS is designed for reliability and dynamically adapts to 
> network conditions by optimizing playback for the available speed of wired and wireless connections.

[read more](docs/hls.md)

## JavaScript

Use JavaScript to enhance the users experience and/or provide more support for end clients.

Not all browser support HLS or MPEG-DASH but may support the segments produced by those protocols by using JavaScript
we can enable playback of such media even if they are not supported natively in the browser.
Along with new features or custom video control interface.

[Video.js](https://videojs.com) is the most predominant JavaScript framework which supports these features and more.

[read more](docs/javascript.md)
