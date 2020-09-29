---
title: Basic Authorization
description: Manage Chronograf security with Basic Authorization.
menu:
  chronograf_1_8:
    name: Basic Authorization
    weight: 70
    parent: Administration
---

This PR allows to turn on HTTP basic access authentication so that all HTTP requests to chronograf are restricted to selected users.
This is possible on CLI with --htpasswd <path to .htpasswd file> or with HTPASSWD environment variable.

The .htpasswd file contains users and their passwords, it is usually managed by the htpasswd utility,
see https://docs.nginx.com/nginx/admin-guide/security-controls/configuring-http-basic-authentication/ to know more.
This type of authentication should be used in cases, in which OAuth integration is not possible.

Warning: When using basic authentication, the authorization rules of Chronograf are not enforced.
Basic access authentication only controls who can access Chronograf, users are then super users.

