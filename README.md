English | [中文](README.zh.md)

# logseq-media-ts-pro

Create timestamps for audio and video to facilitate your learning and meeting reviews.

## Feature Highlights

- Support local audio/video, network audio/video and Bilibili videos.
- Quickly generate audio/video timestamps, click the timestamp to jump to the corresponding time of the audio/video.
- Timestamps support time range, clicking a timestamp will play from the specified start time to the specified end time. (Bilibili not supported)
- The playback count can be set on the ranged timestamp, which is a convenient repeater.
- A timestamp player can be inserted on the page, through which you can filter the timestamps to be played as well as their playing.

## How to Install

1. Download the newest zip file from the [Releases](https://github.com/sethyuan/logseq-hierarchy-jump/releases) page.
1. Unzip the zip file into the folder where you want to store the plugin.
1. Turn on the developer mode in Logseq. ![](./assets/developer_mode.png)
1. Load the unzipped folder (named `logseq-media-ts-pro`) by clicking on the `Load unpacked plugin` button on the plugins modal. ![](./assets/load_plugin.png)
1. You should now see the plugin being installed.

## Usage

### How to insert video/audio

### How to insert single time point timestamps

### How to insert ranged timestamps

### How to specify the number of times to play and the interval between each play

### How to insert and use the control bar

## Timestamp Syntax Reference

### Single time point

Not attached to any particular media:

```
{{renderer :media-timestamp, time}}
```

Attached to a specific media:

```
{{renderer :media-timestamp, time, ((media block ref))}}
```

### Ranged

Not attached to any particular media:

```
{{renderer :media-timestamp, from, to, [play-count], [interval-between-each-play]}}
```

Attached to a specific media:

```
{{renderer :media-timestamp, from, to, [play-count], [interval-between-each-play], ((media block ref))}}
```

`play-count` defaults to `1`.

`interval-between-each-play` is in seconds and it defaults to `1`.

## Control bar syntax reference

```
{{renderer :media-ts-control, interval, [filter tag]}}
```

`interval` is interval to wait between each timestamp.

`filter tag` is a tag in the syntax `[[tag]]` to filter which timestamps to play, only timestamps on those blocks with the specified tag will be played. If no filter tag is provided, all timestamps on the screen will be played.

## Join the community

Join the Discord channel [here](https://discord.gg/vMS3x5QRVx) where we discuss everything related to the plugin.
