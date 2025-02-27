---
title: "room resource type"
description: "Specifies the properties of a room in a tenant."
ms.localizationpriority: medium
author: "vrod9429"
ms.prod: "outlook"
doc_type: "resourcePageType"
---

# room resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a room in a tenant. 

In Exchange Online, each room is associated with a room mailbox. Derived from [place](place.md).

## Methods

| Method                              | Return Type                  | Description |
|:------------------------------------|:-----------------------------|:--------|
| [List places](../api/place-list.md) | A collection of the requested, derived type of [place](place.md) | Get a collection of the specified type of **place** object defined in the tenant. For example, you can get all the rooms, all the room lists, or the rooms in a specific room list in the tenant. |
| [Get place](../api/place-get.md)    | The requested, derived type of [place](place.md)            | Get the properties and relationships of the specified **place** object, such as a room. |

## Properties

| Property               | Type                                              | Description |
|:-----------------------|:--------------------------------------------------|:--|
| address                | [physicalAddress](physicaladdress.md)             | The street address of the room. |
| audioDeviceName        | String                                            | Specifies the name of the audio device in the room. |
| bookingType            | [bookingType](#bookingtype-values)                | Type of room. Possible values are `standard`, and `reserved`. |
| building               | String                                            | Specifies the building name or building number that the room is in. |
| capacity               | Int32                                             | Specifies the capacity of the room. |
| displayName            | String                                            | The name associated with the room. |
| displayDeviceName      | String                                            | Specifies the name of the display device in the room. |
| emailAddress           | String                                            | Email address of the room. |
| floorLabel             | String                                            | Specifies a descriptive label for the floor, for example, P. |
| floorNumber            | Int32                                             | Specifies the floor number that the room is on. |
| geoCoordinates         | [outlookGeoCoordinates](outlookgeocoordinates.md) | Specifies the room location in latitude, longitude and optionally, altitude coordinates. |
| id                     | String                                            | Unique identifier for the room. Read-only. |
| isWheelChairAccessible | Boolean                                           | Specifies whether the room is wheelchair accessible. |
| label                  | String                                            | Specifies a descriptive label for the room, for example, a number or name. |
| nickname               | String                                            | Specifies a nickname for the room, for example, "conf room". |
| phone                  | String                                            | The phone number of the room. |
| placeId                | String                                            | An alternate immutable unique identifier of the place. |
| tags                   | String collection                                 | Specifies other features of the room; for example, the type of view or furniture type. |
| videoDeviceName        | String                                            | Specifies the name of the video device in the room. |

### bookingType values

| Value    | Description                                               |
|:---------|:----------------------------------------------------------|
| standard | The room can be reserved based on the other settings in this cmdlet. This is the default value. |
| reserved | The room is available only on a first come, first served basis. It can't be reserved.|

## Relationships

None.

## JSON representation

The following JSON representation shows the resource type.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.room"
}-->

```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "audioDeviceName": "String",
  "bookingType": "String",
  "building": "String",
  "capacity": 1024,
  "displayName": "String",
  "displayDeviceName": "String",
  "emailAddress": "String",
  "floorLabel": "String",
  "floorNumber": 1024,
  "geoCoordinates": {"@odata.type": "microsoft.graph.outlookGeoCoordinates"},
  "id": "String (identifier)",
  "isWheelChairAccessible": true,
  "label": "String",
  "nickname": "String",
  "phone": "String",
  "tags": ["String"],
  "videoDeviceName": "String",
  "placeId": "String (alternate identifier)"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "room resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


