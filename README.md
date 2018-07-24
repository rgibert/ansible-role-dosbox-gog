# Dosbox

Installs GOG's DOSbox games

## Requirements

- none

## Role Variables

| Variable | Default | Description |
|----------|---------|-------------|
| dosbox_gog_app_bin | | Binary to use to start the game |
| dosbox_gog_app_name_long | | Long form of application name (eg: Quest for Glory) |
| dosbox_gog_app_name_short | | Short form of application name (eg: qfg1) |
| dosbox_gog_desktop_location | ~/.local/share/applications | Path to store desktop file in |
| dosbox_gog_desktop_img | | Image to use for desktop file |
| dosbox_gog_installer_path | | Local path to installer |

## Dependencies

- rgibert.dosbox

## Example Playbook

```
- hosts:
    - servers
  roles:
    - role: rgibert.dosbox-gog
      dosbox_gog_app_name_long: Quest for Glory
      dosbox_gog_app_name_short: qfg1
      dosbox_gog_installer_verification: "{{ dosbox_root }}/app/SCIV.EXE"
      dosbox_gog_installer_path: /tmp/qfg.exe

```

## License

GPLv3

## Author Information

Richard Gibert <richard@gibert.ca>
