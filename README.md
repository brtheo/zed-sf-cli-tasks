# 🚀 SF Zed Tasks

A comprehensive collection of **Salesforce CLI (sf)**, enabling seamless Salesforce development without leaving your modern editor.

While Zed tasks doesn't support prompting to user for input, this repo makes heavy use of [stew](https://github.com/brtheo/stew), a TUI that provides basic UI interaction with the SF cli.

## Why This Matters

Zed is the new default for modern developers thanks to its blazingly fast performance. Salesforce developers can now enjoy the same level of productivity and efficiency as their peers in other technologies.

## What You Get

This repository provides a ready-to-use task configuration that maps common Salesforce operations into Zed tasks, allowing you to:

- ⚡ **Execute Apex** — Run anonymous Apex code directly from your editor (file or selected text)
- 🧪 **Test with Confidence** — Execute Apex tests without context-switching
- 📦 **Deploy & Retrieve** — Deploy source or manifests to your org with a single command
- ✨ **Generate Artifacts** — Create Apex classes, triggers, and Lightning Web Components via interactive prompts
- 📊 **Query Data** — Run SOQL queries directly from your editor
- 🔑 **Manage Orgs** — Authorize, switch between, and open your Salesforce orgs

## Platform Support

- ✅ **Linux** — Full support with native task configurations
- ✅ **Windows** — Full support with Windows-compatible task configurations

## Quick Start

### Option 1: Copy for Your Platform

```bash
# For Linux users
cp linux/tasks.json ~/.config/zed/tasks.json

# For Windows users
cp windows/tasks.json %APPDATA%\zed\tasks.json
```

### Option 2: Merge with Existing Tasks

If you already have tasks configured, merge the new ones:

```bash
# For Linux users
jq -s 'add' linux/tasks.json ~/.config/zed/tasks.json > tasks_merged.json
mv tasks_merged.json ~/.config/zed/tasks.json

# For Windows users
jq -s 'add' windows/tasks.json %APPDATA%\zed\tasks.json > tasks_merged.json
mv tasks_merged.json %APPDATA%\zed\tasks.json
```


## Available features
| VS Code Salesforce Command | Zed Task Implemented? | Zed Task Label |
| :--- | :---: | :--- |
| **SFDX: Execute Anonymous Apex with Editor Contents** | ✅ | `SF::Apex::Run::Anonymous::File` |
| **SFDX: Execute Anonymous Apex with Currently Selected Text** | ✅ | `SF:Apex::Run::Anonymous::Selected` |
| **SFDX: Run Apex Tests** (Class level) | ✅ | `SF::Apex::Run::Test` |
| **SFDX: Deploy Source to Org** | ✅ | `SF::Deploy` |
| **SFDX: Deploy Manifest to Org** | ✅ | `SF::Deploy::Manifest` |
| **SFDX: Retrieve Source from Org** | ✅ | `SF::Retrieve` |
| **SFDX: Retrieve Manifest from Org** | ✅ | `SF::Retrieve::Manifest` |
| **SFDX: Create Apex Class** | ✅ | `SF::Gen::ApexClass` (via `stew`) |
| **SFDX: Create Apex Trigger** | ✅ | `SF::Gen::ApexTrigger` (via `stew`) |
| **SFDX: Create Lightning Web Component** | ✅ | `SF::Gen::LWC` (via `stew`) |
| **SFDX: Open Default Org** | ✅ | `SF::Org::Open` |
| **SFDX: Authorize an Org** / **Set Default Org** | ✅ | `SF::Org::Pick` (via `stew`) |
| **SFDX: Execute SOQL Query with Currently Selected Text** | ✅ | `SF::SOQL::Run::Selected` |
| **SFDX: Execute SOQL Query with Editor Contents** | ✅ | `SF::SOQL::Run::File` |
| **SFDX: Generate Manifest (package.xml)** | ✅ | `SF::Package::Generator` (via `stew`) |
| **SFDX: Create Project** | ❌ | *Missing* |
| **SFDX: Diff File Against Org** | ❌ | *Missing* |
| **SFDX: Refresh SObject Definitions** | ❌ | *Missing* |
| **SFDX: Cancel Active Deploy/Retrieve** | ❌ | *Missing* |
| **SFDX: Scan Current File with Code Analyzer** | ❌ | *Missing* |
