# claude-dispatch releases

Prebuilt macOS binaries of `cdispatch`, the listener for claude-dispatch. Source is private; this repo only hosts releases.

| File | Macs |
|---|---|
| `cdispatch-arm64` | Apple Silicon (M1, M2, M3, M4) |
| `cdispatch-x86_64` | Intel |

## Install or update

```sh
mkdir -p ~/.local/bin
gh release download -R dpunosevac/claude-dispatch-releases -p "cdispatch-$(uname -m)" -O ~/.local/bin/cdispatch --clobber
chmod +x ~/.local/bin/cdispatch
cdispatch --version
```

`$(uname -m)` picks the right file. If the agent is already set up, run `cdispatch install` to restart it on the new version.

Downloaded with a browser instead of `gh`? Clear the quarantine flag first: `xattr -d com.apple.quarantine ~/.local/bin/cdispatch`.

Each release lists the SHA-256 of both files.
