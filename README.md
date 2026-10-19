# Recalen

I designed and built a personal capture and recall app across web and native mobile, now being tested by 20+ people.

**[Read the illustrated case study](https://carsonmcrae.github.io/recalen/)** · **[Visit Recalen](https://recalen.com)**

![Recalen's local web beta with fictional demo entries and walkthrough commentary](https://carsonmcrae.github.io/assets/walkthrough/recalen-poster.webp)

Recalen's local web beta, populated with fictional demo entries. The guided tour below follows the actual interface.

## My role

I owned the original idea, product direction, interface design, development, and beta delivery.

## Results

Recalen has 20+ private-beta testers. Testing is ongoing, and several people use it daily.

## The problem

Thoughts, links, voice notes, and useful messages arrive before there is time to file them. I wanted a place to capture them quickly, keep their context, and find them again when they became useful.

## Product decisions

### Capture first, then decide what deserves to stay.

I gave entries temporary and permanent lifecycles. Temporary entries expire after 72 hours and pass through Trash; permanent entries remain available until the person removes them.

**Why I chose it:** A place to put a passing thought should not require a filing decision up front or make every small capture permanent.

**The tradeoff:** Expiry needs to be understandable and recoverable. Trash has a 30-day grace period before automatic permanent removal.

### Automated organization should respect a person's corrections.

I made generated categories, topics, entities, and related-entry suggestions assistive. Approved or manually added labels survive reprocessing; rejected labels stay rejected.

**Why I chose it:** If a person corrects the product, the next analysis should not undo that work.

**The tradeoff:** The system is conservative about suggestions and has to keep the history of user decisions.

### Offline capture should make a promise the app can keep.

I limited offline writes to new personal captures. The native app saves them durably and syncs them later. Cached browsing and search clearly describe their downloaded-only scope.

**Why I chose it:** Losing a thought, or creating duplicates after reconnecting, would undermine the reason to use a capture app.

**The tradeoff:** Edits and other network-dependent actions need a connection. Offline mode does not pretend to contain the entire account.

### Bring in selected emails without asking for the whole inbox.

I chose deliberate email forwarding to a personal Recalen address, with allowed senders, instead of mailbox synchronization.

**Why I chose it:** The useful information is the message someone chooses to keep. Capturing it should not require permission to scan everything else.

**The tradeoff:** People forward messages themselves. Recalen does not continuously discover or mirror mail.

### A reminder belongs to the thing the person meant to remember.

I kept plan-step reminders attached to stable steps when a plan is edited or reordered. Notes have their own document model, and references connect them to captured messages.

**Why I chose it:** Reorganizing a plan should not detach its reminders. A longer document should also be able to stand on its own.

**The tradeoff:** Notes, captured messages, and plan steps have distinct behaviors that need to stay consistent across web and mobile.

## Engineering depth

**390,720 lines of application source** across 1,991 files, plus **528,369 lines of tests and test support** across 1,999 files.

Saved coverage report (Aug 21, 2026): **100% lines and functions; 99.99% branches** for the measured executable source.

Source sizes measured October 19, 2026. Physical lines include comments and blanks; dependencies, generated output, assets, and lockfiles are excluded. Documentation and tooling are separate. Coverage uses its own configured source scope and report date.

[Measurement details](https://carsonmcrae.github.io/recalen/#engineering)


## Delivery scope

- Text, rich text, links, files, images, and voice capture
- Temporary and permanent feeds, folders, tags, and saved searches
- Search, assisted organization, and related-entry suggestions
- Notes, planning, reminders, and calendar views
- Selected email forwarding and account controls
- Native offline capture, cached reading, and push notifications

**Built with:** Next.js · TypeScript · React Native / Expo · PostgreSQL / Prisma · Clerk

## Status

Recalen is in ongoing private beta and has not had a public release. Some integrations depend on environment configuration. The public product URL currently provides the beta entry point.

This repository presents the product case study. Application source remains private.

## Explore the work

[Product walkthrough](https://carsonmcrae.github.io/recalen/#walkthrough)

[Watch the Recalen product film](https://carsonmcrae.github.io/recalen/#promo)

[Public beta roadmap](https://github.com/users/carsonmcrae/projects/1) · [Delivery snapshot](https://carsonmcrae.github.io/delivery/)

## More work

[Carson McRae](https://carsonmcrae.github.io/) · [GitHub](https://github.com/carsonmcrae) · [LinkedIn](https://www.linkedin.com/in/carsonmcrae/)
