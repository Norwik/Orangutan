<p align="center">
    <img alt="Orangutan Logo" src="/static/logo.png?v=0.1.0" height="200" />
    <h3 align="center">Orangutan</h3>
    <p align="center">Pinkman and Moose Deployment Playbook.</p>
    <p align="center">
        <a href="https://github.com/Norwik/Orangutan/actions/workflows/build.yml">
            <img src="https://github.com/Norwik/Orangutan/actions/workflows/build.yml/badge.svg"/>
        </a>
    </p>
</p>


## Usage

1. Create a python virtual environment.

```zsh
$ python3 -m venv venv
$ source venv/bin/activate
```

2. Install `ansible`

```zsh
$ make config
```

3. Create `hosts.prod` from `hosts` file and replace `127.0.0.1` with the host IP.

4. Create `prod.vault.yml` with these configs.

```zsh
$ ansible-vault create prod.vault.yml
```

```yaml
system_user: orangutan
system_group: orangutan

pinkman_hostname: 0.0.0.0
pinkman_port: 1025
pinkman_backend_url: https://pinkman.free.beeceptor.com
pinkman_backend_api_key: 5ab99869-f403-4481-bed6-da7c8aad7521
```

5. Run ansible playbook

```zsh
$ make run
```

## Versioning

For transparency into our release cycle and in striving to maintain backward compatibility, Orangutan is maintained under the [Semantic Versioning guidelines](https://semver.org/) and release process is predictable and business-friendly.

See the [Releases section of our GitHub project](https://github.com/norwik/orangutan/releases) for changelogs for each release version of Orangutan. It contains summaries of the most noteworthy changes made in each release. Also see the [Milestones section](https://github.com/norwik/orangutan/milestones) for the future roadmap.


## Bug tracker

If you have any suggestions, bug reports, or annoyances please report them to our issue tracker at https://github.com/norwik/orangutan/issues


## Security Issues

If you discover a security vulnerability within Orangutan, please send an email to [hello@clivern.com](mailto:hello@clivern.com)


## Contributing

We are an open source, community-driven project so please feel free to join us. see the [contributing guidelines](CONTRIBUTING.md) for more details.


## License

© 2023, Orangutan. Released under [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0).

**Orangutan** is authored and maintained by [@Norwik](https://github.com/norwik).
