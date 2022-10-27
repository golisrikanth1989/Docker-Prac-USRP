# For running 5G OAI Core Network
 docker-compose -f docker-compose-basic-nrf.yaml up -d mysql oai-nrf oai-udr oai-udm oai-ausf oai-amf oai-smf oai-spgwu oai-ext-dn

 # For running 5G gNB Simulators
  docker-compose -f docker-compose-basic-nrf.yaml up -d oai-gnb1
  docker-compose -f docker-compose-basic-nrf.yaml up -d oai-gnb2

# For running 5G UEs Simulators
docker-compose -f docker-compose-basic-nrf.yaml up -d oai-nr-ue1
docker-compose -f docker-compose-basic-nrf.yaml up -d oai-nr-ue2
docker-compose -f docker-compose-basic-nrf.yaml up -d oai-nr-ue3
docker-compose -f docker-compose-basic-nrf.yaml up -d oai-nr-ue4
docker-compose -f docker-compose-basic-nrf.yaml up -d oai-nr-ue5


# For USRP B210 based 5G gNB in docker
docker-compose -f docker-compose-basic-nrf.yaml up -d gnb_mono_tdd

# For running 5G gNB without docker
sudo ./nr-softmodem -O ../../../targets/PROJECTS/GENERIC-NR-5GC/CONF/gnb_5fi_b210.conf --sa -E --continuous-tx




    
  