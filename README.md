Task 7 - Netdata Monitoring

## Objective
Install Netdata and capture live system/app metrics.

## How I ran Netdata
(Choose the option you used — Docker or native)

### Docker (commands used)
docker run -d --name=netdata -p 19999:19999 --cap-add=SYS_PTRACE --security-opt apparmor=unconfined -v netdataconfig:/etc/netdata -v netdatalib:/var/lib/netdata -v netdatacache:/var/cache/netdata netdata/netdata

### docker-compose (if used)
See docker-compose.yml in repo.

### Native (if used)
sudo bash -c "$(curl -Ss https://my-netdata.io/kickstart.sh)"

## How to view dashboard
Open `http://<host-ip>:19999` in your browser.

## Deliverables
- Screenshots in `/screenshots`
- Commands used in `/run-command.txt` (optional)

## Notes / Troubleshooting

See the Troubleshooting section in this README (or the repository description).

Live Dashboard (Local)

Accessible locally at http://localhost:19999

<img width="1918" height="1036" alt="Screenshot 2025-10-30 121818" src="https://github.com/user-attachments/assets/48b3d750-fe7b-4c1d-99b4-7fdd9bc15ba2" />

---

### **STEP 8 – Push to GitHub**
1. Create a **new repository** in GitHub named `task7-netdata`.  
2. In your local folder, run:
   ```bash
   git init
   git add .
   git commit -m "Task 7 – Netdata Monitoring Setup"
   git branch -M main
   git remote add origin https://github.com/<your-username>/task7-netdata.git
   git push -u origin main

