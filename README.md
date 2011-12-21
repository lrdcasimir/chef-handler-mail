# DESCRIPTION:

A simple chef report handler that uses the Pony gem to send email reports
generated from an Erubis template.

# USAGE:

Using chef_handler LWRP:

    include_recipe "chef_handler"
    
    gem_package "chef-handler-mail" do
      action :nothing
    end.run_action(:install)
    
    chef_handler 'mail-handler' do
      source 'chef/handler/mail'
      args :to_address "admins@example.com"
    end

# LICENSE AND AUTHOR:

Author:: Mathieu Sauve-Frankel (<msf@kisoku.net>)

Copyright:: 2011, Mathieu Sauve-Frankel

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
