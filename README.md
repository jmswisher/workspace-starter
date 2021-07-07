<img src="./assets/OpenFin-Workspace-Starter.png" width="100%" alt="OpenFin Workspace Starter" />

## OpenFin Workspace

The OpenFin Workspace is a full-featured work environment designed to improve the way you get things done. Built on a secure browsing experience powered by Chromium, the core offering includes a smart digital assistant, a powerful web browser built to support modern application workflows out-of-the-box, and a notification system to surface important moments while they're still important.

- [Learn more about OpenFin Workspace](https://www.openfin.co/workspace/)

## What you can do with this repository

This repository contains an example showing how to configure core Workspace functionality for your application.

### Examples:

- [Learn how to launch your content in Workspace](./how-to/add-an-application-to-workspace)

## Before you get started

Be sure you have set up our [recommended development environment](https://developers.openfin.co/of-docs/docs/set-up-your-dev-environment).

OpenFin Workspace is currently **supported only on Windows**.

## Minimum RVM Version

To customize OpenFin Workspace you use DesktopOwnerSettings. This requires a minimum version of the OpenFin RVM. To find the version you currently have, do the following:

1. Using File Explorer, go to `%localappdata%/OpenFin`.
2. Right-click **OpenFinRVM** and select **Properties**.
3. Click  the **Details** tab and look for the value of **Product Version**.

Depending on your version the following rules will apply:

| RVM Version         | Supports Custom Workspace Settings | Setting Required            |
|---------------------|------------------------------------|-----------------------------|
| v6.0.0.3 & below    | No, you must upgrade in order to use this project | N/A          |
| v6.1.0.1 - v6.3.1.3 |                 Yes                | `openfinSystemApplications` |
| v6.4.1.1 & above    |                 Yes                | `systemApps`                |


### Example Desktop Owner Setting for OpenFinRVM v6.1.0.1 - v6.3.1.3

```json
{
  "desktopSettings": {
    "openfinSystemApplications": {
      "home": {
        "customConfig": {
        }
      }
    }
  }
}
```
### Example Desktop Owner Setting for OpenFinRVM v6.4.1.1 & Above

```json
{
  "desktopSettings": {
    "systemApps": {
      "home": {
        "customConfig": {
        }
      }
    }
  }
}
```
