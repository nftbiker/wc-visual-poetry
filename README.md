# About

A ruby script to download all entries from ["Visual Poetry" warpcast channel](https://farcaster.xyz/~/channel/visual-poetry) and keep a copy in json and markdown format. The script is automatically run through a github actions to update the repository with new posts, twice a day.

# How to run

in irb, to download all archives

```
require './warpcast.rb'
data = Warpcast.new.call(days: :all)
```

Casts are read from a public Snapchain node (Farcaster Hub HTTP API, no API key needed).
Override it with `HUB_URL` in `.env` if that node goes down.

to download last 2 days

```
require './warpcast.rb'
data = data=Warpcast.new.call
```

# Jekyll website

Theme based on :
https://github.com/wowthemesnet/jekyll-theme-memoirs
