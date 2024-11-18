

# Join the Union Ceremony

## Install Desktop Environment
Update the package list and install the XFCE desktop environment:

```bash
sudo apt-get update
sudo apt install xfce4 xfce4-goodies -y
```

## Install xrdp
Install xrdp:

```bash
sudo apt install xrdp -y
```

Enable and start xrdp for automatic startup:

```bash
sudo systemctl enable xrdp
sudo systemctl start xrdp
```

## Configure xrdp with Xfce
Set up xrdp to use the Xfce session:

```bash
echo "xfce4-session" >~/.xsession
```

## Configure the Firewall
Open port 3389 for RDP connections:

```bash
sudo ufw allow 3389/tcp
```

## Use Firefox Browser in RDP Connection
Install Firefox:

```bash
sudo apt install firefox -y
```

### Download RDP Client
For example, you can use Microsoft Remote Desktop:

1. Click **Add**.
2. Select **PCs**.
3. Enter the IP address of your server as the **PC name**.
4. Create a new user account by clicking the **+** icon.  
   - **Username**: `root`  
   - **Password**: Enter your server's password.
5. Save the settings and connect.

### Locate Firefox
When connected via RDP, locate Firefox as follows:

1. Click the "Applications" menu.
2. Select the "Internet" or "Web Browsers" category to find the Firefox icon.
3. Click the Firefox icon to open the browser.
4. If it does not appear in the menu, open the terminal and run the following command:

```bash
firefox
```

## Join the Ceremony
1. Go to [https://ceremony.union.build/](https://ceremony.union.build/).
2. Log in with your GitHub or Google account.
3. Select **Linux** and copy the code provided.

## Connect to VPS and Prepare the Session
1. Connect to your VPS via RDP as usual without disconnecting the session.
2. Open a screen session:

```bash
apt install screen
screen -S unicr
```

3. Paste the copied code. If Docker is not installed, an error will be displayed along with installation instructions. Follow those instructions to install Docker and then re-enter the code.
```bash
apt install docker.io
```
4. Once it says "Switch to browser", detach the screen session:

```bash
Ctrl+A+D
```

## Continue in Firefox on RDP
1. Continue the process in Firefox.
2. When a file is downloaded, save it in:

```plaintext
/root/Downloads
```

3. Follow the process to provide the Cosmos address from Keplr.
4. Join the ceremony.

## Disconnect and Reconnect
1. Do not close Firefox. Disconnect the RDP session from the top-right corner using the **X** button.
2. Reconnect later; Firefox will remain open.

Good luck!

**cc:** Zeska
