# Example for using `rules_go` and `rules_oci` with bzlmod

## Usage

```shell-session
bazel build //app:app_tar
docker load --input $(bazel cquery --output=files //app:app_tar)
docker run -it --rm app:latest
```