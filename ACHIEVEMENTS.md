# GitHub profile achievements

Every badge GitHub currently awards, what actually earns it, and what it costs.
The criteria are not documented by GitHub anywhere official — what follows is
the community-established list plus what this repository proved by testing it.

## The rule that is not written down anywhere

**A merged pull request counts once per calendar day.** Three pull requests
merged inside one minute advance Pull Shark by **one**, not three. This is the
reason a profile can show three merged PRs and no Pull Shark badge, and it is
why the fix is patience rather than volume.

Two other constraints apply to everything below:

- **Public repositories only.** Work in a private repository earns nothing,
  whatever it is.
- **Refresh is asynchronous.** Quickdraw and YOLO appear within minutes; the
  counted ones take hours, and community reports run to days.

## Earnable

| Badge | What earns it | Tiers |
| --- | --- | --- |
| **Quickdraw** | Close an issue or pull request within 5 minutes of opening it | 1 |
| **YOLO** | Merge a pull request with no review | 1 |
| **Pull Shark** | Open pull requests that get merged — one per calendar day | 2 / 16 / 128 / 1024 |
| **Pair Extraordinaire** | A merged pull request whose commit carries a `Co-Authored-By:` trailer | 1 / 10 / 24 / 48 |
| **Galaxy Brain** | Have an answer accepted in a repository's Discussions | 2 / 8 / 16 / 32 |
| **Starstruck** | Own a repository that reaches the star count | 16 / 128 / 512 / 4096 |
| **Public Sponsor** | Sponsor anyone through GitHub Sponsors | 1 |

### What each one actually needs

**Quickdraw.** Open an issue, close it. Ten seconds is enough. The only badge
with no waiting and no second party.

**YOLO.** Merge your own pull request without requesting a review. It arrives
alongside the first Pull Shark merge and needs nothing extra.

**Pull Shark.** The pull request must be merged — not closed — into the
repository's **default branch**, and not into a fork. Drafts do not count.
Tier 1 therefore takes **two days minimum**, whatever the volume.

**Pair Extraordinaire.** The trailer has to resolve to a real GitHub account, or
nothing is credited:

```
Co-Authored-By: name <ID+username@users.noreply.github.com>
```

The numeric ID comes from `gh api users/<username> --jq .id`. Both the author
and the co-author earn the badge, so a second account you control earns it for
both at once. Check it landed by opening the merged commit — GitHub shows the
co-author's avatar beside yours.

**Galaxy Brain.** Needs Discussions enabled on a repository, a discussion in an
**answerable** category, and an answer marked accepted. Only the answer's author
earns it, and tier 1 wants **two** accepted answers.

**Starstruck.** Sixteen stars from sixteen accounts. The only badge here that
cannot be arranged — it needs other people to want the repository.

**Public Sponsor.** A real payment to a real maintainer through GitHub Sponsors.
Cheap, and the one badge that does somebody else some good.

## Retired

Nothing can earn these now; they only persist on profiles that already hold
them.

| Badge | Was earned by |
| --- | --- |
| **Arctic Code Vault Contributor** | Code in a repository captured by the 2020 GitHub Archive Program |
| **Mars 2020 Contributor** | Code in a repository used by the Mars 2020 Helicopter Mission |
| **Heart On Your Sleeve** | Reactions. Never officially documented, and no longer awarded |
| **Open Sourcerer** | Never officially documented, and no longer awarded |

## Where the badges are read from

Achievements are rendered into the profile page by a separate fragment rather
than the page itself, so fetching `github.com/<user>` and grepping it finds
nothing. The profile in a browser is the only reliable check.
