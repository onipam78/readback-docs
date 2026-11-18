# Readback — Privacy Policy

Last updated: 2026-11-18

Readback is an app for Jira and Confluence Cloud built on Atlassian Forge by Readback Labs ("we"). This policy describes what the app stores and why.

## Where the app runs

Readback runs entirely on Atlassian Forge. Its code, its database (Forge SQL) and its logs are hosted by Atlassian, in the same infrastructure as your Jira and Confluence site. The app makes no network calls to any service outside Atlassian, and we operate no servers of our own for it. The app itself does not call any AI or language-model service. If you use the Readback agent in Rovo, the agent is run by Atlassian; the app only returns the results of its read-only checks to it.

## What the app stores

In its Forge SQL database, per installation:

- **Controlled documents**: the Confluence page ID, space key, page title, the document code you assign, the scope JQL you enter, and the Atlassian account ID of the document owner.
- **Revisions**: the page version number, a hash of the page body, the change summary and key points entered by the owner, effective and due dates, and the account ID of the person who released the revision. The page body itself is not stored.
- **Read-back requests**: the Atlassian account ID and display name of each person asked to read back, the Jira work item keys that caused the request, and the status of the request (pending, read back, waived, released).
- **Ledger**: an append-only record of events (control, release, request, read-back, waiver, gate decisions, exports). Entries contain account IDs, document codes, revision numbers and work item keys.
- **Organisational context**: names and IDs of goals, teams and related pages returned by Atlassian's Teamwork Graph for a revision.

Account IDs and display names are personal data. The app stores them because the purpose of the app is to record who was asked to read a procedure and who confirmed it.

## What the app does not store or do

- It does not store page content, attachments, Jira work item content or comments.
- It does not store email addresses, passwords or tokens.
- It does not send any data outside Atlassian's infrastructure.
- It does not use data for advertising, profiling or analytics.

## What the app writes to your site

- A comment on each affected Jira work item when a major revision is released. The comment contains the document code, the revision number, the change summary entered by the owner, the due date, a link to the Confluence page and a mention of the assignee. It is visible to everyone who can view that work item.
- An error message on a blocked workflow transition, naming the assignee, the document code and the revision number.

## Who can see the data

Readback checks the viewer's own Jira and Confluence permissions before showing a document or a work item. The ledger can be listed and exported only by Jira administrators and, for their own documents, by document owners. We (the vendor) have no access to the data in your installation, other than operational logs and metrics that Atlassian makes available to app developers; the app does not write page content, tokens or personal details to those logs.

## Retention and deletion

Data is kept for as long as the app is installed, because the ledger is intended to be a lasting record. Retiring a document stops new requests but keeps its history. When the app is uninstalled, Atlassian deletes the app's storage for that installation according to the Forge hosted storage data lifecycle.

If a person asks for their personal data to be erased, open an issue at https://github.com/onipam78/readback-docs/issues (do not put the personal data itself in the issue; we will arrange a private channel). Note that removing a person's entries from the ledger breaks the tamper-evident chain for the entries that follow; we will tell you what that means for your records before anything is removed.

## Sub-processors

Atlassian Pty Ltd (Forge hosting, storage and logs). No others.

## Changes

We will update this page when the app changes what it stores. The date at the top shows the last update.

## Contact

Open an issue at https://github.com/onipam78/readback-docs/issues
