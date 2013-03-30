guard 'rspec', :version => 2 do
watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb$})     { |m| "spec/#{m[1]}_spec.rb" }
  watch('spec/spec_helper.rb')  { "spec/" }
end

notification :tmux,
  :display_message => true,
  :timeout => 5, # in seconds
  :default_message_format => '%s >> %s',
# the first %s will show the title, the second the message
# Alternately you can also configure *success_message_format*,
# *pending_message_format*, *failed_message_format*
  :line_separator => ' > ', # since we are single line we need a separator
  :color_location => 'status-left-bg', # to customize which tmux element will change color
  :display_message => true

