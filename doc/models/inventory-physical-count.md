## Inventory Physical Count

Represents the quantity of an item variation that is physically present
at a specific location, verified by a seller or a seller's employee. For example,
a physical count might come from an employee counting the item variations on
hand or from syncing with an external system.

### Structure

`InventoryPhysicalCount`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | A unique ID generated by Square for the<br>[InventoryPhysicalCount](#type-inventoryphysicalcount). |
| `reference_id` | `String` | Optional | An optional ID provided by the application to tie the<br>[InventoryPhysicalCount](#type-inventoryphysicalcount) to an external<br>system. |
| `catalog_object_id` | `String` | Optional | The Square generated ID of the<br>`CatalogObject` being tracked. |
| `catalog_object_type` | `String` | Optional | The `CatalogObjectType` of the<br>`CatalogObject` being tracked. Tracking is only<br>supported for the `ITEM_VARIATION` type. |
| `state` | [`String (Inventory State)`](/doc/models/inventory-state.md) | Optional | Indicates the state of a tracked item quantity in the lifecycle of goods. |
| `location_id` | `String` | Optional | The Square ID of the [Location](#type-location) where the related<br>quantity of items are being tracked. |
| `quantity` | `String` | Optional | The number of items affected by the physical count as a decimal string.<br>Can support up to 5 digits after the decimal point. |
| `source` | [`Source Application Hash`](/doc/models/source-application.md) | Optional | Provides information about the application used to generate a change. |
| `employee_id` | `String` | Optional | The Square ID of the [Employee](#type-employee) responsible for the<br>physical count. |
| `occurred_at` | `String` | Optional | A client-generated timestamp in RFC 3339 format that indicates when<br>the physical count took place. For write actions, the `occurred_at`<br>timestamp cannot be older than 24 hours or in the future relative to the<br>time of the request. |
| `created_at` | `String` | Optional | A read-only timestamp in RFC 3339 format that indicates when Square<br>received the physical count. |

### Example (as JSON)

```json
{
  "id": "id0",
  "reference_id": "reference_id2",
  "catalog_object_id": "catalog_object_id6",
  "catalog_object_type": "catalog_object_type6",
  "state": "IN_TRANSIT_TO"
}
```

