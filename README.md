# Ansible Role: Gitlab-Config

Add or edit gitlab variables

## Requirements

None.

## Role Variables

### Gitlab keys
```yaml
gitlab_api_url: "https://gitlab.com/api/v4"
gitlab_token: "YOUR_GITLAB_TOKEN"
```

### Variables each project
```yaml
gitlab_variables:
  - project_name: "your-project-name"
    # Project id on the gitlab
    project_id: 1111111
    envs:
      - key: KEY_1_STAGE
        value: "value1"
      - key: KEY_1_MASTER
        value: "value2"
```

## Dependencies

None.

## Example Playbook (using default package)

    - hosts: servers
      roles:
        - role: MahdadGhasemian.ansible-gitlab-config

## License

MIT / BSD

## Author Information

This role was created in 2023 by [Mahdad Ghasemian](https://mahdad.me/).