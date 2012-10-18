require 'rubygems'
gem 'hoe', '>= 2.1.0'
require 'hoe'
require 'fileutils'
require './lib/wifi_location'

Hoe.plugin :newgem
# Hoe.plugin :website
# Hoe.plugin :cucumberfeatures

# Generate all the Rake tasks
# Run 'rake -T' to see list of generated tasks (from gem root directory)
$hoe = Hoe.spec 'wifi_location' do
  self.developer 'Sho Hashimoto', 'hashimoto@shokai.org'
  self.post_install_message = "!! You can get your location with \"whereami\" command. => http://shokai.github.com/wifi_location"
  self.rubyforge_name       = self.name # TODO this is default value
  self.extra_deps         = [['json','>= 1.5.3'],
                             ['args_parser', '>= 0.1.0', '< 1.0.0'],
                             ['launch-agent', '>= 0.7.0', '< 1.0.0']]

end

require 'newgem/tasks'
Dir['tasks/**/*.rake'].each { |t| load t }

# TODO - want other tests/tasks run by default? Add them to the list
# remove_task :default
# task :default => [:spec, :features]
