## 🔑

This repository is for storage all my _public_ SSH/GPG keys, in such way that
with only a `git clone` I get all of them, if necessary.

### SSH key naming convention

The name of the key should follow the convention:

    id_<algorithm>_<category>_<app_or_service>.pub

I've choosen `ed25519` to be the algorithm, as it has a short length and is
strong enough (also, Github itself recommends it).

To create a new pair of SSH public/private key:

```bash
ssh-keygen -t ed25519 -f ~/.ssh/id_ed25519_<category>_<app_or_service> -C "<meaningful_description>"
```

In the `<meaningful_description>` part, describe the purporse of the key.

> WARNING: only the public key **should** be available.
