# Dojo Update

Update Your Dojo!

## GitHub Action

`.github/workflows/update.yml`:
```yml
name: Update Dojo

on: push

jobs:
  update:
    runs-on: ubuntu-latest
    steps:
      - uses: pwncollege/dojo-update@v1
        with:
          dojo: <YOUR DOJO ID HERE>
          update_code: ${{ secrets.UPDATE_CODE }}
```

### Inputs
- `dojo`: The reference id of your dojo, for example `official-dojo` or `unofficial-dojo~1a2b3c4d`.
- `update_code`: The update code of your dojo.

The `update_code` should be a secret, so you should [add it to your repository's secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets?tool=webui#creating-encrypted-secrets-for-a-repository).
In the above example, the secret has been named `UPDATE_CODE`.
