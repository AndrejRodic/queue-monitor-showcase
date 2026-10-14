# Queue Monitor

A public case study for a published Chrome extension. The extension source remains private.

## The problem

Players competing in Minecraft skill tests often wait in Discord queues. They need to watch for a new queue and join quickly.

## What I built

I built and published a JavaScript Chrome extension using Chrome APIs and Manifest V3. It monitors visible queue messages in Discord Web, detects new or edited queue posts, filters duplicate messages, tracks queue status, and can join when a new queue opens. It also includes activity logs and Chrome notifications.

A Cloudflare Workers backend handles license validation and server-side rate limits. The extension does not ask for a Discord account token.

## My contribution

I designed, built, released, and maintained the extension. I worked on queue detection, duplicate handling, joining behavior, user settings, activity information, notifications, and the licensing connection.

## Results

- 300+ extension users, based on my reported count as of October 6, 2026.
- Published on the [Chrome Web Store](https://chromewebstore.google.com/detail/mctiers-queue-sniper-watc/aibcfnkajkoandabcpbebgaijomadkjn).

## Design decisions

- Ignore queue messages already visible when monitoring starts, so old posts do not trigger a join.
- Handle both new queue messages and existing messages edited to add a Join button.
- Keep user settings and activity history on the device where possible.
- Keep licensing decisions and rate limits on the backend.
- Do not collect Discord passwords or account tokens.

## What I learned

Shipping a browser extension means more than writing the popup. Queue messages can change after they appear, repeated events need careful handling, and the product needs a clear boundary between local browser data and server-side licensing.

## Demo

The Chrome Web Store page above is the public demo.

![Early store listing screenshot for Queue Monitor](assets/queue-monitor-early-v1.2.11.png)

This image is from the v1.2.11 store listing and shows an earlier interface. It is included as the project screenshot and can be replaced with a newer capture later.

## Source and privacy

The production source repository is private. This repository is a written case study and does not include private source, credentials, customer data, license keys, or deployment secrets.

This is an unofficial third-party product and is not affiliated with Discord or MCTiers.
