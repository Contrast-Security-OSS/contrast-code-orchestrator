# Contrast CI Orchestrator

Shared GitHub Actions reusable workflow that runs Contrast Security code products
(Contrast Code, Contrast SCA, SmartFix) on your repository.

## Usage

This workflow is called automatically by the `contrast-ci.yml` file installed
by the Contrast GitHub App. You do not need to reference this workflow directly.

## Products

| Job | Product                        | Trigger |
|---|--------------------------------|---|
| `detect-languages` | repository language detection  | All events |
| `detect-app-data` | Application ID/Name detection  | All events |
| `run-contrast-code` | SAST scanning                  | All events |
| `run-sca` | static SCA dependency scanning | All events |
| `run-smartfix` | AI fix PR generation           | PR close, dispatch, schedule |

## Disabling Products

Set the appropriate flag in your `contrast-ci.yml`:

disable_contrast_code: 'true'
disable_contrast_sca:  'true'
disable_smartfix:  'true'

## Support

Contact your Contrast Security account team: [support@contrastsecurity.com].
