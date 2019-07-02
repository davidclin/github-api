# GitHub Enterprise API Notes
Personal notes on basic usage of the GitHub Enterprise API

# Using Chrome browser
All API endpoints -- except Management Console API endpoints -- are prefixed with the following URL:

<pre>
https://hostname/api/v3
</pre>

GitHub Enterprise API endpoints accept the same authentication methods as the GitHub API.<br>
Specifically, you can authenticate yourself with:<br>

1) Auth tokens (which can be created using the Authorization API or<br>
2) Basic authentication<br>

Every Enterprise API endpoint is only accessible to GitHub Enterprise site administrators, with the exception of the Management Console API, which is only accessible via the Management Console password.


# Using curl
<pre>
curl -H "Authorization: bearer [ACCESS_TOKEN]" https://hotname/api/v3/organizations
</pre>

# Resources
[REST API v3 Documentation](https://developer.github.com/v3/)
<br>
[Stackoverflow: What's my GitHub appliance's REST API endpoint?](https://stackoverflow.com/questions/36503800/whats-my-github-appliances-rest-api-endpoint)
