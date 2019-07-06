# Home-Assistant Custom Component for Go Slide

This custom component home-assistant (http://www.home-assistant.io) can control the Go Slide (https://nl.goslide.io). At this moment the component only support the Cloud option, because the local API hasn't been released yet (it planned to be included when released).

## Go Slide

### Installation

- Copy directory `goslide` `<config dir>/custom_components` directory.
- Configure with config below.
- Restart Home-Assistant.

### Usage
To use this component in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry

goslide:
  username: goslide@somedomain.com
  password: secret
  scan_interval: 30
```

Configuration variables:

- **username** (*Required*): The e-mail used to register your account with api.goslide.io, with your iPhone/Android App
- **password** (*Required*): The password of your account with api.goslide.io
- **scan_interval** (*Optional*): Number of seconds between polls. (default = 30)

### Debugging

It is possible to debug the GoSlide component and API library, this can be done by adding the following lines to the `configuration.yaml` file:

```yaml
logger:
  logs:
    goslideapi: debug
    homeassistant.components.goslide: debug
```

### TO DO

- Improve error handling
- Improve debugging
- Add local API support, when released

