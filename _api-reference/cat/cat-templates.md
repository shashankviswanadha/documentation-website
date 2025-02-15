---
layout: default
title: CAT templates
parent: CAT API

nav_order: 70
has_children: false
redirect_from:
- /opensearch/rest-api/cat/cat-templates/
---

# CAT templates
**Introduced 1.0**
{: .label .label-purple }

The CAT templates operation lists the names, patterns, order numbers, and version numbers of index templates.


## Endpoints

```json
GET _cat/templates
```

## Query parameters

Parameter | Type | Description
:--- | :--- | :---
local | Boolean | Whether to return information from the local node only instead of from the cluster manager node. Default is `false`.
cluster_manager_timeout | Time | The amount of time to wait for a connection to the cluster manager node. Default is 30 seconds.

## Example requests

The following example request returns information about all templates:

```json
GET _cat/templates?v
```
{% include copy-curl.html %}

If you want to get information for a specific template or pattern:

```json
GET _cat/templates/<template_name_or_pattern>
```
{% include copy-curl.html %}


## Example response

```
name | index_patterns order version composed_of
tenant_template | [opensearch-dashboards*] | 0  |    
```

To learn more about index templates, see [Index templates]({{site.url}}{{site.baseurl}}/opensearch/index-templates).
