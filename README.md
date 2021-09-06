# Terraform Provider Hasura

This is a Terraform provider for Hasura.

## Build provider

Run the following command to build the provider

```shell
$ go build -o terraform-provider-hasura
```

## Local release build

```shell
$ go install github.com/goreleaser/goreleaser@latest
```

```shell
$ make release
```

You will find the releases in the `/dist` directory. You will need to rename the provider binary to `terraform-provider-hasura` and move the binary into the appropriate subdirectory within the user plugins directory.
## Test sample configuration

First, build and install the provider.

```shell
$ make install
```

Then, navigate to the `examples` directory.

```shell
$ docker-compose -f docker_compose/docker-compose.yml up
$ cd examples
```

Run the following command to initialize the workspace and apply the sample configuration.

```shell
$ terraform init && terraform apply
```
