GitLab Runner bundled with terraform binary.
Registers itself on start-up and de-registers on shut down by extending vendor's entrypoint.

```bash
docker run -d \
    -e 'CI_SERVER_URL="https://gitlab.domain.local"' \
    -e 'REGISTRATION_TOKEN="token"' \
    -e 'RUNNER_TAG_LIST="tag1,tag2"' \
    -v "$(pwd)/config.toml:/etc/gitlab-runner/config.toml" \
    intermedia/gitlab-runner     
```