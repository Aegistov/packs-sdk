---
nav: "ParamDef"
note: "This file is autogenerated from TypeScript definitions. Make edits to the comments in the TypeScript file and then run `make docs` to regenerate this file."
search:
  boost: 0.1
---
# Interface: ParamDef<T\>

[core](../modules/core.md).ParamDef

The definition of a formula parameter.

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends `UnionType` |

## Hierarchy

- **`ParamDef`**

  ↳ [`OptionalParamDef`](core.OptionalParamDef.md)

## Properties

### autocomplete

• `Optional` **autocomplete**: [`MetadataFormula`](../types/core.MetadataFormula.md)

A [MetadataFormula](../types/core.MetadataFormula.md) that returns valid values for this parameter, optionally matching a search
query. This can be useful both if there are a fixed number of valid values for the parameter,
or if the valid values from the parameter can be looked up from some API.
Use [makeMetadataFormula](../functions/core.makeMetadataFormula.md) to wrap a function that implements your autocomplete logic.
Typically once you have fetched the list of matching values, you'll use
[autocompleteSearchObjects](../functions/core.autocompleteSearchObjects.md) to handle searching over those values.
If you have a hardcoded list of valid values, you would only need to use
[makeSimpleAutocompleteMetadataFormula](../functions/core.makeSimpleAutocompleteMetadataFormula.md).

___

### defaultValue

• `Optional` **defaultValue**: [`SuggestedValueType`](../types/core.SuggestedValueType.md)<`T`\>

**`Deprecated`**

This will be removed in a future version of the SDK. Use [suggestedValue](core.ParamDef.md#suggestedvalue) instead.

___

### description

• **description**: `string`

A brief description of what this parameter is used for, shown to the user when invoking the formula.

___

### name

• **name**: `string`

The name of the parameter, which will be shown to the user when invoking this formula.

___

### optional

• `Optional` **optional**: `boolean`

Whether this parameter can be omitted when invoking the formula.
All optional parameters must come after all non-optional parameters.

___

### suggestedValue

• `Optional` **suggestedValue**: [`SuggestedValueType`](../types/core.SuggestedValueType.md)<`T`\>

The suggested value to be prepopulated for this parameter if it is not specified by the user.

___

### type

• **type**: `T`

The data type of this parameter (string, number, etc).
