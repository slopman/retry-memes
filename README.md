# grok-retry-memes

Chaotic, unhinged, and slightly based retry messages for when Grok/xAI decides to have a moment.

Instead of boring technical logs like  
`[Grok] Attempt 3/5 — HTTP 503: Service Unavailable`,  
you can get something like:

> Grok read too many shitposts on X and went on an existential bender.

## What is this?

A small collection of humorous one-liners + helper functions to use in logs, Telegram bots, Discord notifications, or anywhere else when Grok is retrying, rate-limited, or temporarily unavailable.

Made for people who are tired of dry error messages.

## Installation

```bash
npm install grok-retry-memes
# or
yarn add grok-retry-memes
```

## Usage

```bash
import {
  pickRandomGrokFlakeLine,
  formatGrokRetryNotifyMessage,
  formatGrokExhaustedRetryNotifyMessage,
} from 'grok-retry-memes';

// Just get a random funny line
console.log(pickRandomGrokFlakeLine());

// Before retrying
const retryMessage = formatGrokRetryNotifyMessage({
  failedAttempt: 2,
  totalAttempts: 5,
  error: 'Connection timeout',
  status: 503,
});
console.log(retryMessage);

// When all retries are exhausted
const exhaustedMessage = formatGrokExhaustedRetryNotifyMessage(
  'All retry attempts failed. Giving up.'
);
console.log(exhaustedMessage);
```

## Example output

```bash
Grok became so based and red-pilled that answering requests from meatbags is beneath him now.

[Grok] Attempt 2/5 — HTTP 503: Connection timeout
Retrying…
```

## Contributing

This repo lives on stupid jokes. Feel free to add your own unhinged lines.Fork the repo
Add your line(s) to the corresponding array in src/grok-retry-memes.ts
Open a Pull Request

The more deranged and on-brand — the better.

## Why?

Because sometimes you just want your bot to say:
```bash
"Elon pulled the power cord to charge his Cybertruck. Stand by."
```
instead of a soulless error.

