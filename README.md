# scuomstv client patch distribution

This repository currently hosts **synthetic patcher tests only**. No production MapleStory2 patch or dye patch has been published.

- `channels/stable.json`: latest cumulative test release (v3).
- `patcher-test-v1`: initial test release and frozen v1 channel.
- `patcher-test-v3`: latest test rules and binary payloads.
- v2 is deliberately not published; v1 clients update directly to v3.
- Only the dedicated `test-client.id` baseline is accepted. Production game clients do not match it.

Use the local Maple2Patcher 1.1 build with the config in this repository. Download `test-client-baseline.zip` from the v1 release into a new test folder. Apply v1 with `tests/version-1-config.json`, then v3 with `patcher-config.json`. See [test procedure](tests/README.md).

The patcher binary and third-party game/file libraries are not hosted here. Releases contain only original synthetic text payloads and test metadata.
