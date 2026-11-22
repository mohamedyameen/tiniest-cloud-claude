# Tiniest Cloud for Claude

Build and put unlimited apps, websites, dashboards and reports online, free and secure, right
from a conversation with Claude, on [Tiniest Cloud](https://tiniest.cloud). Each one comes with
sign-in, a database, realtime, push notifications, scheduled jobs and AI built in — with no keys
to manage and no server to set up.

This plugin adds two skills:

- **The `tiny` skill**, which tells Claude how to build for the platform — a frontend
  using the `tiny` SDK, no login flow, no `localStorage`, no server of its own (server logic
  goes in backend functions).
- **The `tiny-design` skill**, which tells Claude how what it builds should look: a direction
  chosen for the product and its industry, its own palette and type, balanced screens, quick
  purposeful motion, light and dark, and a checklist — with a playbook each for apps, websites,
  dashboards, presentations and forms. When you have design standards of your own (a design
  system, components, a brand guide), those come first.

The tools come from the **Tiniest Cloud connector** (`https://app.tiniest.cloud/mcp`), which you
add once (see Install). With it, Claude can deploy an app and get a live URL, save a draft and
look at it before it goes live, take an app offline without deleting it, share an app by email,
roll back to an earlier version, connect a third-party API without putting its key in the page,
let an app take payments into your own Stripe or Razorpay account, schedule recurring work, put
an app on your own domain, and read or change the data an app has saved.

## Install

**Claude (web, desktop, mobile and Cowork):** open Customize → Plugins → Discover, find
*Tiniest Cloud* and add it. Then add the connector with
[this link](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Tiniest%20Cloud&connectorUrl=https%3A%2F%2Fapp.tiniest.cloud%2Fmcp), which opens Customize → Connectors with the name and address filled in
(or choose Add custom connector and enter `https://app.tiniest.cloud/mcp`).

**Claude Code:**

    /plugin marketplace add mohamedyameen/tiniest-cloud-claude
    /plugin install tiniest-cloud@tiniest-cloud

A connector added on claude.ai also reaches Claude Code signed in to the same account. To add it
in Claude Code alone:

    claude mcp add --transport http tiniest-cloud https://app.tiniest.cloud/mcp

The first time Claude uses a Tiniest Cloud tool, your browser opens to sign in (or create a
free account). There is nothing to paste.

## Try it

- "Build a small expense tracker and put it on Tiniest Cloud."
- "What apps do I have on Tiniest Cloud?"
- "Share my notes app with sam@example.com."

## What it sends

The plugin itself sends nothing: it is two skills, which are text. The connector you add is
what talks to Tiniest Cloud at `app.tiniest.cloud`, and only when Claude calls one of its tools
on your behalf:

- the files of an app you ask Claude to deploy;
- the email addresses of people you share an app with;
- entries you ask Claude to write to an app's saved data, and the details of any API connection
  or scheduled job you set up.

Reading tools send only the name of the app and what to look up. The plugin stores nothing and
runs no code on your machine, and the server is hosted.

## Privacy and support

- Privacy policy: https://tiniest.cloud/privacy
- Terms: https://tiniest.cloud/terms
- Support: support@tiniest.cloud

This repository contains only the Claude plugin: its manifest and the skills. The server
itself is hosted by Tiniest Cloud.
