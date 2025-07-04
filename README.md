- [Declutter - YouTube](https://raw.githubusercontent.com/thealex-br/web-declutter/refs/heads/main/YouTube.txt) for a minimal interface
- [Cleaner - YouTube](https://raw.githubusercontent.com/thealex-br/web-declutter/refs/heads/main/CleanerYouTube.txt) for a less distracting interface

## Create your own personal filters for YouTube
#### Block video by title
`youtube.com###video-title:has-text(/keyword1|keyword2/i):upward(#dismissible):remove()`
#### Block video by description
`youtube.com##.metadata-snippet-text:has-text(/keyword1|keyword2/i):upward(#dismissible):remove()`
#### Block video by channel
`youtube.com##.yt-formatted-string.yt-simple-endpoint[href="/@youtube_channel_url"]:upward(#dismissible):remove()`
#### Block video by title and description
`youtube.com##:has(#video-title, .metadata-snippet-text):has-text(/keyword1|keyword2/i):upward(#dismissible):remove()`
#### Block video by language
```
! Indian content
youtube.com##:has(#video-title, .metadata-snippet-text):has-text(/[ऀ-ॿঀ-৿ਅ-੿଀-୿அ-௿ఀ-౿ഀ-ൿ]/):upward(#dismissible):remove()

! Arabic content
youtube.com##:has(#video-title, .metadata-snippet-text):has-text(/[؀-ۿِ-ٟࢠ-ࣿ]/):upward(#dismissible):remove()

! Russian content
youtube.com##:has(#video-title, .metadata-snippet-text):has-text(/[А-Яа-яЁё]/):upward(#dismissible):remove()
```

## FAQ
Why `:remove()` instead of just hiding?
- `:remove()` make it consume less memory
