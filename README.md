# synt0x

**→ [synt0x.com](https://synt0x.com/)**

Hi, I'm synt0x. I spent years building software before I moved to breaking and securing it, and this is where I write things down: writeups, research, the checklists I actually use in reviews, and small security tools that run in your browser.

I write the way I'd want to read: what the risk is, what I decided, what it cost, and what I'd still do differently.

## What you're looking at

This repository is only the **build output** of the site. I write it in a separate repository, [Hugo](https://gohugo.io/) builds it, and a GitHub Actions workflow pushes the result here. Every commit here is an automated `Deploy <commit>` that the next build overwrites, so a pull request against these files has nowhere to go. If you spot something, open an issue instead. I read them.

## How the site is built

A security site should practice what it preaches, so I held this one to the same standard I'd hold a client's:

- **Static only.** No server-side code, no database, no admin panel to attack.
- **No trackers, no analytics, no cookies, no third-party requests.** Fonts, styles and scripts all come from this origin.
- **A strict Content Security Policy** (`default-src 'none'`, everything else `'self'`), no inline scripts or styles, and Subresource Integrity on every stylesheet and script.
- **Search runs in your browser** ([Pagefind](https://pagefind.app/)). The index is built at deploy time, so your queries never leave the page.
- **The tools run in your browser too** and make no network requests. A token or payload you paste in stays on your machine.

## Getting in touch

| What                                 | Where                                                                                  |
| ------------------------------------ | -------------------------------------------------------------------------------------- |
| Typo, broken link, rendering problem | [open an issue](../../issues) in this repository                                       |
| Security issue in the site or a tool | see [`security.txt`](https://synt0x.com/.well-known/security.txt) (RFC 9116) |

If you found a security issue, please don't put it in a public issue. Use the contact in `security.txt`, and I'll get back to you.
