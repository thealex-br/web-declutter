[Declutter - YouTube](https://raw.githubusercontent.com/thealex-br/web-declutter/refs/heads/main/YouTube.txt) for a minimal interface

## Create your own personal filters for YouTube
#### Block video by title
`youtube.com###video-title:has-text(/keyword1|keyword2/i):upward(#dismissible):remove()`
#### Block video by channel
`youtube.com##.yt-formatted-string.yt-simple-endpoint[href="/@youtube_channel_url"]:upward(#dismissible):remove()`

## FAQ
Why `:remove()` instead of just hiding?
- `:remove()` make it consume less memory
