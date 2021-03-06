---
title: printerShare resource type
description: Represents a printer that is intended to be discoverable by users and printing applications.
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: resourcePageType
---

# printerShare resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a printer that is intended to be discoverable by users and printing applications.

## Methods

| Method       | Return Type | Description |
|:-------------|:------------|:------------|
| [List](../api/print-list-printershares.md) | [printerShare](printershare.md) collection | Get a list of printer shares in the tenant. |
| [Get](../api/printershare-get.md) | [printerShare](printershare.md) | Read properties and relationships of a **printerShare** object. |
| [Update](../api/printershare-update.md) | [printerShare](printershare.md) | Update a **printerShare** object. |
| [Delete](../api/printershare-delete.md) | None | Unshare a printer. |
| [List allowedUsers](../api/printershare-list-allowedusers.md) | [userIdentity](useridentity.md) collection | Retrieve a list of users who have been granted access to submit print jobs to the associated printer share. |
| [Add allowedUser](../api/printershare-post-allowedusers.md) | None | Grant the specified user access to submit print jobs to the associated printer share. |
| [Remove allowedUser](../api/printershare-delete-alloweduser.md) | None | Revoke printer share access from the specified user. |
| [List allowedGroups](../api/printershare-list-allowedgroups.md) | [identity](identity.md) collection | Retrieve a list of groups that have been granted access to submit print jobs to the associated printer share. |
| [Add allowedGroup](../api/printershare-post-allowedgroups.md) | None | Grant the specified group access to submit print jobs to the associated printer share. |
| [Remove allowedGroup](../api/printershare-delete-allowedgroup.md) | None | Revoke printer share access from the specified group. |

## Properties
| Property     | Type        | Description |
|:-------------|:------------|:------------|
|id|String| The printerShare's identifier. Read-only.|
|name|String|The name of the printer share that print clients should display.|
|createdDateTime|DateTimeOffset|The DateTimeOffset when the printer share was created. Read-only.|

## Relationships
| Relationship | Type        | Description |
|:-------------|:------------|:------------|
|printer|[printer](printer.md)|The printer that this printer share is related to. |
|allowedUsers|[userIdentity](useridentity.md) collection|The users who have access to print using the printer.|
|allowedGroups|[identity](identity.md)|The groups whose users have access to print using the printer.|

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.printerShare",
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity"
}-->

```json
{
  "id": "String (identifier)",
  "name": "String",
  "createdDateTime": "String (timestamp)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "printerShare resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
