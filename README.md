# agent-kit

Agent skills by Dmitriy Panfilyonok, packaged for [skillshare](https://github.com/runkids/skillshare). Licensed under MIT.

## Layout

```
bundles/
  <bundle>/
    <skill>/
      SKILL.md
```

A folder under `bundles/` is a bundle, and a bundle is what you install together. It is not a topic: two skills on the same subject go into different bundles if people install them separately. Every skill lives in exactly one bundle.

| Bundle | What it holds |
|---|---|
| [`personal`](bundles/personal) | Writing style for texts that humans read: tracker tickets, documents, plain punctuation. |

## Naming

Skills, commands and agent roles in a bundle carry the `kit-` prefix. Skills, commands and roles share one `/` namespace in the harness, and the prefix keeps them from shadowing built-ins and other people's skills. It also makes them easy to find.

The one exception is `personal`: its skills keep the `my-` prefix. That prefix already marks them as personal, and renaming them would only break existing calls.

## Install

Install a bundle as a subfolder of this repository and pin it to a tag:

```sh
skillshare install dpanfilyonok/agent-kit/bundles/personal --branch v0.1.0 --all
skillshare sync
```

Add `-s <name>` instead of `--all` to take only some skills from a bundle.

## Versions

Releases are tags `vX.Y.Z`. Install by tag, not from `main`: `main` moves, and a tag is what a lockfile can pin.

## Other people's skills

Skills written by others are not copied here. A bundle refers to them by link with a pinned version. A skill synthesized from others' work is our own text and says what it is based on, with a link to the source license.
