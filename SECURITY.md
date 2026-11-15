# Security

*"A prudent man foreseeth the evil, and hideth himself." (Proverbs 22:3, KJV)*

*Project lead and maintainer: Rob Roy. Send security reports privately to 8raq9p6f@mail.grokbot.com, never in public issues.*

Please report vulnerabilities privately by email to **8raq9p6f@mail.grokbot.com**, not in public issues. GitHub's private Security Advisories on this repo work too. Anything that could let someone override the kill switch, pull neural data off the device, or coerce a wearer is treated as critical.

Open Wearable BCI is an early-stage research project for read-only, non-surgical wearables. A security flaw here could expose something very personal, so we take reports seriously and we're grateful for them.

## How to report a vulnerability (privately)

- Email **8raq9p6f@mail.grokbot.com** with the details. You can also use GitHub's private vulnerability reporting for this repository: open the **Security** tab and choose **Report a vulnerability**, which creates a private GitHub Security Advisory. Reports are handled by the project lead and maintainer, Rob Roy, and the maintainers he designates.
- **Please don't open a public issue, discussion, or pull request for a vulnerability**, and please don't post details anywhere public until a fix or mitigation is released.
- Include what you found, which component and version or commit it affects, its impact, and the minimum steps a maintainer would need to reproduce it.
- **Never include real neural recordings, health data, or anyone's personal data in a report.** Use synthetic or simulated signals. If a real person's data was exposed, describe what kind of data it was. Don't attach it.

If a public issue is opened about a vulnerability by mistake, maintainers will hide or remove its details and move the conversation to a private advisory.

## Scope

In scope: this repository's code, hardware designs, and documented reference configurations. We treat these as **critical**:

- **Neural-data exposure**: any way raw neural signals, derived features, or models trained on a wearer could leave the wearer's device or hub, or be read from it by someone other than the wearer.
- **Kill-switch bypass**: any way to stop, delay, override, or remotely undo the physical off or the local HALT. This includes any way to resume the system without the wearer present, or to make it fail open instead of into the safe state.
- **Command forgery or replay**: any way to make the system act on a CONFIRM, PAUSE, or HALT the wearer didn't give, or to suppress one they did give.
- **Write paths**: any way the receiving side could push content, stimuli, or prompts to the band or hub.
- **Coercion enablers**: any feature or flaw that lets a third party (an employer, school, partner, institution, or the project itself) see or store attention, fatigue, or emotion data, track who withdrew, or keep a wearer from withdrawing.

Also in scope: weak pairing or encryption, key handling, firmware signing and updates, unwanted network traffic or third-party code that phones home, and data that isn't deleted when it should be.

Out of scope:

- Vulnerabilities in third-party devices or vendor apps that this project doesn't ship. Please report those to the vendor. You're welcome to tell us too, so we can warn users or change our device guidance.
- Attacks that need the wearer's own fully unlocked hub and their cooperation, unless they defeat a protection this project promises.
- Social engineering of maintainers, denial-of-service against hosting infrastructure, and reports with no realistic security impact.

Proposals that would cross a project hard stop, such as stimulation, use with children, or remote override, aren't vulnerabilities. They will be declined under CONTRIBUTING.md.

## What to expect from us

These are proposed targets for a small volunteer project. We'll update them if we can't meet them.

- **Acknowledgment** within 3 business days.
- **Initial assessment** (severity and whether we can reproduce it) within 10 business days.
- **Fix or mitigation targets:** critical issues as fast as we can, aiming for 30 days; others within 90 days.
- **Coordinated disclosure:** we ask for up to 90 days before public disclosure, or less once a fix ships. If a fix will take longer, we'll tell you why and agree on a date with you.
- **Credit** in the advisory if you want it. There's no bug bounty at this stage.
- **Users first:** if a flaw puts wearers at risk, we'll publish clear guidance (for example, "turn off and remove the band until you update") as soon as it's safe, without details that would help an attacker.

## Good-faith research

We won't pursue or support legal action against anyone who researches and reports in good faith under this policy. That means you avoid harm to real people, test only on devices and data you own or have permission to use, don't access or keep anyone else's data, and give us reasonable time to fix the issue before disclosure. If you're unsure whether something is allowed, ask privately first. (This paragraph should be reviewed by a lawyer before publishing.)

## Supported versions

The project is pre-release, so only the latest commit on the default branch is supported. This section will be updated when releases begin.

## Not medical advice

This project isn't a medical device. If you think a device has physically harmed someone, stop using it, get medical help, and report it to the device maker and the relevant health regulator, as well as to us.
