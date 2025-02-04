# Deprecated Registry

> [!NOTE]
> Integrations and actions in this repository are deprecated as of v0.23.
> We recommend replacing all actions under the `integrations.` namespace with new actions under the `tools.` namespace.

This repository contains a registry for deprecated actions and integrations.
You can also use this as a template to add your own custom registry to Tracecat.

## Getting Started

1. Clone the repository.
```bash
git clone git@github.com:TracecatHQ/deprecated-integrations.git
```

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

![Sync repository](/img/sync-repo.png)

> [!NOTE]
> You might encounter an error the first time you sync the repository.
> You can safetly ignore this error and try to sync again.

6. View custom actions

Go to the `Actions` page and filter by `Origin`.
You should see all the pre v0.22 actions and integrations.

![Actions](/img/actions.png)
