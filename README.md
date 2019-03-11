# qgm-make-docker-host

You need a naked ubuntu 18.04 server host.

* Install git & ansible: ``apt-get install git ansible``
* Clone this repo
* ``cd qgm-make-docker-host``
* ``ansible-playbook  dockerhost.yml`` takes care of the rest.

Attention: 

* This is work in progress, use with care
* The playbook **disables ssh password authentication** to you host, so be shure that you have direct console access or acces with a public key auth to the server 
