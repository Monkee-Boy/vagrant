![Monkee-Boy](https://dujrsrsgsd3nh.cloudfront.net/img/emoticons/113009/mboy-1403710932.jpg) mBoy Vagrant
==============

This is the default Monkee-Boy Vagrantfile. It uses the awesome [Vaprobash](https://github.com/fideloper/Vaprobash).

## Usage

* `git clone git@github.com:Monkee-Boy/vagrant.git && cd vagrant`
* Modify line 108 in `Vagrantfile` to your root Sites directory. This will be the synced directory and the path to adding your vhosts.
* `vagrant up`
* Use `vagrant ssh` if you need to make any changes or to have further control.

### Add Domain

* `cd` to this git repo.
* `vagrant ssh -c 'sudo vhost -s client-domain.dev -a www.client-domain.dev -d /vagrant/clientname/site'`
  * `-s` is the server name, `-a` is the server alias, `-d` is the document root.
* Edit your hosts file with `192.168.22.10 client-domain.dev`.
* http://client-domain.dev should now work.

#### Quick Add

* Edit `./vagrantvhost.sh` with your vagrant id. Get this by running `vagrant global-status`.
* Setup `alias vagrantvhost="sh ~/Sites/mBoy/mboy-vagrant/vagrantvhost.sh"` as an alias. Modify the path to this repo.
* Add new domain with `vagrantvhost client-domain.dev /vagrant/clientname/site`.

### MySQL Connection

We recommend using [SequelPro](http://www.sequelpro.com/) for easy database management.

* Host: `192.168.22.10`
* User: `root`
* Pass: `root`

## The Dev Team

Handcrafted with ♥ in Austin, Texas by the [Monkee-Boy Troop](http://www.monkee-boy.com/about/the-troop.php).

| [![James Fleeting](https://avatars0.githubusercontent.com/u/23062?s=100)](https://github.com/fleeting) | [![Pete Gautier](https://avatars3.githubusercontent.com/u/5394199?s=100)](https://github.com/pgautier404) | [![Sarah Higley](https://avatars3.githubusercontent.com/u/3819570?s=100)](https://github.com/smhigley) | [![John Hoover](https://avatars2.githubusercontent.com/u/48278?s=100)](https://github.com/defvayne23) | [![Jessica Canales](https://avatars3.githubusercontent.com/u/6892358?s=100)](https://github.com/jesscanales) |
|---|---|---|---|---|
| [James Fleeting](http://github.com/fleeting) | [Pete Gautier](https://github.com/pgautier404) | [Sarah Higley](https://github.com/smhigley) | [John Hoover](https://github.com/defvayne23) | [Jessica Canales](https://github.com/jesscanales) |

![Monkee-Boy](http://www.monkee-boy.com/img/logo-withtag-vertical-dark.jpg)
