

Navigate to your DNS provider and create a CNAME record for the www subdomain that points to your GitHub Pages default domain. For example, if your site is located at <user>.github.io, you should create a CNAME record that points www.example.com to <user>.github.io Similarly, for an organization site located at <organization>.github.io, you should create a CNAME record that points www.example.com to <organization>.github.io. Ensure that the CNAME record points directly to <user>.github.io or <organization>.github.io without including the repository name.


To create A records, point your apex domain to the IP addresses for GitHub Pages.

185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
To create AAAA records, point your apex domain to the IP addresses for GitHub Pages.

2606:50c0:8000::153
2606:50c0:8001::153
2606:50c0:8002::153
2606:50c0:8003::153


EXAMPLE.COM with your apex domain. Confirm that the results match the IP addresses for GitHub Pages above.

For A records:

$ dig EXAMPLE.COM +noall +answer -t A
> EXAMPLE.COM    3600    IN A     185.199.108.153
> EXAMPLE.COM    3600    IN A     185.199.109.153
> EXAMPLE.COM    3600    IN A     185.199.110.153
> EXAMPLE.COM    3600    IN A     185.199.111.153
For AAAA records:

$ dig EXAMPLE.COM +noall +answer -t AAAA
> EXAMPLE.COM     3600    IN AAAA     2606:50c0:8000::153
> EXAMPLE.COM     3600    IN AAAA     2606:50c0:8001::153
> EXAMPLE.COM     3600    IN AAAA     2606:50c0:8002::153
> EXAMPLE.COM     3600    IN AAAA     2606:50c0:8003::153


[1] https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
