<img width="1413" height="201" alt="Screenshot 2026-08-17 at 12 45 10 PM" src="https://github.com/user-attachments/assets/e7e443df-11c6-4469-b2ed-cf7aa2f9428d" />
# CyberSpace/64

CyberSpace/64 is a Commodore 64 BBS client for [CyberSpace.Online](https://cyberspace.online). It acts as a telnet bridge that translates CyberSpace's REST/Firebase API into real-time PETSCII, so a real (or emulated) C64 can log in and use it like a proper BBS featuring a live post feed, real-time chatrooms (via "CIRC"), private "C-Mail", real-time notifications, and more. All primary data lives on CyberSpace's servers â€” CS/64 just bridges the wire protocol. The only thing ever stored locally is an optional "remember me" record (your email plus a refresh token, not your password) so the client can auto-sign-in on future connections. :-)

NOTICE: This is an unofficial, third-party client. CyberSpace.Online, the CyberSpace API, and all CyberSpace-related material belong to [@UnremarkableGarden](https://github.com/unremarkablegarden). See [`LICENSE`](LICENSE) for what MIT covers concerning this client.

NOTICE #2: CyberSpace/64 is currently in **BETA**. That said, please create a GitHub issue if you find bugs!

Alternatively, if you have suggestions, please [email me!](mailto:thereal.landonjsmith@gmail.com)

## Features of CyberSpace/64

- **The CyberSpace Feed:** browse, read, reply to, and post entries with titles, topics, and NSFW flags. Due to hardware limitations, images, ASCII art, internet links, and posted songs are listed as a bracketed placeholder instead of the original posted medium (e.g., `[WEB LINK]` instead of `https://landonjsmith.com`).

- **Live Chat via "CIRC":** CIRC gives you selectable multi-user chatrooms, slash commands (`/fortune`, `/8ball`, `/rainbow`, `/slap`, `/hi5`, `/me`, `/slow`), `@mention` for alerting a user, a dynamically updated online user roster, and an in-client `/help` for a command list.

- **Private messaging via "C-Mail":** C-Mail gives you 1-on-1 conversations, live typing indicators, scrollable history, and the same slash commands as the CIRC system.

- **Notifications:** notifications on the client mirror those sent to you on CyberSpace.Online, with a live "unread" badge on the main menu, a dynamic inbox, and a direct jump-to-content system for replies, mentions, pokes, and follows. C-Mail's own unread badge works a little differently â€” it polls C-Mail directly rather than relying on notifications, since CyberSpace's DM notifications don't reliably fire on their own.

- **User Directory lookup:** this allows you to search for a username, view a profile, poke someone, or browse a person's feed post history.

- **Saved logins:** the client can remember accounts across sessions with a "remember me" capability. This is the one piece of data CS/64 ever stores locally â€” your email and a refresh token (never your password) â€” kept in a JSON file on whatever machine is running the bridge. (That is, if you're hosting the Python bridge on a Raspberry Pi, that file lives on the Pi.)

- **Everything delivers live:** feed, notifications, and C-Mail all poll in the background and surface new items so you can easily keep track of replies, posts from friends or people you're following, mentions from people in chatrooms, and quite a bit more. :-)

## Setup
Setup is really easy! Just three steps.*

1. pip install aiohttp
2. python3 bbs.py --port 6400
3. Connect your C64 terminal client to the machine's IP on that port.


*( Three steps provided you have python installed... ;-) )

## CIRC Chatroom/C-Mail Commands

Inside a CIRC chatroom or C-Mail conversation, these are the valid client chat commands:

| Command | Does |
|---|---|
| `/help` | List commands |
| `/who` | Who's online (chat only) |
| `/fortune` | Random fortune |
| `/8ball <question>` | Magic 8-ball |
| `/rainbow <message>` | Rainbow text |
| `/slow <message>` | S p a c e d   o u t   t e x t |
| `/slap <@user>` | Slap someone |
| `/hi5 <@user>` | High-five someone |
| `/me <action>` | Action message |
| `/quit` | Leave |

## License

CYBERSPACE-64 CLIENT

Copyright (C) 2026 Landon James Smith

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
