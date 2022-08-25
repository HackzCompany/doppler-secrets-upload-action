# doppler-secrets-upload-action
Action to upload secrets to Doppler using a `.env` file

# Usage example
```yaml
doppler-sync:
    runs-on: ubuntu-latest
    needs: [install-deps, load-env]
    name: Doppler Sync
    steps:
      - uses: hackzcompany/doppler-secrets-upload-action@v2
        with:
          project: event-api
          token: ${{ secrets.DOPPLER_TOKEN }}
          config_name: dev
          env_file: env/dev.env
```

# Arguments

### `project`
The name of your Doppler project

### `token`
The token to access your Doppler project.

This can be a personal or a service token.

### `config_name`
The environment configuration name to point the upload to.

### `env_file`
The path to your env file.


# Maintainers
- Created by [@jgtvares](https://github.com/jgtvares)
- Maintained by [@HackzCo](https://github.com/HackzCompany) team
