---
title: "A Beginner’s guide to download any (almost) video on the internet."
datePublished: Mon Aug 21 2023 03:30:13 GMT+0000 (Coordinated Universal Time)
cuid: cllkbk4ge000109m9fzsvce5t
slug: download-any-video
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1681331656934/02571102-20e0-4c1e-bd77-c7fa1d8c5fa7.png
tags: youtube, youtube-dl, python-libraries, wemakedevs, yt-dlp

---

## Introduction

**Yt-dlp** is a command-line program used to download videos from the internet, including websites like Facebook, Instagram, LinkedIn, Twitch, Vimeo, YouTube, Twitter, TikTok, Reddit, and 1000 others<sup>[</sup>[<sup>1</sup>](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md)<sup>]</sup>.

While there are many ways to download internet videos, most of them are filled with ads and/or don't provide many features.

**Yt-dlp** is safe to use and packs various features that enable you to download playlists and extract the audio file from a video using '**FFmpeg**', a Yt-dlp dependency.

## History

Yt-dlp is a popular fork(version) of the now inactive YouTube-dl repository on GitHub with 119K stars that supports additional features and bug fixes. YouTube-dl has been inactive since December 2021, and since then, *yt-dlp* has seen significant growth in its usage and it was included in Ubuntu's 22.04 version release.

YouTube-DL, launched by **Ricardo Garcia** in 2006, initially only supported downloading videos from YouTube. Over the years, many maintainers for the project have changed, and it now supports more video-sharing websites.

On October 23rd, 2020, it was taken down by GitHub upon a request from the **Recording Industry Association of America (RIAA)** under the **Digital Millennium Copyright Act (DMCA)**, stating that it violates many copyright issues in the United States and the EU by bypassing YouTube’s *rolling cypher* protection that was meant to stop third parties from accessing the videos hosted on its platform.

Furthermore, YouTube-DL **doesn't violate any act that was mentioned by the RIAA**, and on top of that, it helps many users in downloading Creative Commons-licensed or public domain videos, and GitHub chose to reinstate YouTube-DL<sup>[</sup>[<sup>2</sup>](https://github.blog/2020-11-16-standing-up-for-developers-youtube-dl-is-back/)<sup>]</sup>.

## Working

> While it's unsure how the 'rolling cypher' works on YouTube, according to a document released by The Electronic Frontier Foundation<sup>[</sup>[<sup>3</sup>](https://github.com/github/dmca/blob/master/2020/11/2020-11-16-RIAA-reversal-effletter.pdf)<sup>]</sup> on November 20, 2020, YouTube uses a mechanism called Signature to access the videos from their servers.
> 
> In short, YouTube sends a small JavaScript program to the user’s browser which is requesting a video, then it derives a sig value making it part of the URL and sends it back to YouTube's server to request the actual video. This entire process can be seen by anyone on YouTube’s source page without the need for any decryption methods.
> 
> YouTube-dL works the same way as a browser, it intercepts the JavaScript program and derives the sig value to make the video available for downloading<sup>[</sup>[<sup>4</sup>](https://news.ycombinator.com/item?id=24876321)<sup>]</sup>.

## Installation

### PIP

The easiest way to install *yt-dlp* on your computer is by using the ***pip*** package manager, which comes pre-installed with Python.

If ***pip*** is not there on your computer, even after installing Python, run the following in your command line interface to install it manually:

`python -m ensurepip`

Now, to install *yt-dlp* run,

`pip install yt-dlp`

### Github

Alternatively, you can download Yt-dlp straight from its GitHub repository. Go to the *yt-dlp's* GitHub [repository](https://github.com/yt-dlp/yt-dlp).

Now click on Download and select the operating system your machine is running on.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692570751778/d68ef0a3-da0f-4bbc-bc91-a11756ffaadd.png align="center")

Now click on ***Download*** and select your operating system.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692570830761/e82c0b3e-dfa9-4340-ab6a-f0909c2a3ab9.png align="center")

Similar to any other software that you install, you need to add its ***Bin*** folder (which essentially contains the executable files of the program) to the *path* of your system’s environment variables. If you are unsure of how to do it, a quick Google search can help you.

This allows your system to access these executable files globally, through which you can run the particular code from any interface.

If you have installed Yt-dlp using *pip*, it will automatically install the program in a directory that is already in your system’s environment variable path.

## Dependencies

Yt-dlp works perfectly out of the box, although it is highly recommended to download dependencies like ***FFmpeg*** and ***FFprobe***.

***FFmpeg*** is an open-source multimedia framework that contains ***FFprobe*** and the ***FFmpeg*** library itself. Here it is used to gather multiple streams of the requested video and audio, find the highest quality video available to download, merge streams, and so on.

***FFprobe*** is used to gather the metadata of a video or an audio file, like its playtime, codec, resolution, and others.

### Installation

To install **FFmpeg**, it is recommended to download it directly from its website. Go to the official [FFmpeg](https://ffmpeg.org/download.html) website.

Select your operating system, Here, I’ve selected *Windows* as my operating system and select "***Windows builds from*** [***g***](http://gyan.dev)***yan.dev***".

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692570940056/7238c5f0-3fc3-48fa-a582-4181a56a0453.png align="center")

Here, navigate to **git master builds** and select "***ffmpeg-git-essentials.7z***".

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692570995130/219f536c-ecdd-4124-a7df-67576b6c2e71.png align="center")

Now add the ***bin*** folder to your system’s environment variables **path**, and you are good to go!

## Usage

Open a command-line interface like the terminal to make sure that everything is properly working.

Run,

`yt-dlp`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692569495392/df2f4e32-9c4a-4ce9-aa14-4d15f41ecb2e.png align="center")

Similarly, run ***ffmpeg***, and it should show up something like this!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692571080514/13ab3298-8ed9-48e2-a96e-e2a9c5a563d8.png align="center")

Now, to view all the available features in yt-dlp, run

`yt-dlp --help`

### **Downloading videos from the internet**

To download a single video run,

`yt-dlp [URL]`

*Ex: yt-dlp* [*https://www.youtube.com/watch?v=\_BtXPQimVhg*](https://www.youtube.com/watch?v=_BtXPQimVhg)

To download multiple video run,

`yt-dlp [URL] [URL] [URL]`

*Ex: yt-dlp:* [*https://www.youtu.be/BtXPQimVhg*](https://www.youtu.be/BtXPQimVhg) [*https://youtu.be/dqC5x7cwwl0*](https://youtu.be/dqC5x7cwwl0)

Alternatively, you can place multiple URLs in a '**.txt**' file in the same folder of your current directory, which can be seen in your terminal. Now run,

`yt-dlp -a [File name].txt`

To see a list of all the available video and audio formats, run

`yt-dlp -F [URL]`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692571747478/724ce901-1d92-4a0a-aea0-3bee29e8a98a.png align="center")

Here, select any ***format ID*** that you want to, highlighted in the **green** colour and run the following to download your specified file format,

`yt-dlp -f [format_id] [URL]`

To download a playlist use,

`yt-dlp [Playlist URL]`

To download a YouTube live video from the start run,

`yt-dlp--live-from-start [URL]`

*Note: This is an experimental feature and may not work for every live-stream video.*

By default, your videos don't include the thumbnails or subtitles. Run the following to get the same,

`yt-dlp [URL]--embed-thumbnail --write-subs`

Alternatively, you can also use,

`--write-thumbnail --embed-subs --write-auto-subs (To download auto-generated subtitles)`

### **Note:**

* **All the methods and supported sites mentioned at the time of writing this article, may not work/support while you are reading it, always refer to the official 'Yt-dlp' repository for the up-to-date information.**
    
* **This article is for educational purposes only. The author and Hashnode do not endorse or promote the use of yt-dlp or any other software to download videos without permission. You are advised to respect the intellectual property rights of content creators.**
    

# References

1. [Yt-dlp supported sites](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md)
    
2. [GitHub re-instating YouTube-dl](https://github.blog/2020-11-16-standing-up-for-developers-youtube-dl-is-back/)
    
3. [The document released by the Electronic Frontier Foundation](https://github.com/github/dmca/blob/master/2020/11/2020-11-16-RIAA-reversal-effletter.pdf)
    
4. [De-ciphering the Rolling Cipher](https://news.ycombinator.com/item?id=24876321)