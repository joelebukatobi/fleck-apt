# Fleck packages

The apt repository for [Fleck](https://github.com/joelebukatobi/fleck), sticky
notes for the COSMIC desktop. Only packages live here; the source is in the
other repository.

Add it once and Fleck updates with the rest of your system:

```bash
curl -fsSL https://joelebukatobi.github.io/fleck-apt/fleck.gpg | sudo tee /usr/share/keyrings/fleck.gpg > /dev/null
echo 'deb [signed-by=/usr/share/keyrings/fleck.gpg] https://joelebukatobi.github.io/fleck-apt stable main' | sudo tee /etc/apt/sources.list.d/fleck.list
sudo apt update && sudo apt install fleck
```

Releases are published here automatically when Fleck is tagged. See
[CHANGELOG.md](CHANGELOG.md) for what changed.

## Layout

```
fleck.gpg                  the key the indexes are signed with
dists/stable/              Release, InRelease, Release.gpg, Packages
pool/main/f/fleck/         the .deb files, every version kept
```
