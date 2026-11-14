# Voidstrap News

The news feed shown on the News page in [Voidstrap](https://github.com/KloBraticc/Voidstrap).

## Files

| File | Used by |
| --- | --- |
| `feed.json` | Current Voidstrap releases |
| `news.json` | Older Voidstrap releases, kept as is so they keep working |

New posts go into `feed.json`. Add them to `news.json` too only if older releases should see them.

## Format

```json
{
  "version": 1,
  "posts": [
    {
      "id": "2026-10-07-voidstrap-now-supports-linux",
      "date": "2026-10-07",
      "title": "Voidstrap now supports Linux",
      "body": "Voidstrap now runs on Linux.",
      "image": "https://example.com/picture.png",
      "links": [
        { "label": "Release v1.1.3.0", "url": "https://github.com/KloBraticc/Voidstrap/releases/tag/v1.1.3.0" }
      ]
    }
  ]
}
```

| Field | Required | Notes |
| --- | --- | --- |
| `id` | Yes | Unique, lowercase letters, digits and `-`, never changed once posted, likes and dislikes are saved under it |
| `date` | Yes | `YYYY-MM-DD` with leading zeros |
| `title` | Yes | Short headline in sentence case |
| `body` | Yes | Plain text, no links inside it |
| `image` | No | Direct link to a PNG, JPG or WEBP |
| `links` | No | Buttons under the post, each with a `label` and an `https` `url` |

## Writing posts

- Newest post first.
- Give every new post its own `id`, usually the date followed by the title in lowercase with `-` between words.
- Keep titles short, without exclamation marks or all caps.
- Put every link in `links`, never in `body`.
- Check the file is valid JSON before you push it.
