<p align="center">
  <img src="./docksal-logo.svg" width="20%" />
</p>

<h1 align="center">Ansible Role for <a href="https://docksal.io">Docksal</a></h1>

<p>
  <a href="./LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" />
  </a>
</p>

> This repo contains an Ansible role that installs and configures Docksal on a supported Linux distributions.

## Requirements

**⚠️ This role assumes [Docker](https://docker.com) already installed!** Role will throw an error in case if `docker-ce` package is not installed on target host.

## Example Ansible Playbooks

### Simple

```yaml
- hosts: 127.0.0.1
  roles:
    - role: ansible-role-docksal
```

### Complex

It's possible to override global settings for Docksal: just pass `docksal_global_config` variable with configuration object.

```yaml
- hosts: 127.0.0.1
  roles:
    - role: ansible-role-docksal
      vars:
        docksal_global_config:
          DOCKSAL_CONTAINER_HEALTHCHECK_INTERVAL: 10s
          DOCKSAL_DNS_UPSTREAM: 1.1.1.1
```

See [docksal documentation](https://docs.docksal.io/stack/configuration-variables/#global-variables) for all available global config variables.

## Author

👤 **Alexander Danilenko**

* Website: https://danilenko.in
* Github: [@alexander-danilenko](https://github.com/alexander-danilenko)
* LinkedIn: [@alexander-danilenko](https://linkedin.com/in/alexander-danilenko)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/alexander-danilenko/ansible-role-docksal/issues). 

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2022 [Alexander Danilenko](https://github.com/alexander-danilenko).<br />
This project is [MIT](./LICENSE) licensed.

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_