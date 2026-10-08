# Broker radio with text-to-speech (n8n)

n8n workflow for an online radio for brokers: on a schedule it generates speech with the
OpenAI text-to-speech API (`/v1/audio/speech`) and posts the audio file to Discord.

Nodes: Schedule Trigger, `tts` (Code), `rename` (Code), `server` (HTTP Request to OpenAI),
`Discord`.

## Setup

1. Import `radio.json` in n8n.
2. Put your OpenAI API key into the places marked `YOUR_API_KEY` / `REPLACE_ME`
   (Code node `tts` and the `Authorization` header of the HTTP node).
3. Select your own Discord webhook credential in the `Discord` node.
