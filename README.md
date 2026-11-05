# Sonos2mqtt companion

The default [MQTT](https://www.home-assistant.io/integrations/mqtt/) integration for Home Assistant does not have support for **Media Players**.
To get the speakers from sonos2mqtt into homeassistant you have to use this component (and enable discovery for sonos2mqtt)

[![HACS Custom][badge_integration]][link_integration-repo] [![Github stars][badge_integration-stars]][link_integration-repo] [![Github issues][badge_integration-issues]][link_integration-issues]

[![Support me on Github][badge_sponsor]][link_sponsor] [![Follow on BlueSky][badge_bluesky]][link_bluesky]

## Installation

1. Install [HACS (Home Assistant Community Store)](https://hacs.xyz/docs/setup/prerequisites)
2. Add a [custom repository](https://hacs.xyz/docs/faq/custom_repositories)
3. Look for the mqtt integration and click install

Custom repository details:

- Repository: `svrooij/homeassistant-sonos2mqtt/`
- Category: `Integration`

## Works with

This integration and [Sonos2mqtt](#sonos2mqtt) are both build by [me](https://svrooij.io/) and work perfectly toghether. If you build a media player that also emits mqtt messages, you should be able to get it to work for your own media player with minor changes. Just send a [PR][link_integration-pr]

### Sonos2mqtt

[![Sonos2mqtt][badge_sonos-mqtt]][link_sonos-mqtt] [![docker pulls][badge_sonos-mqtt-docker]][link_sonos-mqtt-docker] [![sonos2mqtt issues][badge_sonos-mqtt-issues]][link_sonos-mqtt-issues]

The latest beta version of Sonos2mqtt ([3.2.0-beta.7](https://github.com/svrooij/sonos2mqtt/releases/tag/v3.2.0-beta.7)) has support for sending the correct mqtt discovery messages. And works perfectly in combination with this home assistant integration.

Thousands of users are already using this application, according to the amount of Dockerhub pulls.

The most noteworthy feature is support for [notifications](https://svrooij.io/sonos2mqtt/control/notifications.html), which actually restore playback after playing.

## License

This integration is licensed under [MIT license](https://github.com/svrooij/home-assistant-mqtt-component/blob/main/LICENSE), so feel free to copy or adjust. I like contributions but use for your own good otherwise.

## Developer information

[![Devcontainer][badge_devcontainer]][link_devcontainer]

Start by installing the [Dev Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

This repository has a custom crafted [devcontainer](./.devcontainer/devcontainer.json) that downloads the latest version of [Home Assistant](https://www.home-assistant.io/) upon creation.

### Debugging

Let's say you changed something to this module and want to test your changes. Just press `F5` (for the default debug action). It's that easy, a clean version Home Assistant instance will start on the local `8123` port, with the debugger connected.

**Note** The first time you start home assistant you'll have to do the regular onboarding flow. And the first time it might take a little longer to install all the requirements (they are not installed when we just install home assistant).

Additional debug sessions will go much faster, I promise.

### Update test Home Assistant

This repository does not have the code for Home Assistant, it just has a [requirements](./requirements.txt) file that is uses to install home assistant upon container creation.
If you want to update your dev envirionment press `CTRL + SHIFT + P` and execute `Dev Containers: Rebuild container`.

### GIT information

You won't be able to commit your changes until you set your git information inside the container, but the script is configured to copy the `GIT_NAME` and `GIT_EMAIL` environment variables from your local system when the container is created.

You can also execute these commands afterwards if you already made changes and want to commit those.

```bash
git config --global user.name "your name"
git config --global user.email "youremail@somedomain.com"
```

[badge_devcontainer]: https://img.shields.io/badge/VSCode-DevContainer-orange.svg?logo=visualstudiocode&style=for-the-badge
[badge_integration]: https://img.shields.io/badge/HACS-Custom-41BDF5.svg?logo=Home+Assistant+Community+Store&style=for-the-badge&logoColor=white
[badge_integration-issues]: https://img.shields.io/github/issues/svrooij/home-assistant-mqtt-component?logo=github&style=for-the-badge
[badge_integration-stars]: https://img.shields.io/github/stars/svrooij/home-assistant-mqtt-component?logo=github&style=for-the-badge

[badge_sonos-mqtt]: https://img.shields.io/badge/sonos-mqtt-blue?style=for-the-badge
[badge_sonos-mqtt-docker]:https://img.shields.io/docker/pulls/svrooij/sonos2mqtt?logo=docker&style=for-the-badge
[badge_sonos-mqtt-issues]: https://img.shields.io/github/issues/svrooij/sonos2mqtt?logo=github&style=for-the-badge
[badge_sonos-mqtt-stars]: https://img.shields.io/github/stars/svrooij/sonos2mqtt?logo=github&style=for-the-badge

[badge_sponsor]: https://img.shields.io/github/sponsors/svrooij?logo=github&style=for-the-badge
[badge_bluesky]: https://img.shields.io/bluesky/followers/svrooij.io?logo=bluesky&style=for-the-badge&logoColor=white

[link_devcontainer]: https://code.visualstudio.com/docs/devcontainers/containers
[link_integration-issues]: https://github.com/svrooij/homeassistant-sonos2mqtt/issues
[link_integration-pr]: https://github.com/svrooij/homeassistant-sonos2mqtt/pulls
[link_integration-repo]: https://github.com/svrooij/homeassistant-sonos2mqtt

[link_sonos-mqtt]: https://svrooij.io/sonos2mqtt
[link_sonos-mqtt-docker]: https://hub.docker.com/r/svrooij/sonos2mqtt
[link_sonos-mqtt-issues]: https://github.com/svrooij/sonos2mqtt/issues
[link_sonos-mqtt-repo]: https://github.com/svrooij/sonos2mqtt

[link_sponsor]: https://github.com/sponsors/svrooij
[link_bluesky]: https://bsky.app/profile/svrooij.io
