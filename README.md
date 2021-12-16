# github-action-validate-envoy-proxy

GitHub Actions to validate [Envoy Proxy](https://www.envoyproxy.io/) Configuration.

## How does it works?

This action executes `envoy` with [--mode validate](https://www.envoyproxy.io/docs/envoy/latest/operations/cli#cmdoption-mode) option.
The binary of envoy isn't provided, so this action executes envoy with Docker image via `docker run` command.
If the configuration file is invalid, this action posts a comment to Pull Request or commit with [github-comment](https://github.com/suzuki-shunsuke/github-comment).

## Example

## Requirements

* [github-comment](https://github.com/suzuki-shunsuke/github-comment)

## Inputs, Outputs

Please see [action.yaml](action.yaml)

## License

[MIT](LICENSE)
