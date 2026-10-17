<div align="center">

# website.php

**One file. One method. Zero regrets.\***

[![files](https://img.shields.io/badge/files-1-FFD60A?style=flat-square)](website.php)
[![methods](https://img.shields.io/badge/methods-website()-FFD60A?style=flat-square)](website.php)
[![database](https://img.shields.io/badge/database-an%20array-111110?style=flat-square)](website.php)
[![build](https://img.shields.io/badge/build-there%20is%20no%20build-46A758?style=flat-square)](#installation)
[![tests](https://img.shields.io/badge/tests-it%20loaded-46A758?style=flat-square)](#testing)
[![coverage](https://img.shields.io/badge/coverage-vibes-FF7A1A?style=flat-square)](#testing)
[![dependencies](https://img.shields.io/badge/dependencies-hope-6BD4FF?style=flat-square)](#requirements)

**[website.php.revenantal.com](https://website.php.revenantal.com)**

</div>

website.php is the Monolith-First™ framework: an entire website, lovingly hand-stuffed into a single PHP function called `website()`. There's no database, no classes, no router, no build step, and no second file. It's just arrays, if statements, and the quiet confidence of someone who has never heard of Git.

This is now a Git repository. We're working through it.

<sub>\*Regrets sold separately. Regrets may appear around line 40,000.</sub>

---

## Why website.php?

| | "Modern" frameworks | website.php |
| --- | --- | --- |
| Files | 4,812 (excluding `node_modules`) | **1** |
| Methods to remember | Several hundred, renamed every major version | **`website()`** |
| Database | Postgres, Redis, a queue, a cache for the queue | **`$data = [];`** |
| Routing | `routes/web.php`, `routes/api.php`, middleware | **`if`** |
| Build step | 17 minutes and a prayer | **Ctrl + S** |
| Architecture diagram | A Miro board nobody understands | **□** |
| Learning curve | Steep | **Flat. Extremely long. Flat.** |

## Requirements

- PHP (any version that still answers the phone)
- Hope

## Installation

1. Drag `website.php` onto any server that runs PHP.
2. Click "Overwrite".
3. Do not click anything else. Ever.

Or, for people who like typing:

```bash
php -S localhost:8000 website.php
```

Then open http://localhost:8000. That's the whole getting-started guide. You're done. Go outside.

## Project structure

```
website.php
```

Every other file in this repository is a hostage of GitHub's conventions. None of them run. None of them are website.php. Legal has confirmed they don't count as a second file. Legal is an array.

## Architecture

```
+-----------------+
|   website.php   |
+-----------------+
```

Print it out. Frame it. Show your investors.

## Routes

Routing is a chain of `if` statements on `$_GET['page']`. To add a route, add an `else if`. To remove a route, comment it out and move it to the **BACKUPS — DO NOT DELETE** section, where it will live forever.

| Route | What it does |
| --- | --- |
| `?page=home` | The landing page |
| `?page=about` | Our story, from 2003 to the Second Method Incident |
| `?page=docs` | Inline documentation, rendered from an array |
| `?page=contact` | Talk to sales. Leads are stored in an array and forgotten when the request ends |
| `?page=cookies` | Cookie preferences and our trusted partners. One of them is Steve |
| `?page=robots` | robots.txt, but it's an array |
| `?page=llms` | llms.txt, for the robots that read |
| `?page=api` | A REST API with one endpoint. It describes itself |
| `?page=download` | website.php downloads website.php. A quine with a business model |
| `?page=admin` | There is no admin panel |
| anything else | Rewrites the request to `home` and calls `website()` again |

Add `?accent=orange`, `green` or `blue` to change the colour. Each one has been personally approved by an `else if`.

## Docker

### A statement from the Founder regarding the Dockerfile

We were told that a modern project "needs a Dockerfile."

We asked why. We were told it was so that website.php would "run the same everywhere."

We pointed out that website.php is one file, and it already runs the same everywhere, because it is the same file everywhere. We were told that was "not the point."

We were then told the Dockerfile would make website.php "cloud-native." We asked what website.php was before. Nobody could tell us.

And so, after a long and painful meeting, we present: **a second file, whose only job is to carry the first file.**

### The Dockerfile

```dockerfile
FROM php:8.4-apache

COPY website.php /var/www/html/index.php
```

Two lines. Read them slowly. Notice what happens on line two.

**It renames website.php to `index.php`.**

We want to be very clear that this is not a second file. It is the same file, entering a witness protection programme. Inside the container, website.php lives a quiet life under an assumed name. It doesn't talk about where it came from. If you see it, don't say anything.

### Usage

```bash
docker build -t website-php .
docker run -p 8080:80 website-php
```

Then open http://localhost:8080.

### Container architecture

```
+--------------------------------------------------+
|  Docker                                          |
|  +--------------------------------------------+  |
|  |  Debian (~75 MB)                           |  |
|  |  +--------------------------------------+  |  |
|  |  |  Apache (several thousand files)     |  |  |
|  |  |  +--------------------------------+  |  |  |
|  |  |  |  PHP 8.4 (several more)        |  |  |  |
|  |  |  |  +--------------------------+  |  |  |  |
|  |  |  |  |  index.php               |  |  |  |  |
|  |  |  |  |  (it's website.php,      |  |  |  |  |
|  |  |  |  |   in a fake moustache)   |  |  |  |  |
|  |  |  |  +--------------------------+  |  |  |  |
|  |  |  +--------------------------------+  |  |  |
|  |  +--------------------------------------+  |  |
|  +--------------------------------------------+  |
+--------------------------------------------------+
```

To run one file, Docker downloads an entire operating system, a web server and a language runtime. This is called "lightweight."

### Frequently asked Docker questions

**Do I need Docker to run website.php?**
No. You need PHP. You have always only needed PHP. Docker is here because a recruiter asked.

**Does the image contain more than one file?**
The image contains roughly 20,000 files. website.php is one of them. The other 19,999 are infrastructure, and infrastructure doesn't count. That's the rule. We just made it up.

**Is website.php now microservices?**
It is one microservice. It is a macroservice in a microservice's clothing.

**Can I use Kubernetes?**
You can. We'd like you to sit with that decision first. Take a walk. Drink some water. If you still want to orchestrate a fleet of identical containers, each holding one identical file, we can't stop you. But we will be thinking about you.

**Why was Dockerfile in the .gitignore?**
Because it was supposed to never exist. It now exists. The `.gitignore` entry has been commented out, not deleted, in keeping with our version-control philosophy. One day we may need to restore our dignity.

**Is there a docker-compose.yml?**
No. We have to draw the line somewhere, and that line is "one file to carry the one file." A file to configure the file that carries the file is where we get off.

## Testing

Open the page in a browser. Does it load? Test passed. Does it not load? Refresh. Does it load now? Test passed.

```bash
php -l website.php   # our entire CI pipeline
```

## Branching strategy

We use a branching model called **Trunk-Based Denial**. All real work happens on `main`. Other branches exist, but only as cautionary tales.

| Branch | Status |
| --- | --- |
| `main` | Production. Also staging. Also dev. Also Kyle's sandbox, unfortunately |
| `kyle/refactor-into-functions` | Adds a second function. Will never be merged. Kyle asks about it every standup |
| `feature/database` | "Migrates to a database" by renaming an array to `$db`. Technically correct |
| `hotfix/friday-deploy` | Deployed at 4:58 PM on a Friday. Fixed nothing. Broke nothing. Nobody knows why it exists |
| `website-v2` | The rewrite. One commit. It's a TODO |
| `do-not-merge` | Has been merged into `main`. Check the history. Check the comment it left behind |

Merge conflicts are resolved by keeping both versions and commenting one out. See: **BACKUPS — DO NOT DELETE**.

## Releases

Every release is the same commit, tagged with increasing confidence:

- `v1.0.0`
- `v1.0.0-final`
- `v1.0.0-final-v2`
- ~~`v1.0.0-FINAL-v2`~~ (we pressed caps lock and felt powerful, but Windows filenames aren't case-sensitive, so Git refused to create it: "tag already exists." The operating system has seen through us.)
- `v1.0.0-final-v2-for-real`

## Deployment

Our CI/CD pipeline:

1. Open FileZilla.
2. Drag `website.php` onto the server.
3. Overwrite? **Yes.**

It has never once been red.

## FAQ

**Does it scale?**
Yes. Vertically. The file just gets taller.

**Can I add a second method?**
No.

**Why is this on GitHub if you don't believe in Git?**
Version control, the website.php way, is commenting out the old code and leaving it there forever. Git is our backup of the backups.

**Is this a joke?**
`if ($you_laughed) { return true; } else { website(); }`

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). (It tells you to see website.php.)

The short version: shout "I'M IN WEBSITE.PHP" across the office before editing. Whoever shouts last wins. This is called eventual consistency.

Pull requests that split `website()` into "smaller, more focused functions" will be closed. It is extremely focused. It is focused on everything.

## License

[MIT](LICENSE), plus the One-File Rider: you may use this file however you like, provided you never split it into two files.
