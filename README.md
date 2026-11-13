# Love it or Loathe it?

<p align="center">
<img src="https://img.shields.io/github/stars/gazoodle/casa-mia-love-or-loathe?style=for-the-badge&label=Stars&color=d6a102" alt="Stars">
<a href="https://github.com/gazoodle/casa-mia-love-or-loathe/releases"><img src="https://img.shields.io/github/downloads/gazoodle/casa-mia-love-or-loathe/total?style=for-the-badge&label=Downloads&color=e8604c" alt="Downloads"></a>
<a href="https://github.com/gazoodle/casa-mia-love-or-loathe/releases/latest"><img src="https://shields.io/github/v/release/gazoodle/casa-mia-love-or-loathe?style=for-the-badge&color=5da3a6" alt="version"></a>
<a href="https://github.com/gazoodle/casa-mia-love-or-loathe/actions/workflows/validate.yml"><img src="https://img.shields.io/github/actions/workflow/status/gazoodle/casa-mia-love-or-loathe/validate.yml?style=for-the-badge&label=Validated&color=3fbf5f" alt="Validated"></a>
<a href="https://github.com/gazoodle/casa-mia-love-or-loathe/blob/main/LICENSE"><img src="https://img.shields.io/badge/licence-MIT-5da3a6?style=for-the-badge" alt="Licence: MIT"></a>
</p>

An automatic media watcher that boosts the volume for a song you love, or changes the
radio station for one you loathe.

> **Maturity: Alpha.** Does its job every day in the author's house, but hasn't been tried in many others. Expect rough edges and changes. ([The levels](https://github.com/gazoodle/casa-mia/blob/2026.11.7/docs/README.md#maturity))

Sick of Xmas songs in November, yet love them in December? Then this is for you. But
that's not all: you can mark songs as loved or loathed, live, as they are playing.

Bored of radio stations with a short playlist? Then ask this integration to watch for
songs repeated within a period of time, and use those as triggers to change station too.

Or maybe you don't want the adverts? Shunt them too.

Pair it with Casa Mia's local radio station system and you can fade across to songs you
truly love to hear.

A full integration with events, so you can trigger your own automations too, including
notifications of what happened!

<img src="https://raw.githubusercontent.com/gazoodle/casa-mia/2026.11.7/docs/screenshots/love-or-loathe-detail.webp" alt="Love it or Loathe it's page in Casa Mia for an entry named Downstairs. Playing now: the kitchen is away on another station until 14:10, the living room is playing a song in the group Loathed by Ben, and the garden a song in Loved by Ann, each with Love it and Loathe it buttons. Under them the groups of songs, each with Love, Loathe and Ignore to click: Christmas songs, Heard too often, Loved by Ann and Loathed by Ben" width="800">

**Not built yet:** shunting the adverts, and the fade. Casa Mia's local radio station
is a Casa Mia feature still to come, not part of this integration: when it exists, it
is one more station to switch to. The rest of this guide describes what works today.

## What it's for

A radio station plays a mix you mostly like, with some songs you would rather skip and a
few you want louder. Love it or Loathe it watches the title and artist your media players
report, and acts when a track matches one of your groups of songs:

- change the volume by a percentage until the next track,
- mute until the next track,
- switch to another station for some minutes, then go back,
- or only fire an event, for an automation to act on.

How you feel about a group of songs can change. Each group is loved, loathed or ignored
at the moment, with an action for loved and another for loathed, and an automation can
change the feeling. The shipped list of Christmas songs is the example: loathed in
November, when a station starts playing them too early, and loved in December.

Each person in the house can have their own loved and loathed groups, and add the song
that is playing to them with a button on a dashboard.

It is an integration of its own, **Love it or Loathe it**. It runs wholly in Home
Assistant and needs neither the Casa Mia app nor the Casa Mia integration. Installed by
itself, from HACS or the Marketplace, it is set up and changed with Home Assistant's own
screens. With the Casa Mia app it also has a page there, which changes the same
settings. [Two ways to change its settings](https://github.com/gazoodle/casa-mia/blob/2026.11.7/docs/applets/love-or-loathe.md#two-ways-to-change-its-settings) lists
both.


## Installing

The Downloads badge at the top is GitHub's count of downloads of the releases' packages. Every
update and every repeat download adds to it, so it isn't the number of houses using
Love it or Loathe it.

Love it or Loathe it needs Home Assistant 2026.3.0 or later.

1. In HACS, or in Home Assistant's Marketplace (2026.11 and later), add
   `https://github.com/gazoodle/casa-mia-love-or-loathe` as a custom repository of the type Integration.
2. Download Love it or Loathe it there, then restart Home Assistant.
3. In Settings → Devices & services, choose Add integration and pick Love it or Loathe it.

The [guide](https://github.com/gazoodle/casa-mia/blob/2026.11.7/docs/applets/love-or-loathe.md) covers setting it up and everything it does.

## Part of Casa Mia

Love it or Loathe it is part of [Casa Mia](https://github.com/gazoodle/casa-mia), where it is written and
released. This repository is generated from Casa Mia 2026.11.7 (commit `cd152d50c4`) and
isn't edited by hand, so [issues](https://github.com/gazoodle/casa-mia/issues) and changes go to Casa Mia.

The Casa Mia app installs this same integration itself. A house with both needs to do
nothing about it: [With HACS or the Marketplace](https://github.com/gazoodle/casa-mia/blob/2026.11.7/docs/applets/love-or-loathe.md#with-hacs-or-the-marketplace)
says what happens.
