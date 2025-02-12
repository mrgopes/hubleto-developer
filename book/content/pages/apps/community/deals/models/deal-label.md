# Model DealLabel

namespace HubletoApp\Deals\Models\DealLabel

Labels given to a Deal

## Constants

This model does not define constants.

## Properties

| Property                                                                                 | Value                     |
| :--------------------------------------------------------------------------------------- | :------------------------ |
| [eloquentClass](https://docs.wai.blue/adios-framework/models/properties#eloquentClass)   | Eloquent\DealLabel::class |
| [table](https://docs.wai.blue/adios-framework/models/properties#table)                   | deal_labels               |
| [lookupSqlValue](https://docs.wai.blue/adios-framework/models/properties#lookupSqlValue) | [TABLE].id                |

## Data Scructure

| Column   | Title | ADIOS Type                                                               | Length | Required |
| -------- | ----- | ------------------------------------------------------------------------ | ------ | -------- |
| id_deal  | Deal  | [lookup](https://docs.wai.blue/adios-framework/models/attributes#lookup) |        | TRUE     |
| id_label | Label | [lookup](https://docs.wai.blue/adios-framework/models/attributes#lookup) |        | TRUE     |

## Foreign Keys

| Column   | Model                                                                        | Relation | OnUpdate | OnDelete |
| -------- | ---------------------------------------------------------------------------- | -------- | -------- | -------- |
| id_deal  | [Modules\Sales\Deals\Models\Deal](deal)                                 | 1:1      | Cascade  | Restrict |
| id_label | [Modules\Core\Settings\Models\Label](../../../core/settings/models/label) | 1:1      | Cascade  | Restrict |

## Indexes

Only [default indexes](https://docs.wai.blue/adios-framework/default-indexes) are used.

## Relations

| Relation | Type       | Other parameters              |
| -------- | ---------- | ----------------------------- |
| DEAL     | BELONGS_TO | Deal::class, 'id_deal','id'   |
| LABEL    | BELONGS_TO | Label::class, 'id_label','id' |
