# Contrast Code Orchestrator

Shared GitHub Actions reusable workflow that runs Contrast Security code products
(SmartScan, SmartSCA, SmartFix) on your repository.

## Usage

This workflow is called automatically by the `contrast-security.yaml` file installed
by the Contrast GitHub App. You do not need to reference this workflow directly.

## Products

| Job | Product                          | Trigger |
|---|----------------------------------|---|
| `detect-app-data` | Application ID/Name detection    | All events |
| `run-smartscan` | SAST scanning          | All events |
| `run-sca` | SCA dependency scanning      | All events |
| `run-smartfix` | AI fix PR generation    | PR close, dispatch, schedule |

## Disabling Products

Set the appropriate flag in your `contrast-security.yaml`:

disable_smartscan: 'true'
disable_smartsca:  'true'
disable_smartfix:  'true'

## Support

Contact your Contrast Security account team: [support@contrastsecurity.com].
