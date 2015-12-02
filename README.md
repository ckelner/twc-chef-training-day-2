twc-chef-training-day-2
===============

Work done from local workstation instead of remote EC2 instance.

# Common commands
## From Day 1
Using chef-zero
### Chef
- `chef generate template <filename>`
- `chef generate cookbook <new cookbook name>`
### Chef-client
- `chef-client --local-mode -r "recipe[apache]"`
### Chef-apply
- `chef-apply recipes/<recipe-filename>``
## From Day 2
Using hosted chef
### Knife
- `knife client list`
- `knife cookbook list`
- `knife bootstrap <ipaddr-hostname> -x user -P pass --sudo -N node1`
  - Adds an existing machine as a node.  Seems janky and something I'd never do.
- `knife node list`
  - Shows all nodes chef server knows about
- `knife node show <nodename>`
  - returns all data about a node
- `knife node run_list add <nodename> "recipe[<receipename>]"`
- `knife node show <nodename> -a <attribute>`
  - Gets specific bits of data about node
- `knife ssh "name:<nodename>" -x <user> -P <pass> "sudo chef-client"`
  - Seems janky.
### Kitchen
- `kitchen test`
### Berks
- `berks install`
- `berks upload`
