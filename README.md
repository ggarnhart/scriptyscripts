# scriptyscripts

To install dependencies:

```bash
bun install
```

It's possible to install all of this stuff with npm, yarn, pnpm, etc., but I prefer `bun` because it's trendy and fast and neat.

To run, I recommend using Vercel:

```bash
vercel run dev
```

# Shortcuts

## stationTimes.js

The `stationTimes.js` endpoint (accessible here: `https://scriptyscripts.vercel.app/api/shortcuts/stationTimes`) accepts a `POST` request and a JSON object that accepts the following parameters:

```JSON
{
    "stations": ["L01S", "A31N"], // these can be any relevant stations. You can view the absurd JSON document of all station info in the stationTimes.js file
    "lines": ["L", "A"] // these can be any releavnt lines. 'A', 'G', etc.
}
```

It is currently hosted on Vercel's hobby tier. If it gets abused I'll change its structure / remove it, but for now it's a fun little thing to play with and I don't pay for it. Go wild.

Anyway, you'll get back a JSON object that looks like this:

```JSON
{
    "messages": [
        "L: 3, 8 minutes\n",
        "A: 1, 26 minutes\nC: 0, 4 minutes\nE: 0, 13 minutes\n"
    ]
}
```

Anyway, I like to use this with iOS Shortcuts. Maybe you will too!
