# ansiblevCloudBuild
The goal of this playbook is to build out an environment in vcloud without using 3rd party modules Using ansible 2.5

The URI and XML module are mainly used against the vCloud REST API. Initially friendly names are used for variables, production I would likely use hrefs or object guids to avoid naming conflicts when dealing with multiple vcd environments. The InstantiatevAppTemplate operation in vCloud is not fun and the documentation seems to contradict the results. '/roles/common/xml' holds the template for the vm build, may build this on the fly though I hate dealing with xml(aparently json inputs are coming to vCloud so my TAM says). '/roles/common/vars' contains all the variables used

vcdlogon - Performs the authentication and outputs the auth token cookie and org href vcdgetvApp - Get the href of the vApp template within a specific catalogue(umming and ahhing about how I should spell catalogue in variables was a constant battle)

04/07/2018
Added looping to build multiple vapps that are listed in the vars file

TODO : Full environment build and software installation/configuration.
