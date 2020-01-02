# PSONO GCP Cloud Run

[![Run on Google Cloud](https://deploy.cloud.run/button.svg)](https://deploy.cloud.run?git_repo=https://github.com/psono/psono-gcp-cloud-run.git)

# Canonical source

The canonical source of PSONO GCP Cloud Run is [hosted on GitLab.com](https://gitlab.com/psono/psono-gcp-cloud-run).

# Documentation

The documentation for the psono server can be found here:

[Psono Documentation](https://doc.psono.com/)

Some things that have not yet found their place in the documentation:

# How to use?

1) Create startup parameters

You need a couple of parameters that you can generate with the following docker command:

    docker run --rm -ti psono/psono-server:latest python3 ./psono/manage.py generateserverkeys

2) Create a [Google Cloud Project](https://console.cloud.google.com/projectselector2/home/dashboard?hl=de)

3) [Enable Cloud Run API](http://console.cloud.google.com/apis/library/run.googleapis.com?hl=de)

3) [Enable Cloud SQL Admin API](https://console.cloud.google.com/flows/enableapi?apiid=sqladmin&redirect=https://console.cloud.google.com)

4) Create a [Cloud Postgres DB](https://console.cloud.google.com/sql/instances)

Remember the name of the instance

5) Click [Run on Google Cloud](https://deploy.cloud.run?git_repo=https://github.com/psono/psono-gcp-cloud-run.git)

If you receive a timeout you can start the provisioning

    cloudshell_open --repo_url "https://github.com/psono/psono-gcp-cloud-run.git" --page "editor"

6) Answer questions all the questions

7) Add [Domain Mapping](https://console.cloud.google.com/run/domains)

Use your provider to configure the necessary CNAME record

8) Configure email

Pick one of the supported email providers in the [Documentation](https://doc.psono.com/mydoc_configuration_email_amazon_ses.html) and configure the environment variables accordingly.

# LICENSE

Visit the [License.md](/LICENSE.md) for more details
