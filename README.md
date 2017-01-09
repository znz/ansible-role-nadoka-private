# Ansible role for `nadoka` to private servers

- Setup `nadoka` with `runit`

## Requirements

- Debian
- Ubuntu

## Role Variables

### Common

- `user`: nadoka process user
- `group`: group of nadoka process user
- `nadoka_fprog_host`: host name of IRC server 1
- `nadoka_fprog_port`: port of IRC server 1
- `nadoka_fprog_pass`: password of IRC server 1
- `nadoka_fprog_key`: channel key of `#servers` of IRC server 1
- `nadoka_slack_host`: host name of IRC server 2
- `nadoka_slack_port`: port of IRC server 2
- `nadoka_slack_pass`: password of IRC server 2
- `nadoka_slack_user`: user name of IRC server 2

## Dependencies

None.

## Example Playbook

Normal usage with :

    ---
    - hosts: all
      become: yes
      roles:
      - znz.nadoka
      vars_files:
      - config.yml

## Example vars file

    ---
    user: "vagrant"
    group: "vagrant"

    nadoka_fprog_host: "irc.example.org"
    nadoka_fprog_port: 6667
    nadoka_fprog_pass: "ServerPass"
    nadoka_fprog_key: "ChannelKey"

    nadoka_slack_host: "example.irc.slack.com"
    nadoka_slack_port: 6667
    nadoka_slack_pass: "example.YourPassword"
    nadoka_slack_user: "YourUser"

## License

MIT License
