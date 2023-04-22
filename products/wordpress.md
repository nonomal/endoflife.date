---
title: WordPress
category: server-app
iconSlug: wordpress
permalink: /wordpress
versionCommand: wp core version
releasePolicyLink: https://codex.wordpress.org/Supported_Versions
changelogTemplate: "https://wordpress.org/support/wordpress-version/version-{{'__LATEST__'|drop_zero_patch|replace:'.','-'}}/"
releaseColumn: true
releaseDateColumn: true
eolColumn: Support

# This regex drops '.0' from versions because x.y.0 releases are always referred as x.y.
# The patch part is like that to handle properly tiny versions, such as 1.5.1.3, are handled properly.
# But note that this regex would not work if WordPress releases a x.y.0.t version.
# That should not be a problem though, such version were only used with 1.5.1.
# See https://github.com/endoflife-date/endoflife.date/pull/2768#issuecomment-1491875624.
auto:
-   git: https://github.com/WordPress/wordpress-develop.git
    regex: '^(?<major>\d+)\.(?<minor>\d+)\.?(?<patch>[1-9][0-9.]*)?'

identifiers:
-   repology: wordpress
-   purl: pkg:docker/library/wordpress
-   purl: pkg:docker/bitnami/wordpress
-   purl: pkg:docker/bitnami/wordpress-nginx
-   purl: pkg:docker/bitnami/wordpress-intel
-   purl: pkg:docker/rapidfort/wordpress

# EOL(x) = releaseDate(X+1)
releases:
-   releaseCycle: "6.2"
    releaseDate: 2023-03-29
    eol: false
    latest: "6.2"
    latestReleaseDate: 2023-03-29
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3, 7.4, 8.0, 8.1, 8.2"

-   releaseCycle: "6.1"
    releaseDate: 2022-11-02
    eol: 2023-03-29
    latest: "6.1.1"
    latestReleaseDate: 2022-11-15
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3, 7.4, 8.0, 8.1, 8.2"

-   releaseCycle: "6.0"
    releaseDate: 2022-05-24
    eol: 2022-11-01
    latest: "6.0.3"
    latestReleaseDate: 2022-10-17
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3, 7.4, 8.0, 8.1"

-   releaseCycle: "5.9"
    releaseDate: 2022-01-25
    eol: 2022-05-24
    latestReleaseDate: 2022-10-17
    latest: "5.9.5"
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3, 7.4, 8.0, 8.1"

-   releaseCycle: "5.8"
    releaseDate: 2021-07-20
    eol: 2022-01-25
    latestReleaseDate: 2022-10-17
    latest: "5.8.6"
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3, 7.4, 8.0"

-   releaseCycle: "5.7"
    releaseDate: 2021-03-09
    eol: 2021-07-20
    latestReleaseDate: 2022-10-17
    latest: "5.7.8"
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3, 7.4, 8.0"

-   releaseCycle: "5.6"
    releaseDate: 2020-12-08
    eol: 2021-03-09
    latestReleaseDate: 2022-10-17
    latest: "5.6.10"
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3, 7.4, 8.0"

-   releaseCycle: "5.5"
    releaseDate: 2020-08-11
    eol: 2020-12-08
    latestReleaseDate: 2022-10-17
    latest: "5.5.11"
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3, 7.4"

-   releaseCycle: "5.4"
    releaseDate: 2020-03-31
    eol: 2020-08-11
    latestReleaseDate: 2022-10-17
    latest: "5.4.12"
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3, 7.4"

-   releaseCycle: "5.3"
    releaseDate: 2019-11-12
    eol: 2020-03-31
    latestReleaseDate: 2022-10-17
    latest: "5.3.14"
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3, 7.4"

-   releaseCycle: "5.2"
    releaseDate: 2019-05-07
    eol: 2019-11-12
    latestReleaseDate: 2022-10-17
    latest: "5.2.17"
    supportedPHPVersions: "5.6, 7.0, 7.1, 7.2, 7.3"

-   releaseCycle: "5.1"
    releaseDate: 2019-02-21
    eol: 2019-05-07
    latestReleaseDate: 2022-10-17
    latest: "5.1.15"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6, 7.0, 7.1, 7.2, 7.3"

-   releaseCycle: "5.0"
    releaseDate: 2018-12-06
    eol: 2019-02-21
    latestReleaseDate: 2022-10-17
    latest: "5.0.18"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6, 7.0, 7.1, 7.2, 7.3"

-   releaseCycle: "4.9"
    releaseDate: 2017-11-16
    eol: 2018-12-06
    latestReleaseDate: 2022-10-17
    latest: "4.9.22"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6, 7.0, 7.1, 7.2"

-   releaseCycle: "4.8"
    releaseDate: 2017-06-08
    eol: 2017-11-16
    latestReleaseDate: 2022-10-17
    latest: "4.8.21"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6, 7.0, 7.1"

-   releaseCycle: "4.7"
    releaseDate: 2016-12-06
    eol: 2017-06-08
    latestReleaseDate: 2022-10-17
    latest: "4.7.25"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6, 7.0, 7.1"

-   releaseCycle: "4.6"
    releaseDate: 2016-08-16
    eol: 2016-12-06
    latestReleaseDate: 2022-10-17
    latest: "4.6.25"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6, 7.0"

-   releaseCycle: "4.5"
    releaseDate: 2016-04-12
    eol: 2016-08-16
    latestReleaseDate: 2022-10-17
    latest: "4.5.28"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6, 7.0"

-   releaseCycle: "4.4"
    releaseDate: 2015-12-09
    eol: 2016-04-12
    latestReleaseDate: 2022-10-17
    latest: "4.4.29"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6, 7.0"

-   releaseCycle: "4.3"
    releaseDate: 2015-08-18
    eol: 2015-12-08
    latestReleaseDate: 2022-10-17
    latest: "4.3.30"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6"

-   releaseCycle: "4.2"
    releaseDate: 2015-04-23
    eol: 2015-08-18
    latestReleaseDate: 2022-10-17
    latest: "4.2.34"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6"

-   releaseCycle: "4.1"
    releaseDate: 2014-12-18
    eol: 2015-04-23
    latestReleaseDate: 2022-10-17
    latest: "4.1.37"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5, 5.6"

-   releaseCycle: "4.0"
    releaseDate: 2014-09-04
    eol: 2014-12-18
    latestReleaseDate: 2022-11-30
    latest: "4.0.38"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5"

-   releaseCycle: "3.9"
    releaseDate: 2014-04-16
    eol: 2014-09-04
    latestReleaseDate: 2022-11-30
    latest: "3.9.40"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5"

-   releaseCycle: "3.8"
    releaseDate: 2013-12-12
    eol: 2014-04-16
    latestReleaseDate: 2022-11-30
    latest: "3.8.41"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5"

-   releaseCycle: "3.7"
    releaseDate: 2013-10-24
    eol: 2013-12-12
    latestReleaseDate: 2022-11-30
    latest: "3.7.41"
    supportedPHPVersions: "5.2, 5.3, 5.4, 5.5"

-   releaseCycle: "3.6"
    releaseDate: 2013-08-01
    eol: 2013-10-24
    latestReleaseDate: 2013-09-11
    latest: "3.6.1"

---

> [WordPress](https://wordpress.org/) is a free and open-source content management system (CMS)
> written in PHP and paired with a MySQL or MariaDB database. Features include a plugin architecture
> and a template system, referred to within WordPress as "Themes".

The only officially supported and actively maintained version of WordPress is the last major release.

Security updates will be backported to older releases when possible, but there are no guarantee and
no timeframe for older releases. There are no fixed period of support nor Long Term Support (LTS)
version. None of these are safe to use, except the latest series, which is actively maintained.
Moreover, versions 3.7 to 4.0 [are guaranteed to not get security updates after
Dec 1, 2022](https://wordpress.org/news/2022/09/dropping-security-updates-for-wordpress-versions-3-7-through-4-0/).

## [PHP Support](https://make.wordpress.org/core/handbook/references/php-compatibility-and-wordpress-versions/)

:warning: Note that PHP 8 compatibility is
[considered as beta](https://make.wordpress.org/core/2020/11/23/wordpress-and-php-8-0/),
and thoroughly testing a site is recommended before upgrading it to PHP 8.

{%- assign collapsedCycles = page.releases  | where_exp:"r","r.releaseCycle != '3.6'" | collapse_cycles:"supportedPHPVersions"," - " %}
{% include table.html
  labels="Release,Supported PHP Versions"
  fields="releaseCycle,supportedPHPVersions"
  types="string,string"
  rows=collapsedCycles %}
