# linux-stuff

#Add a custom systemd service
```
sudo nano /etc/systemd/system/custom-service.service
systemctl --user enable custom-service
systemctl --user start custom-service
```

Example systemd service to run a script on boot:
```
[Unit]
Description=Startup Script

[Service]
ExecStart=sudo ./home/bsamsom/startup.sh

[Install]
WantedBy=multi-user.target
```
