# SFMC Standard Roles Backup

As the [default System Roles permissions](https://mateuszdabrowski.pl/docs/config/sfmc-config-permissions/) in Salesforce Marketing Cloud can be edited freely and [currently there is no easy way to revert those changes](https://ideas.salesforce.com/s/idea/a0B8W00000KSOTSUA5/), I created this repository to let you check what are the out-of-the-box configurations.

## Structure

You can see two folders in this repository with backups for different purposes.

### Roles Documentation

Here you can find .tsv files (tab separted values) with full description of all the Standard Roles.

In each row you can find full path to each permission along with its checkbox value (first for Allow checkbox, second for Deny checkbox). It allows you to:

1. Manually check what are the differences in specific permissions between your configuration and the default one documented in this repo.
2. Make a batch comparision by leveraging my [extaction script](https://mateuszdabrowski.pl/docs/js/js-snippet-export-import-document-sfmc-roles/#document-sfmc-roles) on your Role and comparing the outcome with the one available here in a difference comparision tool, for example, free [DiffChecker](https://www.diffchecker.com).

Those files can be easily imported into Excel or Google Sheets and converted into three-column table.

### Roles Import Files

Here you can find cryptic .json files that - while not really readable - enable you to revert your Standard Roles to their out-of-the-box version with help of my [role importing script](https://mateuszdabrowski.pl/docs/js/js-snippet-export-import-document-sfmc-roles/#importing-a-sfmc-role).

## Considerations

The Standard Roles and available Permissions are changing from SFMC Release to Release. I will try to keep this repository updated with most recent version of the default roles, but before importing the role I highly recommend checking whether the Documentation version is aligned in terms of the available permissions.

If there will be some new permissions in your system that are not visible in the documentation file stored here - don't use the import. It might create issues with the configuration. Let me know about the problem and I will update it to the latest version.
