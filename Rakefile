desc "Return list of GitHub repositories for a user"

task :repos do
  require 'json'
  require 'open-uri'

  #
  # enter github username within quotes below
  gh_name = 'gaphead'
  #
  #

  url = "https://api.github.com/users/#{gh_name}/repos"
  repos_serialized = open(url).read
  repos = JSON.parse(repos_serialized)

  # returns
  repos.each { |repo| puts repo['full_name'].gsub("#{gh_name}/", '') }
end
