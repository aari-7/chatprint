# Chatprint

Drop in a chat export and get a full report: messages, mood by week, who starts conversations, reply times, a day-by-hour heatmap, word clouds and signature words, a mosaic of every day you talked, and a separate analysis for every person in the chat.

The full version, with AI insights, shareable reports and "Text their twin" (a clone that texts back the way your friend actually texts), runs on claude.ai:
https://claude.ai/artifact/BABxxjeK87iPyU8xG88fD9

## Supported exports
- WhatsApp `.txt` or `.zip` (Export chat → Without media)
- Instagram / Messenger `.json`
- Telegram Desktop `.json`
- Discord (DiscordChatExporter) `.json`
- iMessage via `imessage-exporter -f txt`

## Privacy and security
- Chats are parsed and counted entirely in your browser. Nothing is uploaded by the page itself.
- The standalone `index.html` ships a strict Content-Security-Policy (`connect-src 'none'`), so it cannot send data anywhere. The only external script is JSZip from cdnjs, pinned with a Subresource Integrity hash.
- Hosted on GitHub Pages it is served over HTTPS only.
- In the claude.ai version, AI features send a sample of messages to Claude on the viewer's own account, and a shared report stores only stats and AI write-ups, never the messages.

## Files
- `index.html` — standalone page (stats only; AI features need claude.ai)
- `src/chatprint.artifact.html` — the claude.ai artifact source
