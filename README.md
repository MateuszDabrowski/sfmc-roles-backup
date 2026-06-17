# SFMC Standard Roles Backup

As the [default System Roles permissions](https://mateuszdabrowski.pl/docs/config/sfmc-config-permissions/) in Salesforce Marketing Cloud can be edited freely and [currently there is no easy way to revert those changes](https://ideas.salesforce.com/s/idea/a0B8W00000KSOTSUA5/), I created this repository to let you check what are the out-of-the-box configurations.

## Structure

You can see three folders in this repository with backups for different purposes.

### Roles Backup v2

Here you can find the new approach with a single file covering both Documentation and Importable data in more user friendly .csv format.

In each row you can find full path to each permission along with its checkbox id and value. It allows you to:

1. Manually check what are the differences in specific permissions between your configuration and the default one documented in this repo.
2. Make a batch comparision by leveraging my [extaction script](https://mateuszdabrowski.pl/docs/js/js-snippet-export-import-document-sfmc-roles/#export-mce-roles) on your Role and comparing the outcome with the one available here in a difference comparision tool, for example, free [DiffChecker](https://www.diffchecker.com).
3. Revert your Standard Roles to their out-of-the-box version with help of my [role importing script](https://mateuszdabrowski.pl/docs/js/js-snippet-export-import-document-sfmc-roles/#import-mce-role).
4. Duplicate or migrate any roles across Orgs.

Those files can be easily imported into Excel or Google Sheets and converted into a nice table, but it's good to keep them as .csv files for imports.

### Roles Documentation v1

Here you can find the old Documentation approach with .tsv files (tab separted values) with full description of all the Standard Roles. Now you can document them using new Roles Backup v2.

### Roles Import Files v1

Here you can find old import approach with cryptic .json files that - while not really readable - enabled you to revert your Standard Roles to their out-of-the-box version. Now done by new Roles Backup v2.

## Considerations

The Standard Roles and available Permissions are changing from MCE Release to Release. I will try to keep this repository updated with most recent version of the default roles, but before importing the role I highly recommend checking whether the Documentation version is aligned in terms of the available permissions.

If there will be some new permissions in your system that are not visible in the documentation file stored here - don't use the import. It might create issues with the configuration. Let me know about the problem and I will update it to the latest version.
