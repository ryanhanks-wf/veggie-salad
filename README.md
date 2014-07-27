# veggie-wrap

This project uses [soloist](https://github.com/mkocher/soloist) and [librarian-chef](https://github.com/applicationsonline/librarian-chef)
to run a subset of the recipes in sprout's cookbooks.

[Fork it](https://github.com/ryanhanks/veggie-salad/fork) to 
customize its [attributes](http://docs.opscode.com/chef_overview_attributes.html) in [soloistrc](/soloistrc) and the list of recipes 
you'd like to use. You may also want to add other cookbooks to its [Cheffile](/Cheffile), perhaps one 
of the many [community cookbooks](http://community.opscode.com/cookbooks). By default it configures an OS X 
Mavericks workstation for development.

## Creating a machine base image

1. Finalize OS X install
2. Install software updates
3. xcode-select --install
4. Install VMWare Tools
5. Install Xcode
6. Create and upload github tokens

## Installation under Mavericks (OS X 10.9)

1. Run provisioning script
```bash
mkdir ~/Workspaces
cd ~/Workspaces
git clone git@github.com:ryanhanks/veggie-salad
cd veggie-salad
sudo gem install bundler
sudo ARCHFLAGS=-Wno-error=unused-command-line-argument-hard-error-in-future bundle
sudo pmset sleep 90
time bundle exec soloist
cd ~/.bash_it
git remote set-url origin git@github.com:ryanhanks/bash-it
```

2. Enable Witch
3. Restart
4. Log in to drop box
5. Wait for sync
6. Open 1password
7. Log in to chrome
4. Take snapshot

See Pivotal Tracker: https://www.pivotaltracker.com/s/projects/884116

## Discussion List

  Join [sprout-users@googlegroups.com](https://groups.google.com/forum/#!forum/sprout-users) if you use Sprout.

## References

* Slides from @hiremaga's [lightning talk on Sprout](http://sprout-talk.cfapps.io/) at Pivotal Labs in June 2013
* [Railscast on chef-solo](http://railscasts.com/episodes/339-chef-solo-basics) by Ryan Bates (PAID)
