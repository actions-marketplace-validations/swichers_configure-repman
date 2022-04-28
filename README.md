# Configure Repman

A GitHub action for configuring composer to use Repman.

## Usage

```yml
      - uses: actions/checkout@v3

      - uses: swichers/configure-repman@v1
        with:
          token: ${{ secrets.REPMAN_TOKEN }}
          organization: swichers

      - uses: "ramsey/composer-install@v2"

      # Composer should be able to access Repman based packages.
```

## Action inputs

All inputs are required.

| Name           | Description                                                       |
|----------------|-------------------------------------------------------------------|
| `token`        | A Repman access token.                                            |
| `organization` | The organization machine name available from your Repman settings |

It is recommended to use a secret configured in GitHub instead of hard coding the Repman access token.
