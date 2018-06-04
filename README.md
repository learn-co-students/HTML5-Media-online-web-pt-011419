# Working with HTML5 Media

## Problem Statement
The internet is a highly interactive environment. Even blogs where text
may be the most dominant content, audio and video elements often support,
or even supplement, the content. In the case of 3rd party media sites such
as YouTube, SoundCloud, and Vimeo, you are given an all-in-one line of code
with configurable properties that creates the embeddable content for you--
but how do you do this manually in your application? Often times, you will be working
with, and manipulating, media that is being uploaded into or generated by your
app. HTML has evolved dramatically since the days of the generic `embed` tag.
How is this done today?

## Overview
1. Demonstrate how to embed audio elements in HTML5
2. Demonstrate how to embed video elements in HTML5
3. Link to audio and video converters

## Demonstrate How to Embed Audio Elements in HTML5
Embedding audio can be a nice touch to a website. If you had a MySpace page back
in the 2000s, you can probably heavily relate to this. HTML was very different back
then. The HTML tags were not semantic, especially not for media, and it was less forgiving
to install. If you wanted to embed audio, you often times also needed to embed an audio 
player, which might have to be flash, java, or javascript based. If you did not, you 
could easily play audio with no way for the user to control it. This is no longer an
issue, as HTML5 has its own default media players supported in the browser.

We can do this now by including the <audio> element. Enclosed within the audio element are 
source elements that point to the location of various audio file formats. The reason we 
provide multiple source files is that not all browsers support both audio codecs required 
for playback. By providing both an MP3 file and an OGG file, we ensure that all browsers 
will be able to play the content. 

```
<audio controls>
  <source src="purrr.mp3" type="audio/mp3">
  <source src="purrr.ogg" type="audio/ogg">
  <p>Sorry your browser doesn't support HTML5 Audio! Please <a href="http://browsehappy.com/?locale=en">upgrade your browser</a>.</p>
</audio>
```

On the first line we open the `<audio>` tag with the controls attribute. This is required to 
display the audio controls to start and pause playback, adjust the recording's volume, etc. 
The presence of the `controls` attribute name itself is sufficient, no other properties are 
needed. There are optional attributes you can provide such as `autoplay` and `loop`, to start the 
song on page load, or to repeat the audio after it ends. For the full list of accepted attributes 
check out the [MDN documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio). 

Lines 2 and 3 we provide two different source files for playback. If the browser does not 
recognize the first filetype it will ignore it and move on to the next. If neither of 
the formats are supported it will instead display the paragraph on line 4. If the 
browser is able to play one of the source files it will ignore any other code 
below until it reaches the closing </audio> tag. For source we must set the src 
location of the file by providing the relative path to the file, and the type which 
clues the browser as to which audio codec is suitable for that particular filetype.

## Demonstrate How To Embed Video Elements in HTML5

Embedding a video is very similar to embedding audio. This can be done by including the `<video>`
tag. Inside the video tag are source tags that point to the location of various video file 
formats. The reason we provide multiple source files is that not all browsers support both 
video codecs required for playback. By providing either an MP4 (h264) and OGV, or MP4 (h264) 
and WEBM file, we ensure that all browsers will be able to play the content.

```
<video controls>
  <source src="real-estate.mp4" type="video/mp4">
  <source src="real-estate.ogv" type="video/ogg">
  <p>Sorry your browser doesn't support HTML5 Video! Please <a href="http://browsehappy.com/?locale=en">upgrade your browser</a>.</p>
</video>
```

Similarly to audio, we will open the `<video>` tag with the controls attribute. For 
the full list of accepted attributes, you can check the [MDN documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video) 
On lines 2 and 3 we provide two different source files for playback. If the browser 
does not recognize the first filetype it will ignore it and move on to the next 
just the same as it does for the audio element. If neither of the formats are 
supported it will display the paragraph instead on line 4. If the browser is 
able to play one of the source files it will ignore any other code below 
until it reaches the closing </video> tag. We must use src to specify a 
relative path to the location of the file and type to tell the browser 
which video codec is suitable.

## Link to Audio and Video Converters
There are a number of free tools that will convert audio files when needed. 
See the following resource links for a few recommended free audio and video 
converters you can use to change one file type to another. This is helpful 
to create both source file types needed.
- [Presentation Slides](https://docs.google.com/presentation/d/1R2usO7eha-xvU6McOYjR8n2papGK-gzW_LwO4AM5NTA/edit?usp=sharing)
- [Audacity - Free Audio Editor/Converter](https://sourceforge.net/projects/audacity/)
- [MediaHuman - Free Audio Converter](http://www.mediahuman.com/audio-converter/)
- [JavaScript HTML5 Video Player Comparison](https://praegnanz.de/html5video/)

## Conclusion

In the past, it may have been a little more challenging to understand how to
embed media files into websites. With the HTML5 `audio` and `video` tags, you
are empowered to have the functionality needed for display these elements and 
other fallbacks built right into the browser for your convenience with a few 
lines of code. 
