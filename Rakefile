require 'rake'
require 'aws-sdk'

desc "build AMI for rails"
task :build do
  opts = {}
  opts[:ami_id] = "ami-0af1df87db7b650f4" # amzn2-ami-hvm-2.0.20200207.1-x86_64-gp2
  opts[:ami_name] = "rails-base"
  args = opts.map { |k, v| "-var '#{k}=#{v}'" }.join(" ")

  sh "packer build #{args} packer/ami.json"
end

