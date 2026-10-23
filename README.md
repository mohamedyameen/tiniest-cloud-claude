# Tiniest Cloud for Claude

Build a web app in a conversation with Claude and put it online at
[Tiniest Cloud](https://tiniest.cloud). Every app gets sign-in, per-user storage, realtime, push
notifications, scheduled jobs and an AI model — with no keys to manage and no backend to write.

This plugin adds three things:

- **The Tiniest Cloud MCP server** (`https://app.tiniest.cloud/mcp`). Claude can deploy an app
  and get a live URL, save a draft and look at it before it goes live, publish it or take an app
  offline without deleting it, share an app by email, roll back to an earlier version, connect a
  third-party API without putting its key in the page, schedule recurring work, put an app on
  your own domain, and read or change the data an app has saved.
- **The `tiny` skill**, which tells Claude how to build for the platform — a static frontend
  using the `tiny` SDK, no login flow, no `localStorage`, no server of its own (server logic
  goes in backend functions).
- **The `tiny-design` skill**, which tells Claude how what it builds should look: a direction
  chosen for the product and its industry, its own palette and type, balanced screens, quick
  purposeful motion, light and dark, and a checklist — with a playbook each for apps, websites,
  dashboards, presentations and forms. When you have design standards of your own (a design
  system, components, a brand guide), those come first.

## Install

**Claude (web, desktop, mobile and Cowork):** open Customize → Plugins → Discover, find
*Tiniest Cloud* and add it, then connect it on the plugin's Connectors tab.

**Claude Code:**

    /plugin marketplace add mohamedyameen/tiniest-cloud-claude
    /plugin install tiniest-cloud@tiniest-cloud

The first time Claude uses a Tiniest Cloud tool, your browser opens to sign in (or create a
free account). There is no API key to paste.

## Try it

- "Build a small expense tracker and put it on Tiniest Cloud."
- "What apps do I have on Tiniest Cloud?"
- "Share my notes app with sam@example.com."

## What it sends

Everything goes to Tiniest Cloud at `app.tiniest.cloud`, and only when Claude calls one of its
tools on your behalf:

- the files of an app you ask Claude to deploy;
- the email addresses of people you share an app with;
- entries you ask Claude to write to an app's saved data, and the details of any API connection
  or scheduled job you set up.

Reading tools send only the name of the app and what to look up. The plugin itself stores
nothing and runs no code on your machine; the skills are text, and the server is hosted.

## Privacy and support

- Privacy policy: https://tiniest.cloud/privacy
- Terms: https://tiniest.cloud/terms
- Support: support@tiniest.cloud

This repository contains only the Claude plugin: its manifest, the MCP server address and the
skills. The server itself is hosted by Tiniest Cloud.
