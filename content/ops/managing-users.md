---
menu:
  main:
    parent: users
title: Managing Users
---

## Note for GovCloud environment

Only single sign-on user accounts are allowed. Service accounts, such as deployer credentials, are permissible with the condition that they are scoped to a particular space with limited access.

No local accounts to UAA shall be created for user access.

## Creating users

The preferred way to invite new users is to [invite them](https://login.cloud.gov/invitations/new). If you need to create a user manually, follow the instructions for [the `provision-user-space` CLI plugin](https://github.com/18F/cf-provision-user-space-plugin).

## Changing passwords

First ask the user **[to try resetting their own password]({{< relref "getting-started/accounts.md#resetting-your-password" >}})**.

If a user logs in using their agency's account system, the only way to reset that password is for them to use their agency's normal password reset process.

If they log in with a cloud.gov account that has its own password (including `ORGNAME_deployer` accounts), you can [change their password for them](http://docs.cloudfoundry.org/adminguide/uaa-user-management.html#changing-passwords), using

```bash
uaac target uaa.cloud.gov
```

## Additional access

### Organizations and spaces

You can grant the user access to additional organizations and spaces by giving them additional [roles](http://docs.cloudfoundry.org/concepts/roles.html#roles). See [the instructions](https://docs.cloudfoundry.org/adminguide/cli-user-management.html#orgs-spaces) for changing them.

### Creating Admins

[Run the script.](https://github.com/18F/cg-scripts/#make-admins)
