# GCP

## Compute Engine - Create a VM 
```
gcloud compute instances create-with-container test-vm-20211006 --project=shining-rush-328212 \
--zone=us-central1-c --machine-type=e2-micro --network-interface=network-tier=PREMIUM,subnet=default \
--maintenance-policy=MIGRATE --service-account=156817271061-compute@developer.gserviceaccount.com \
--scopes=https://www.googleapis.com/auth/devstorage.read_only,https://www.googleapis.com/auth/logging.write,https://www.googleapis.com/auth/monitoring.write,https://www.googleapis.com/auth/servicecontrol,https://www.googleapis.com/auth/service.management.readonly,https://www.googleapis.com/auth/trace.append \
--tags=http-server,https-server --container-image=us.gcr.io/shining-rush-328212/app-engine-tmp \
--container-restart-policy=always --create-disk=auto-delete=yes,boot=yes,device-name=test-vm-20211006,image=projects/cos-cloud/global/images/cos-stable-89-16108-534-9,mode=rw,size=10 --no-shielded-secure-boot --shielded-vtpm --shielded-integrity-monitoring \
--labels=environment=dev,container-vm=cos-stable-89-16108-534-9
```
