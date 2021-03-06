# Management

[[toc]]

## Recipes

Recipes allow you to save common Bash scripts and run them across any of your servers. For example, you could save a recipe to install MongoDB so you can conveniently run it on future servers. The output of the recipe will be e-mailed to you.

### Creating Recipes

You can create your own recipe from the [Recipes](https://forge.laravel.com/recipes) page. When creating a new recipe you will be asked to supply:

- Name of the recipe
- User to run the script as (`root` or `forge`)
- Script contents

#### Variables

Forge provides a few variables that can be used to make your recipe more dynamic:

<div v-pre>

- `{{server_id}}` - The ID of the server that the recipe is running on
- `{{ip_address}}` - The public IP address of the server.
- `{{private_ip_address}}` - The private IP address of the server.

</div>

When used in a recipe, variables must exactly match the syntax shown above.

### Managing Recipes

Your existing recipes will be listed on the [Recipes](https://forge.laravel.com/recipes) page, which is where you can edit, run and delete them.

### Running Recipes

When running a recipe, you will be presented with options that allow you to have the output of the recipe emailed to you and allow you configure which servers the recipe will run on.

## Security

Typically, security updates are automatically applied to your server on a weekly basis. Forge accomplishes this by enabling and configuring Ubuntu's automated security update service that is built-in to the operating system.

Forge does not automatically update other software such as PHP or MySQL automatically, as doing so could cause your server to suffer downtime if your application's code is not compatible with the upgrade.

## IP Addresses

If your servers IP address changes you will need to inform Forge so that it can remain connected and continue to manage your server.

To update the IP address of a server, go to the Meta tab and update the **IP Address** field under the Server Metadata section.

:::tip Rebooting an AWS Server

When rebooting an AWS server, AWS will allocate a new IP address to the server. You will need to update the IP address after a reboot.

:::

## Archiving Servers

You may archive a server from the Forge UI by clicking the **Archive** button at the bottom of the server's detail page.

:::warning No Data Loss
Archiving a server will not delete your server from the provider and will leave all data intact. The server will no longer display in listings within the Forge UI.
:::

## Transferring Servers To Other Users

Servers may be transferred to other Forge accounts from the server's "Meta" tab by providing the email address of the other Forge account.

The receiving Forge account will be sent an email address asking them to confirm the request.

:::tip Paid Accounts Only
You may only transfer servers to a paid account that has not met its server number limits.
:::

## Server Logs

Forge provides the ability to view server log files from within the dashboard. You should select a log file from the **View Log** dropdown.

For performance reasons, Forge will only return the last 500 lines from a file. The log file path will be shown in both the dropdown and at the bottom of the log output.
