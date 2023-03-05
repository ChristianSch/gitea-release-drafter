# gitea-release-drafter

_Gitea Release Drafter_ automates release notes as a draft release whenever a pull request finds it's way into the default branch of your repository.

⚠️ This action is compatible with gitea and forgejo starting from version `1.19.0`.

![Screenshot 2023-03-05 at 23 05 12](https://user-images.githubusercontent.com/6138133/222988558-5e99e5b4-9955-4650-9ce6-6d565dd85f34.png)

## Using The Release Drafter

...

`config-path` to set the location of the action configuration. Defaults to `.gitea/release-drafter.yml`

## Example Configuration

```
name-template: 'v$RESOLVED_VERSION 🌈'
tag-template: 'v$RESOLVED_VERSION'
version-resolver:
  major:
    labels:
      - 'major'
  minor:
    labels:
      - 'minor'
  patch:
    labels:
      - 'patch'
  default: patch
```

## Configuration Variables

- `RESOLVED_VERSION`: the proposed version for the next release (does not contain the leading `v`)
