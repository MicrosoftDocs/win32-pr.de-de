---
UID: NS:directml.DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
title: DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
description: Füllt einen tensorflow mit dem angegebenen Konstanten *Wert*.
helpviewer_keywords:
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure
- direct3d12.dml_fill_value_constant_operator_desc
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.openlocfilehash: d2b69f1f6b1c9768c24cab9a58bba3c3cadb04bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106362806"
---
# <a name="dml_fill_value_constant_operator_desc-structure-directmlh"></a>DML_FILL_VALUE_CONSTANT_OPERATOR_DESC-Struktur (directml. h)

Füllt einen tensorflow mit dem angegebenen Konstanten *Wert*. Dieser Operator führt den folgenden Pseudocode aus.

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
endfor
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax
```cpp
struct DML_FILL_VALUE_CONSTANT_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      Value;
};
```



## <a name="members"></a>Member

`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der tensorflow, in den die Ergebnisse geschrieben werden sollen. Dieser Mandanten kann eine beliebige Größe aufweisen.


`ValueDataType`

Typ: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**

Der Datentyp des *Wertfelds* , das " *outputtensor. DataType*" entsprechen muss.


`Value`

Typ: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**

Ein konstanter Wert zum Auffüllen der Ausgabe mit *valuedatatype* , der bestimmt, wie das Feld interpretiert werden soll.

## <a name="examples"></a>Beispiele

```
Value = 13.0

OutputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
    [[[[13.0f, 13.0f, 13.0f, 13.0f],
       [13.0f, 13.0f, 13.0f, 13.0f]]]]
```

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Outputtensor | Ausgabe | 4 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |