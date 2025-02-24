# Infrastructure

This document is supposed to document all of the infrastructure that PyGreece owns. It
serves as a guide to new organizers and should be used to onboard new team members. It is
also supposed to be a reminder to all PyGreece organizers that maintaining the
infrastructure takes a lot of care and should be, together with updating this guide, a
regular thing.

## Google Workspace

PyGreece has a Google Workspace for Nonprofits organization.

### Users & user permissions

Every PyGreece organizer should have a user account under this organization. The naming
convention for our PyGreece emails is `<first_name>@pygreece.org`. Other naming schemes
may be used when a first name might conflict with others. User permissions should follow
the principle of least privilege. Hence, the permissions should be set up as follows:

- **PyGreece AMKE administrators**: They should be organization super-admins and have full
  control over the organization and billing.
- **PyGreece AMKE directors & PyGreece organizers**: They should be organization members
  with no admin control, unless permissions are needed for directors / organizers to be
  successful in fulfilling their board role.
- **PyCon GR organizers**: They should be organization members with no admin control,
  unless permissions are needed for PyCon GR organizers to be successful in fulfilling
  their organizer role. Organizers that solely handle PyCon organization tasks should get
  `pycon.gr` email addresses only.

External (non-organizer) users that regularly contribute to PyGreece-maintained projects
can request to get a `pygreece.org` email address, in case it's needed for them to be able
to effectively contribute to their projects.

> [!NOTE]
> There's currently also one Google Workspace account for `bot@pygreece.org`, the
> bot user that is used for registering any bot accounts with various services. Accounts
> like this should always get as little permissions as possible.

### Groups

The PyGreece organization has the following groups for easy management of group
communication:

- **PyGreece AMKE Administrators**: This should be the group used by administrators for
  account related to the AMKE's financials. Banking accounts, eAADE, GEMI, and others
  should use this account. PyGreece AMKE administrators are group owners.
- **PyGreece Security**: This should be a security-intensive group that only gives access
  to the necessary people. It should be used as the email for accounts that require higher
  levels of security, like password managers and others. It currently includes all
  PyGreece organizers, but that is not necessary and might change in the future. PyGreece
  AMKE administrators are owners, directors are managers, and other organizers are
  members.
- **PyGreece Organizers**: This is a group email that inlcudes all PyGreece organizers and
  should be used for internal meeting invitations, Google Drive sharing with multiple
  people, as well as external communications as a group. PyGreece AMKE administrators are
  owners, directors are managers, and other organizers are members.
- **PyGreece Subscriptions**: This account should be used as the default account to
  register for online services, like Github, Cloudflare, etc. PyGreece AMKE administrators
  are owners, directors are managers, and other organizers are members.
- **PyGreece CoC Committee**: This is a group email that should be listed as the email
  address for CoC incident reports. Members of the CoC committee should be using the email
  address for all CoC-related communications.

There's also Google groups used for PyCon organizers and the team managing its
organization:

- **PyCon GR Support**: Externally facing group email address. Should be used for all
  communications with attendees and should also be the email listed as the main point of
  contact on the PyCon GR website.
- **PyCon GR Sponsors**: This group email should be used by the Sponsors team for all
  communications/negotiations with potential sponsors.
- **PyCon GR Program**: Group email for the Program team. Can be used for communications
  with (keynote) speakers, and should be the point of contact listed on the CfP. Can also
  be used for CfP software (like pretalx), and others.
- **PyCon GR Organizers**: Interal group email for all PyCon GR organizers. Can be used
  for calendar events, internal communications, etc.

The permissions model is the following:

|                             | PyGreece AMKE Administrators | PyGreece Security | PyGreece Organizers | PyGreece Subscriptions | PyCon GR Support | PyCon GR Sponsors | PyCon GR Program. | PyCon GR Organizers |
| --------------------------- | ---------------------------- | ----------------- | ------------------- | ---------------------- | ---------------- | ----------------- | ----------------- | ------------------- |
| See group                   | Organization                 | Organization      | Organization        | Organization           | Organization     | Organization      | Organization      | Organization        |
| Join group                  | Invitation-only              | Invitation-only   | Invitation-only     | Invitation-only        | Invitation-only  | Invitation-only   | Invitation-only   | Invitation-only     |
| View conversations          | Owners                       | Members           | Members             | Members                | Members          | Members           | Members           | Members             |
| Post                        | Anyone                       | Anyone            | Anyone              | Anyone                 | Anyone           | Anyone            | Anyone            | Members             |
| View member                 | Organization                 | Organization      | Organization        | Organization           | Organization     | Organization      | Organization      | Organization        |
| Manage members              | Owners                       | Managers          | Managers            | Managers               | Managers         | Managers          | Managers          | Managers            |
| Modify custom roles         | Owners                       | Managers          | Managers            | Managers               | Managers         | Managers          | Managers          | Managers            |
| Contact group owners        | Anyone                       | Anyone            | Anyone              | Anyone                 | Anyone           | Anyone            | Anyone            | Members             |
| View member email addresses | Organization                 | Organization      | Organization        | Organization           | Organization     | Organization      | Organization      | Organization        |
| Reply privately to authors  | Anyone                       | Anyone            | Anyone              | Anyone                 | Anyone           | Anyone            | Anyone            | Members             |
| Attach files                | Anyone                       | Anyone            | Anyone              | Anyone                 | Anyone           | Anyone            | Anyone            | Members             |
| Moderate content            | Owners                       | Managers          | Managers            | Managers               | Managers         | Managers          | Managers          | Managers            |
| Moderate metadata           | Owners                       | Managers          | Managers            | Managers               | Managers         | Managers          | Managers          | Managers            |
| Post as group               | Owners                       | None              | Members             | None                   | Members          | Members           | Members           | None                |

> [!TIP]
> Some of the above settings need to be selected from the Google Admin console,
> while others need to be selected from the group settings on groups.google.com.

## Github

PyGreece has a nonprofit [organization account](https://github.com/pygreece) on Github.

### Users & user permissions

All PyGreece organizers should be part of our Github organization. Again, the principle of
least privilege should be used. That means the following in terms of user permissions:

- **PyGreece AMKE administrators**: They should be organization owners and have full
  control over the organization and billing.
- **PyGreece AMKE directors & PyGreece organizers**: They should be organization members
  with no admin control, unless permissions are needed for directors to be successful in
  fulfilling their board role.
- **PyCon GR organizers**: They should be organization members with no admin control,
  unless permissions are needed for directors to be successful in fulfilling their
  organizer role.
- **Contributors**: If a contributor needs organization access, they should be able to get
  it. All external contributors should be members with no admin access. Ideally,
  contributors should be added as outside collaborators to the specific repos they
  contribute to, though becoming an organization member is okay if they need it.

> [!NOTE]
> Our Github organization currently has a
> [bot member](https://github.com/pygreece-bot) as well. This is needed for some
> automations to run, like [Pulses](https://pulses.dev), etc. Any bot on our Github
> organization should have as little permissions as possible.

### Teams

- **community**: Organizers that are responsible for community outreach should be part of
  this team. It should give write access to all community-related private repositories.
- **org**: All organizers should be part of this team. It should give write access to all
  PyGreece private repositories.
- **translation**: Organizers that are responsible for the Python docs translation project
  should be in this team. It should not give write access to any repositories. Its main
  purpose is notifying groups of people for reviews, issue assignments, etc.
- **pycon25**: PyCon GR organizers that are responsible for tasks related to PyCon GR. It
  should give write access to all repositories that are related to PyCon GR. For each
  year's PyCon a new team should be created, so that old organizers do not lose access to
  the material produced during the organization of older PyCon's.

### Repositories

- [**community**](https://github.com/pygreece/community): The PyGreece community knowledge
  base. It serves as the primary collection of resources for all organizers and members.
  Also serves the wesite you're currently seeing. It should always remain public for
  anyone to contribute to.
- [**org**](https://github.com/pygreece/org): This repository serves as the main
  collection of issues and discussions needed for organizers to run their day-to-day
  tasks. It should be private. The `org` team should have write access to it.
- [**infrastructure**](https://github.com/pygreece/infrastructure): This repository serves
  as a place to host all infrastructure-related code and resources for PyGreece
  organizers. It is currently private, but could be made public in the future.
- [**discord**](https://github.com/pygreece/discord): The code for the PyGreece discord
  bot. It should always remain public for anyone to contribute to.
- [**org-pycon-2025**](https://github.com/pygreece/org-pycon-2025): This repository serves
  as the main collection of issues and discussions needed for PyCon organizers. It should
  be private. The `pycon25` team should have write access to it.
- [**pycon-gr-website**](https://github.com/pygreece/pycon-gr-website): This repository
  hosts the code and all of the needed infrastructure scripts for the `pycon.gr` website.
  It should be public, so that external contributors can also contribute to it. The
  `pycon25` and any future PyCon-related teams should have write access to it.

> [!NOTE]
> **python-docs-gr**: This repository hosts the translation of the Python document
> to the Greek language. It has been moved under the [python](https://github.com/python)
> organization.

## Domains

PyGreece currently owns four domains.

- **pygreece.org**: Serves as the main website for anything related to the PyGreece
  community. It currently is the home of the PyGreece knowledge base, but that might
  change in the future.
  - DNS Management: Cloudflare
  - Registrar: Cloudflare
  - Hosting solution: readthedocs.org
  - Repository: [Github](https://github.com/pygreece/community)
- **pygreece.eu**: Should be an alias to `pygreece.org`.
  - DNS Management: Cloudflare
  - Registrar: Name.com
- **pycon.gr**: Serves as the main website for PyCon Greece. It should include all content
  related to the conference, as well as any conference-related activities. It is currently
  empty, but will be populated soon.
  - DNS Management: Cloudflare
  - Registrar: [papaki](https://papaki.com)
- **pycongreece.gr**: Should be an alias to `pycon.gr`.
  - DNS Management: Cloudflare
  - Registrar: [papaki](https://papaki.com)

### Cloudflare

Cloudflare should be used for DNS management for all our domains, as well as for
registering domains, except for cases where it's not possible (`.gr` or `.eu` domains
currently cannot be registered through or transferred to Cloudflare).

#### Users & user permissions

- **PyGreece AMKE administrators**: They should be Super Administrators and have full
  control over all domains and billing.
- **PyGreece AMKE directors & PyGreece organizers**: They should be account administrators
  for all domains, but not have access to billing settings.
- **PyCon volunteers**: PyCon volunteers that are working on the PyCon website might need
  access to Cloudflare for the `pycon.gr` and `pycongreece.gr` domains. They should only
  get the permissions they need (typically DNS management) for these specific domains.

## Password management

The PyGreece team hosts a Vaultwarden server on our DigitalOcean infrastructure. It
implements a Bitwarden server and is open-source. Members of the team can install the
Bitwarden extension on their browser and point it to
[`https://vaultwarden.pygreece.org`](https://vaultwarden.pygreece.org), which is where our
password manager lives.

### Users

All PyGreece and PyCon organizers should have an individual account on our password
management solution and follow security best practices when it comes to storing their
passwords. PyGreece AMKE Administrators should be organization owners, while everyone else
should be an organization member. In addition to this, there should be two shared vaults
that multiple users have access to.

### Vaults

- **AMKE**: This vault should contain all passwords associated with PyGreece AMKE
  financial accounts, like banking accounts, eAADE, GEMI, etc. PyGreece AMKE
  administrators should have edit access.
- **Default collection**: This vault should contain all other passowrds to accounts that
  all PyGreece organizers should be able to log in to. PyGreece AMKE administrators and
  PyGreece organizers should have edit access.
- **PyCon**: This vault should contain password related to PyCon. PyGreece AMKE
  Administrators and PyGreece organizers should have edit access, while PyCon organizers
  should have read access.
