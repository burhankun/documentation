---
title: Timelines API
menu:
  docs:
    parent: api
    weight: 10
---

## GET /api/v1/timelines/home

Returns array of [Status]({{< relref "entities.md#status" >}})

### Resource information

{{< api_method_info auth="Yes" user="Yes" scope="read read:statuses" version="0.0.0" >}}

### Parameters

|Name|Description|Required|Default|
|----|-----------|:------:|:-----:|
| `max_id` | Return results older than ID | Optional ||
| `since_id` | Return results newer than ID | Optional ||
| `limit` | Maximum number of results | Optional | 20 |

### Pagination

{{< api_dynamic_pagination >}}

## GET /api/v1/timelines/public

Returns array of [Status]({{< relref "entities.md#status" >}})

### Resource information

{{< api_method_info auth="No" user="No" scope="read read:statuses" version="0.0.0" >}}

### Parameters

|Name|Description|Required|Default|
|----|-----------|:------:|:-----:|
| `local` | Only local statuses | Optional ||
| `only_media` | Only statuses with media attachments | Optional ||
| `max_id` | Return results older than ID | Optional ||
| `since_id` | Return results newer than ID | Optional ||
| `limit` | Maximum number of results | Optional | 20 |

### Pagination

{{< api_dynamic_pagination >}}

## GET /api/v1/timelines/tag/:hashtag

Returns array of [Status]({{< relref "entities.md#status" >}})

### Resource information

{{< api_method_info auth="No" user="No" scope="read read:statuses" version="0.0.0" >}}

### Parameters

|Name|Description|Required|Default|
|----|-----------|:------:|:-----:|
| `local` | Only local statuses | Optional ||
| `only_media` | Only statuses with media attachments | Optional ||
| `max_id` | Return results older than ID | Optional ||
| `since_id` | Return results newer than ID | Optional ||
| `limit` | Maximum number of results | Optional | 20 |

### Pagination

{{< api_dynamic_pagination >}}

## GET /api/v1/timelines/list/:list_id

Returns array of [Status]({{< relref "entities.md#status" >}})

### Resource information

{{< api_method_info auth="Yes" user="Yes" scope="read read:statuses" version="0.0.0" >}}

### Parameters

|Name|Description|Required|Default|
|----|-----------|:------:|:-----:|
| `max_id` | Get a list of statuses with ID less than this value | Optional ||
| `since_id` | Get a list of statuses with ID greater than this value | Optional ||
| `limit` | Maximum number of statuses to return | Optional | 20 |

### Pagination

{{< api_dynamic_pagination >}}