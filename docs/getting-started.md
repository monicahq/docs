---
sidebar_position: 1
---

# Getting started

Monica aims to document someone's life. Your life is a series of events that happens to you, and a series of interactions with the people close to you, personally or professionally. By documenting what's happening to you, and what happens to others, we believe we can improve everyone's life greatly.

At its core, Monica has a few key concepts:

* accounts,
* vaults,
* contacts.

An account is what users sign up for when they register to Monica. It's the root element of Monica and contains everything needed to manage your data. The person who signs up for an account will be the first administrator of the account. You can add other administrators if you want in the future, but an account needs at least one administrator. You can also add other users who won't be administrators.

A vault hosts user's data – basically contacts, documents etc... An account can have as many vaults as needed. Vaults are private inside an account. This means that other users in the account, even if they are administrators of the account, can't read the data in a vault if there are not part of this vault. They can’t even see that the vault exists, for that matter.

A contact is the core data of Monica. It's someone you know (or think you know). A contact lives inside a vault.





## Getting Started

Get started by **creating a new site**.

Or **try Docusaurus immediately** with **[docusaurus.new](https://docusaurus.new)**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 14 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.

## Generate a new site

Generate a new Docusaurus site using the **classic template**.

The classic template will automatically be added to your project after you run the command:

```bash
npm init docusaurus@latest my-website classic
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

The command also installs all necessary dependencies you need to run Docusaurus.

## Start your site

Run the development server:

```bash
cd my-website
npm run start
```

The `cd` command changes the directory you're working with. In order to work with your newly created Docusaurus site, you'll need to navigate the terminal there.

The `npm run start` command builds your website locally and serves it through a development server, ready for you to view at http://localhost:3000/.

Open `docs/intro.md` (this page) and edit some lines: the site **reloads automatically** and displays your changes.
