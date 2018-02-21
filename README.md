# Discussions

> DLang-community is a GitHub organization which maintains D packages that are
important to the D ecosystem.

About the organization
----------------------

This organization was formed by annoyance of needing to fork popular repositories to get fixes merged.
Similarly to `std.experimental` projects are still driven by their original authors if they have the time.
However, small bug fixes don't need to wait in the queue for months and in case the author is completely gone
the DLang community has one upstream repository instead of ten different forks containing the same fix.
Moreover, thanks to being a larger organization the overhead of a project can be
distributed and more easily automated (e.g. documentation builds, binary releases etc.).

Getting in touch
----------------

This is public discussion list based on [GitHub issues](https://github.com/dlang-community/discussions/issues).

Do you have a question?
Then don't hesitate to [open an issue](https://github.com/dlang-community/discussions/issues/new)!

Adoption guidelines
-------------------

These question are intended to give a rough feeling on what packages might be considered for adoption.
In doubt, please open an issue!

### Popularity

Q: Is there enough interest from the D community, s.t. it is "worth maintaining"?

### Competition

Q: Is there a similar library with active development out there?

### Maintainer/sponsor

Q: Is at least one of the DLang community member competent for the domain covered by the project?
   If no is there anyone who's willing to join?

Best practices
--------------

This is a list of requirements that should be enabled for each repository.
It's not a requirement for adoption, but a reminder for DLang community members.

### GitHub branch protections

GitHub branch protections (https://github.com/dlang-community/X/settings/branches)
are very important to avoid accidentally pushing to `master`. All repos should have
these two checks enabled:
- Master branch should be set to "force-push protected"
- "Require status checks to pass before merging" should be set

### CI integration

To prevent regressions, assist reviewers and help improving the D ecosystem stability
all changes should be tested as extensively as possible:

- Travis (Linux, OS X)
  - Enable daily crons
- AppVeyor (Windows)
- Test the following compilers
  - `dmd`, `dmd-beta`, dmd-nightly
  - `ldc`, `ldc-beta`

### DUB

All repos should be published on the DUB registry.

### Automated generation (TBD)

- Automated documentation generation (TBD)
- Automated binary generation (TBD)

Guidelines
----------

### Q: When can I (self)-pull a PR?

- Allowed without CI: typos, Readme changes, etc.
- Allowed to pull immediately: critical bug fixes that pass the CI (critical = breakage with dmd-nightly or obviously wrong)
- Allowed without a reply within a few days: bug fixes that pass the CI
- Do _not_ pull new features without approval (if the original author is still present, new features should be approved by him)


These guidelines are WIP - [your feedback](https://github.com/dlang-community/discussions/issues) is welcome!

### Q: What should I do when I want to move a package to dlang-community?

Please open an issue and let's have a discussion - we don't bite!
Don't create new package _without_ consulting other dlang-community members.


How do I become a member of the DLang community?
------------------------------------------------

First of all, by reading this you most likely are already.
For this GitHub community there are two options:
You are already a well-known member of the D community, then simply [ping us](https://github.com/dlang-community/discussions/issues/new) for merge rights.
Otherwise, start contributing to one of the projects and earn your trust.
