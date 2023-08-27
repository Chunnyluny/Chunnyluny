RSS feed
{{range rss "https://domain.tld/feed.xml" 5}}
Title: {{.Title}}
URL: {{.URL}}
Published: {{humanize .PublishedAt}}
{{end}}
Your recent contributions
{{range recentContributions 10}}
Name: {{.Repo.Name}}
Description: {{.Repo.Description}}
URL: {{.Repo.URL}})
Occurred: {{humanize .OccurredAt}}
{{end}}
This function requires GitHub authentication with the following API scopes: repo:status, public_repo, read:user.

Your recent pull requests
{{range recentPullRequests 10}}
Title: {{.Title}}
URL: {{.URL}}
State: {{.State}}
CreatedAt: {{humanize .CreatedAt}}
Repository name: {{.Repo.Name}}
Repository description: {{.Repo.Description}}
Repository URL: {{.Repo.URL}}
{{end}}
This function requires GitHub authentication with the following API scopes: repo:status, public_repo, read:user.

Repositories you recently starred
{{range recentStars 10}}
Name: {{.Repo.Name}}
Description: {{.Repo.Description}}
URL: {{.Repo.URL}})
Stars: {{.Repo.Stargazers}}
{{end}}
This function requires GitHub authentication with the following API scopes: repo:status, public_repo, read:user.

Repositories you recently created
{{range recentRepos 10}}
Name: {{.Name}}
Description: {{.Description}}
URL: {{.URL}})
Stars: {{.Stargazers}}
{{end}}
This function requires GitHub authentication with the following API scopes: repo:status, public_repo, read:user.

Custom GitHub repository
{{with repo "muesli" "markscribe"}}
Name: {{.Name}}
Description: {{.Description}}
URL: {{.URL}}
Stars: {{.Stargazers}}
Is Private: {{.IsPrivate}}
Last Git Tag: {{.LastRelease.TagName}}
Last Release: {{humanize .LastRelease.PublishedAt}}
{{end}}
This function requires GitHub authentication with the following API scopes: repo:status, public_repo, read:user.

Forks you recently created
{{range recentForks 10}}
Name: {{.Name}}
Description: {{.Description}}
URL: {{.URL}})
Stars: {{.Stargazers}}
{{end}}
This function requires GitHub authentication with the following API scopes: repo:status, public_repo, read:user.

Recent releases you contributed to
{{range recentReleases 10}}
Name: {{.Name}}
Git Tag: {{.LastRelease.TagName}}
URL: {{.LastRelease.URL}}
Published: {{humanize .LastRelease.PublishedAt}}
{{end}}
This function requires GitHub authentication with the following API scopes: repo:status, public_repo, read:user.

Your published gists
{{range gists 10}}
Name: {{.Name}}
Description: {{.Description}}
URL: {{.URL}}
Created: {{humanize .CreatedAt}}
{{end}}
This function requires GitHub authentication with the following API scopes: repo:status, public_repo, read:user.

Your latest followers
{{range followers 5}}
Username: {{.Login}}
Name: {{.Name}}
Avatar: {{.AvatarURL}}
URL: {{.URL}}
{{end}}
This function requires GitHub authentication with the following API scopes: read:user.
