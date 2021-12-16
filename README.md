# github-action-validate-envoy-proxy

GitHub Actions to validate [Envoy Proxy](https://www.envoyproxy.io/) Configuration.

## How does it works?

This action executes `envoy` with [--mode validate](https://www.envoyproxy.io/docs/envoy/latest/operations/cli#cmdoption-mode) option.
The binary of envoy isn't provided, so this action executes envoy with Docker image via `docker run` command.
If the configuration file is invalid, this action posts a comment to Pull Request or commit with [github-comment](https://github.com/suzuki-shunsuke/github-comment).

## Example

* [.github/workflows/test-actions.yml](.github/workflows/test-actions.yml)
* [.github-comment.yml](.github-comment.yml)
* [aqua.yaml](aqua.yaml)

![image](https://user-images.githubusercontent.com/13323303/146328887-a92e122f-d9ed-4485-a364-0720bf8d4fff.png)

https://github.com/suzuki-shunsuke/github-action-validate-envoy-proxy/pull/1#issuecomment-995517990

## Requirements

* [github-comment](https://github.com/suzuki-shunsuke/github-comment)

## Inputs, Outputs

Please see [action.yaml](action.yaml)

## Docker Authentication

This action pulls the Docker Image for Envoy Proxy.
In this action the authentication isn't executed, so please do it in advance if needed.

## Customization

If you want to customize the Pull Request Comment or hide old comments,
please see the document of github-comment.

https://github.com/suzuki-shunsuke/github-comment

## License

[MIT](LICENSE)
