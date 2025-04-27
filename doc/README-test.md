# Cert-Manager ACME DNS01 Webhook Solver for HE DNS

## testdata directory

Copy the example Secret files (testdata/secrets.yaml.example),
replacing `$HE_USERNAME` and `$HE_PASSWORD` with your
actual HE credentials:

```bash
export HE_USERNAME="<your HE username>"
export HE_PASSWORD="<your HE password>"
sed "s/%%HE_USERNAME%%/${HE_USERNAME}/; s/%%HE_PASSWORD%%/${HE_PASSWORD}/" testdata/he/secret.yaml.example > testdata/he/secret.yaml
```

## manual test you can do after deploying

see latest version on [repo page](https://github.com/mmoerz/cert-manager-webhook-he/pkgs/container/cert-manager-webhook-he/versions).

```
docker pull ghcr.io/mmoerz/cert-manager-webhook-he:latest
docker pull ghcr.io/mmoerz/cert-manager-webhook-he:${LATEST_VERSION}

```

helm chart manual test

```
helm show all oci://ghcr.io/mmoerz/charts/cert-manager-webhook-he --version 0.0.8
```
