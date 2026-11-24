DISCLAIMER: This is just a English Translation for the Applicaiton from a Korean Developer via Ai usage. All Credits goes to their respective owners


# Gakuen Idolmaster Launcher

A Windows launcher for running Gakuen Idolmaster (DMM edition) without DMM GAME PLAYER or a manually configured VPN.

Download `GakumasLauncher.exe` from [Releases](../../releases). The game must already be installed through DMM GAME PLAYER.

## Japan connection methods

| Method | Description |
|---|---|
| VPN Gate | Default. Connects through public VPN Gate servers operated by the University of Tsukuba only from within the launcher. No additional setup is required. |
| VPN File | Connects through a configuration file from your VPN provider. OpenVPN (`.ovpn`) and WireGuard (`.conf`) are supported. |
| Direct Connection | Uses the PC's internet connection without a VPN. If you are outside Japan, connect to Japan with a VPN app first. |

VPN Gate and VPN File do not change Windows network settings; only connections made by the launcher use the VPN.

### Using a VPN file

1. Download a manual configuration file for a **Japan server** (OpenVPN or WireGuard) from your VPN provider's account page.
2. In the launcher, select **VPN File** and then **Select File**.
3. If the OpenVPN file requires credentials, enter them under **Account**. These are often manual-configuration OpenVPN credentials, not the provider's normal account password.

The configuration file and credentials are encrypted so they can only be decrypted under this Windows user account on this PC.

## Build

```
cargo build --release --bin GakumasLauncher
```

## Notice

DMM does not officially support use outside Japan. The user is responsible for complying with applicable terms and laws.
