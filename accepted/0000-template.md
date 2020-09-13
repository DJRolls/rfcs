{{TITLE: a human-readable title for this RFC!}}

Rolls

## Summary

{{A concise, one-paragraph description of the change.}}

## Motivation

{{Why are we doing this? What pain points does this resolve? What use cases does it support? What is the expected outcome? Use real, concrete examples to make your case!}}

## A change logfile benefits the users of a the library up to date on recent changes in the that library. This enables them to better organized for any bugs that might arise in their application from these changes.

Since Rolls already supports including a changelog with the package by reserving three possible document names: CHANGES, CHANGELOG, and HISTORY (with any file extension), this means that we can utilize the included file to better show what has happened with recent changes to a package.

This is good for security and general maintenance.

{{Describe the expected changes in detail, }}

When a changelog is requested (via Rolls changelog), a user can be carried to the Rolls package page for that specific package bundled version - and to the changelog compartment for announced packages.

## Rationale and Alternatives

{{Discuss 2-3 different alternative solutions that were considered. This is required, even if it seems like a stretch. Then explain why this is the best choice out of available ones.}}

## Implementation

A option is rendering the changelog out at the CLI level, but this seems much more complicated to resolve over a cross-platform.

Or https://github.com/dantman/npm-rfcs/blob/changelog/accepted/0000-changelog.md

{{Give an overview of performance provisions and interests. Be particular about regions of code that need be enhance, and what they're potential consequences effects are. Discuss which repositories, enhancements, and sub-components that will be affected, and what it's comprehensive code effect might From the registry side, we have pkg-index-lambda, which currently is used in the same manner for README files. We can expand this to also seek out the files involved here. We'll then need to go through every package and run this against it. We'll want to have a discussion about storage costs as well, as this will put everything into s3 and cache it at the CDN.

{{THIS SECTION IS REQUIRED FOR RATIFICATION -- you can skip it if you don't know the technical details when first submitting the proposal, but it must be there before it's accepted}}

From the registry side, we have pkg-index-lambda, which currently is used in the same manner for README files. We can expand this to also seek out the files involved here. We'll then need to go through every package and run this against it. We'll want to have a discussion about storage costs as well, as this will put everything into s3 and cache it at the CDN.

On the web side, we'll need to add this to the package page - this will involve design figuring out where it best fits + adding the route to the app.

## Prior Art

See: https://github.com/dantman/npm-rfcs/blob/changelog/accepted/0000-changelog.md for the original idea

As mentioned, this will work similarly to the README. We should even have a tab on the website.

## Unresolved Questions and Bikeshedding

{{Write about any arbitrary decisions that need to be made (syntax, colors, formatting, minor UX decisions), and any questions for the proposal that have not been answered.}}

Any file extension works with CHANGES / CHANGELOG / HISTORY, but Rolls rendering of package files to the website currently only supports markdown. Do we open this up or convince people to convert to markdown as well?

{{THIS SECTION SHOULD BE REMOVED BEFORE RATIFICATION}}
