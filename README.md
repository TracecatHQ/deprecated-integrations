# Deprecated Registry

> [!IMPORTANT]
> Integrations and actions in this repository are deprecated as of v0.23.
> We recommend replacing all actions under the `integrations.` namespace with new actions under the `tools.` namespace.

This repository contains a registry for deprecated actions and integrations.
You can also use this as a template to add your own custom registry to Tracecat.

## Getting Started

1. Create a new repo from the template

<img width="905" alt="Screenshot 2025-02-05 at 1 24 59 PM" src="https://github.com/user-attachments/assets/5a5f532b-857f-4ed3-af17-c91b84f1a65a" />

2. Configure remote repo URL

Go into `Organization` settings and configure the remote repo URL to point to your private repository.

![Remote Repo URL](/img/git-repo.png)

3. Create a deploy key in GitHub

Create a SSH key pair. Store the public key in GitHub.

![Deploy Keys](/img/deploy-keys.png)

4. Add the private key to Tracecat

Add the private key to Tracecat as a SSH key secret with the name `github-ssh-key`.

![SSH Key](/img/ssh-key.png)

5. Sync the repository

Go to the `Registry` page and select `Repositories.`
Press refresh repositories to see your new custom repository.
Then, under `custom_actions` settings, press `Sync` to sync the repository.

![Sync repository](/img/sync.png)
![Sync confirmation](/img/sync-confirm.png)

6. View custom actions

> [!NOTE]
> If you're still on v0.22.x and under, `integrations.` namespaced actions will be still visible under `tracecat_registry`.
> After updating to v0.23, you should see the `integrations.` namespaced actions under the custom git repo origin.

Go to the `Actions` page and filter by `Origin` to view synced actions.

![Actions](/img/actions.png)


7. 🎉 That's it!

Feel free to remove or add your own custom Python UDFs actions and YAML template actions to the registry.
Just push to your git repo, press sync in Tracecat registry, and updates will show up immediately.
