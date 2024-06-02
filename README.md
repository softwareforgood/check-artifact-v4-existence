Check Artifact v4 Existence
====

A composite Github Action inspired by the very awesome [xSAVIKx/artifact-exists-action](https://github.com/xSAVIKx/artifact-exists-action)

Checks if an artifact with a given name, uploaded with actions/upload-artifact@v4, exists. Only works with the actions/upload-artifact v4 and later, not versions v1-v3.

## Inputs

- **name (required)** - Name of the artifact to check

## Outputs

- **exists** - Whether the artifact exists and could be downloaded. `true` if it the artifact was downloaded, `false` it couldn't be downloaded. It could also be `null` if something  in the composite workflow failed and it never couldn't got to the end, if the `download-artifact` call was skipped
or something else strange happened.

## Example usage

```yaml
- uses: softwareforgood/check-artifact-v4-existence@v0
  with:
    name: "example-artifact"
```
