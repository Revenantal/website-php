# website.php

**One file. One method. Zero regrets.\***

website.php is the Monolith-First™ framework: an entire website, lovingly hand-stuffed into a single PHP function called `website()`. There's no database, no classes, no router and no build step. It's just arrays, if statements, and the quiet confidence of someone who has never heard of Git.

(This is now a Git repository. We're working through it.)

\*Regrets sold separately. Regrets may appear around line 40,000.

## Installation

1. Drag `website.php` onto any server that runs PHP.
2. Click "Overwrite".
3. Do not click anything else. Ever.

Or run it locally:

```bash
php -S localhost:8000 website.php
```

## Project structure

```
website.php
```

That's it. This README is not a second file. It's documentation. Legal checked. Legal is an array.

## What's inside

| Route | What it does |
| --- | --- |
| `?page=home` | The landing page |
| `?page=about` | Our story, from 2003 to the second method incident |
| `?page=docs` | Inline documentation, rendered from an array |
| `?page=contact` | Talk to sales. Leads are stored in an array and forgotten when the request ends |
| `?page=cookies` | Cookie preferences, and our partners. One of them is Steve |
| `?page=robots` | robots.txt, but it's an array |
| `?page=llms` | llms.txt, for the robots that read |
| `?page=api` | A REST API with one endpoint. It describes itself |
| `?page=download` | website.php downloads website.php |
| `?page=admin` | There is no admin panel |
| anything else | Rewrites the request to `home` and calls `website()` again |

Add `?accent=orange`, `green` or `blue` to change the colour. Each one has been personally approved by an `else if`.

## Contributing

Shout "I'M IN WEBSITE.PHP" across the office before editing. Whoever shouts last wins. This is called eventual consistency.

Pull requests that split `website()` into "smaller, more focused functions" will be closed. It is extremely focused. It is focused on everything.

## License

You may use this file however you like, provided you never split it into two files.
