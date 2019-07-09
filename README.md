# GitHub Enterprise API Notes
Personal notes on basic usage of the GitHub Enterprise API

<p>

# GitHub API Documentation
[REST API v3](https://developer.github.com/v3/)

<p>

# Using Chrome browser
All API endpoints -- except Management Console API endpoints -- are prefixed with the following URL:

<pre>
https://hostname/api/v3
</pre>

GitHub Enterprise API endpoints accept the same authentication methods as the GitHub API.<br>
Specifically, you can authenticate yourself with:<br>

1) Auth tokens (which can be created using the Authorization API) or<br>
2) Basic authentication<br>

Every Enterprise API endpoint is only accessible to GitHub Enterprise site administrators, with the exception of the Management Console API, which is only accessible via the Management Console password.

<p>

# Using curl
<pre>
Example using the organizations API:

curl -H "Authorization: [token|bearer] [OAuth_Token|ACCESS_TOKEN]" https://hotname/api/v3/organizations
</pre>

<p>
  
# Getting list of supported API endpoints
To get a list of all API endpoints, simply pass the https://[hostname]/api/v3 API call.

Example:
<details>
<summary>
  
<pre>  
$ curl -H "Authorization: token 553daa92ecbd764b5ef1ec05455f5fc02968b6c9" https://github.awsinternal.tri.global/api/v3
{
  "current_user_url": "https://github.awsinternal.tri.global/api/v3/user",
  "current_user_authorizations_html_url": "https://github.awsinternal.tri.global/settings/connections/applications{/client_id}",
  "authorizations_url": "https://github.awsinternal.tri.global/api/v3/authorizations",
  "code_search_url": "https://github.awsinternal.tri.global/api/v3/search/code?q={query}{&page,per_page,sort,order}",
  "commit_search_url": "https://github.awsinternal.tri.global/api/v3/search/commits?q={query}{&page,per_page,sort,order}",
  "emails_url": "https://github.awsinternal.tri.global/api/v3/user/emails",
  "emojis_url": "https://github.awsinternal.tri.global/api/v3/emojis",
  "events_url": "https://github.awsinternal.tri.global/api/v3/events",
  "feeds_url": "https://github.awsinternal.tri.global/api/v3/feeds",
  "followers_url": "https://github.awsinternal.tri.global/api/v3/user/followers",
  "following_url": "https://github.awsinternal.tri.global/api/v3/user/following{/target}",
  "gists_url": "https://github.awsinternal.tri.global/api/v3/gists{/gist_id}",
  "hub_url": "https://github.awsinternal.tri.global/api/v3/hub",
  "issue_search_url": "https://github.awsinternal.tri.global/api/v3/search/issues?q={query}{&page,per_page,sort,order}",
  "issues_url": "https://github.awsinternal.tri.global/api/v3/issues",
  "keys_url": "https://github.awsinternal.tri.global/api/v3/user/keys",
  "notifications_url": "https://github.awsinternal.tri.global/api/v3/notifications",
  "organization_repositories_url": "https://github.awsinternal.tri.global/api/v3/orgs/{org}/repos{?type,page,per_page,sort}",
  "organization_url": "https://github.awsinternal.tri.global/api/v3/orgs/{org}",
  "public_gists_url": "https://github.awsinternal.tri.global/api/v3/gists/public",
  "rate_limit_url": "https://github.awsinternal.tri.global/api/v3/rate_limit",
  "repository_url": "https://github.awsinternal.tri.global/api/v3/repos/{owner}/{repo}",
  "repository_search_url": "https://github.awsinternal.tri.global/api/v3/search/repositories?q={query}{&page,per_page,sort,order}",
  "current_user_repositories_url": "https://github.awsinternal.tri.global/api/v3/user/repos{?type,page,per_page,sort}",
  "starred_url": "https://github.awsinternal.tri.global/api/v3/user/starred{/owner}{/repo}",
  "starred_gists_url": "https://github.awsinternal.tri.global/api/v3/gists/starred",
  "team_url": "https://github.awsinternal.tri.global/api/v3/teams",
  "user_url": "https://github.awsinternal.tri.global/api/v3/users/{user}",
  "user_organizations_url": "https://github.awsinternal.tri.global/api/v3/user/orgs",
  "user_repositories_url": "https://github.awsinternal.tri.global/api/v3/users/{user}/repos{?type,page,per_page,sort}",
  "user_search_url": "https://github.awsinternal.tri.global/api/v3/search/users?q={query}{&page,per_page,sort,order}"
}
</pre>
</summary>
</details>


# Resources
[REST API v3 Documentation](https://developer.github.com/v3/)
<br>
[Stackoverflow: What's my GitHub appliance's REST API endpoint?](https://stackoverflow.com/questions/36503800/whats-my-github-appliances-rest-api-endpoint)
