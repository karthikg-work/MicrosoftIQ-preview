# Install the latest stable Work IQ plugin

This repository contains the separate `workiq-preview` plugin. To install Microsoft's current stable Work IQ plugin and its latest published skill bundle in GitHub Copilot CLI, use the official `microsoft/work-iq` marketplace. This installs the complete published plugin, including its skills and references, rather than copying an incomplete snapshot into this preview repository.

The official catalog currently lists stable `workiq` version **3.0.0**. Verify the catalog for updates before installation: [microsoft/work-iq/PLUGINS.md](https://github.com/microsoft/work-iq/blob/main/PLUGINS.md).

## Install in Copilot CLI

Start the CLI in a terminal:

```sh
copilot
```

Then enter these commands in the Copilot CLI session:

```text
/plugin marketplace add microsoft/work-iq
/plugin install workiq@work-iq
```

Restart the Copilot CLI session after installation so the new skills are loaded. Use `/plugin list` to check the installed plugins.

## Preview and stable are separate

Installing stable does not replace or remove this repository's `workiq-preview` plugin. If both are enabled, follow the version/precedence guidance in their skills for overlapping requests. To use stable only, uninstall the preview plugin through the host's plugin manager before restarting:

```text
/plugin uninstall workiq-preview
```

## Availability and consent

The plugin uses the hosted WorkIQ MCP service at `https://workiq.svc.cloud.microsoft/mcp`. Sign-in, tenant consent, licensing, and available tools depend on the Microsoft 365 tenant. Installing the plugin does not itself grant access or guarantee that a given tool or retrieval strategy is enabled.

More information: [official Work IQ plugin guide](https://github.com/microsoft/work-iq/blob/main/plugins/workiq/README.md).
