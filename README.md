# Xbox-xCloud-Client

[![Build/release](https://github.com/unknownskl/xbox-xcloud-client/actions/workflows/build.yml/badge.svg)](https://github.com/unknownskl/xbox-xcloud-client/actions/workflows/build.yml)

xbox-xcloud-client is an open-source client for Xbox home streaming made in Javascript and Typescript.

_DISCLAIMER: Xbox-xCloud-Client is not affiliated with Microsoft or Xbox._

## Features

- Stream video and audio from the Xbox One and Xbox Series
- Support for gamepad controls
- Keyboard controls
- Build-in online friends list

### Keyboard controls

The following keys are mapped as following:

    Dpad: Keypad direction controls
    Buttons: A, B, X, Y, Backspace (Mapped as B), Enter (Mapped as A)
    Nexus (Xbox button): N

### Streaming stats

During the stream you can show extra debug statistics that contain extra data about the buffer queues and other information. To bring this up you have to press `~` on your keyboard.

On the left bottom you can see the status (Altough not always accurate). The right top you can find the FPS of the video and audio decoders including the latency. On the right bottom you can find debug information about the buffer queues and other information that is useful for debugging perposes.

When possible always provide this information with your issue when possible (if it is related).

### Online friends list

The application also provides a way to see which of your friends are online. This can be useful when you want to quickly check if anyone is online to play with :)

## Install

You can either compile the project yourself or download the (unsigned) executable from the [releases](https://github.com/unknownskl/xbox-xcloud-client/releases) page

## Local Development

Clone the repository:

    git clone https://github.com/unknownskl/xbox-xcloud-client.git
    cd xbox-xcloud-client

Install dependencies:

    npm ci

Run development build:

    npm start

## Known Issues

- Audio can get distorted when the audio is delayed or gets out of sync. This should recover within 3 seconds. You can also manually press `0` on your keyboard to reset the audio timings.
- Video can get behind when the window is out of focus. To fix the issue, restart the application.
- Starting a new stream after disconnecting from the old one can cause unexpected behaviour and performance issues. Restart the application to fix this problem.
- Streaming from the Xbox Series seems to be working much better then with the Xbox One. The application is tested on both the Xbox One and Xbox Series.

## Changelog

See [changelog](CHANGELOG.md)