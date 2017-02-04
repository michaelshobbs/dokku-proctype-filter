# dokku-proctype-filter

dokku-proctype-filter is a plugin for [dokku][dokku] that only runs Procfile processes as defined by a config variable

## Requirements

This plugin uses the `pre-deploy` trigger to modify the `DOKKU_SCALE` file to only run Procfile processes defined by the `DOKKU_PROCFILE_FILTER` environment variable.

## Installation & Example

```sh
# Install the plugin:
# dokku 0.4+
dokku plugin:install https://github.com/michaelshobbs/dokku-proctype-filter.git

dokku config:set <app> DOKKU_PROCFILE_FILTER="web worker"
dokku ps:restart <app>
```

## License

This plugin is released under the MIT license. See the file [LICENSE](LICENSE).

[dokku]: https://github.com/progrium/dokku
