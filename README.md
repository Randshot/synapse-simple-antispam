# synapse-simple-antispam
A simple spam checker module for Synapse to block invites from unwanted homeservers


## Installation

In your Synapse python environment:
```bash
pip install git+https://github.com/Randshot/synapse-simple-antispam#egg=synapse-simple-antispam
```

Then add to your `homeserver.yaml`:
```yaml
# simple antispam
spam_checker:
  module: "synapse_simple_antispam.AntiSpamInvites"
  config:
    # A list of homeservers to block invites from.
    blocked_homeservers:
      - 200acres.org
      - glowers.club
    blocked_rooms:
      - "!HDmUYXHdcrmSKoMwNy:matrix.thisisjoes.site"
```

Synapse will need to be restarted to apply the changes. To modify the list of homeservers,
update the config and restart Synapse.
