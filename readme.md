![Monkee-Boy](https://dujrsrsgsd3nh.cloudfront.net/img/emoticons/113009/mboy-1403710932.jpg) mBoy Vagrant
==============

This is the default Monkee-Boy Vagrantfile. It was generated using [PuPHPet](https://puphpet.com). Ubuntu, Apache, PHP, MySQL, and Ruby versions match those found on Habitat.

## Usage

* `git clone git@github.com:Monkee-Boy/vagrant.git && cd vagrant`
* Modify line 108 in `Vagrantfile` to your root Sites directory. This will be the synced directory and the path to adding your vhosts. Typically this won't need to be changed if this is cloned inside your Sites directory.
* `vagrant up`
* Use `vagrant ssh` if you need to make any changes or to have further control.

### Add Domain

* `cd` to this git repo.
* `vagrant ssh -c 'sudo vhost -s client-domain.dev -a www.client-domain.dev -d /var/www/clientname/site'`
  * `-s` is the server name, `-a` is the server alias, `-d` is the document root.
* Edit your hosts file with `192.168.22.10 client-domain.dev`.
* http://client-domain.dev should now work.

#### Quick Add

* Edit `./vagrantvhost.sh` with your vagrant id. Get this by running `vagrant global-status`.
* Setup `alias vagrantvhost="sh ~/Sites/vagrant/vagrantvhost.sh"` as an alias. Modify the path to this vagrant repo.
* Add new domain with `vagrantvhost client-domain.dev /var/www/clientname/site`. This will automatically include a server alias of www.

### MySQL Connection

We recommend using [SequelPro](http://www.sequelpro.com/) for easy database management.

* Host: `192.168.22.10`
* User: `root`
* Pass: `root`

## The Dev Team

Handcrafted with ♥ in Austin, Texas by the [Monkee-Boy Troop](https://www.monkee-boy.com/who/the-troop/).

[![James Fleeting](https://avatars0.githubusercontent.com/u/23062?s=144)](https://github.com/fleeting) | [![Pete Gautier](https://avatars2.githubusercontent.com/u/5394199?v=3&s=144)](https://github.com/pgautier404) | [![John Hoover](https://avatars3.githubusercontent.com/u/48278?v=3&s=144)](https://github.com/defvayne23) | [![David Saunders](https://avatars3.githubusercontent.com/u/4614981?v=3&s=144)](https://github.com/djsaun)
:---:|:---:|:---:|:---:|:---:
[James Fleeting](https://github.com/fleeting) | [Pete Gautier](https://github.com/pgautier404) | [John Hoover](https://github.com/defvayne23) | [David Saunders](https://github.com/djsaun)

![Monkee-Boy](http://assets.monkee-boy.com/mboy-logo-tagline.jpg)
