# Terrarium

> a tiny wrapper for Terraform to make loading env vars transparent by convention

see https://github.com/terrarium-tf/cli for concrete usage of `terrarium`

## Use within Github-Actions

```yaml
jobs:
  global:
    - name: Configure AWS credentials
      uses: aws-actions/configure-aws-credentials@v1
      with:
        aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
        aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
        aws-region: eu-central-1

    - name: Setup Terraform
      uses: hashicorp/setup-terraform@v1

    - name: Setup Terrarium
      uses: terrarium-tf/github-action@0.1

    - name: "default/foo stack"
      run: terrarium apply default stacks/foo

```

## TODO

* tests
