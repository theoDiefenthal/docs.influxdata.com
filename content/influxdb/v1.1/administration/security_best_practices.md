---
title: Security Best Practices
menu:
  influxdb_1_1:
    weight: 80
    parent: administration
---

Exposing InfluxDB to the open internet also exposes your data.
Check out the sections below for how protect the data in your InfluxDB instance.

## Enable Authentication

Password protect your InfluxDB instance to keep any unauthorized individuals
from accessing you data.

Resources:
[Set up Authentication](/influxdb/v1.1/query_language/authentication_and_authorization/#set-up-authentication)

## Manage Users and their Permissions

Prevent unintentional mishaps by creating individual users and assigning them
the relevant read and/or write permissions.

Resources:
[User Types and Privileges](/influxdb/v1.1/query_language/authentication_and_authorization/#user-types-and-privileges),
[User Management Commands](/influxdb/v1.1/query_language/authentication_and_authorization/#user-management-commands)

## Set up HTTPS

HTTPS secures the communication between clients and the InfluxDB server, and, in
some cases, HTTPS verifies the authenticity of the InfluxDB server to clients.

Resources:
[HTTPS Setup](/influxdb/v1.1/administration/https_setup/)

## Secure your Host

Keep InfluxDB safe by securing its host.

### Ports
If you're only running InfluxDB, close all ports on the host except for port `8086`.
You can also use a proxy to port `8086`.

### AWS Recommendations

If you're hosting InfluxDB on AWS, be sure to encrypt the disk/volume.