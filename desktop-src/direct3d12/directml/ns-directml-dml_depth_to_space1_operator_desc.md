---
UID: NS:directml.DML_DEPTH_TO_SPACE1_OPERATOR_DESC
title: DML_DEPTH_TO_SPACE1_OPERATOR_DESC
description: Ordnet (permutiert) Daten aus der Tiefe in Blöcke räumlicher Daten neu. Der Operator gibt eine Kopie des Eingabe-Tensors aus, bei dem Werte aus der Tiefendimension in räumliche Blöcke in die Höhe und Breite verschoben werden.
helpviewer_keywords:
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure
- direct3d12.dml_depth_to_space1_operator_desc
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.openlocfilehash: 89b62a9916ee77dd6907d01710624d6e9a40a20a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417863"
---
# <a name="dml_depth_to_space1_operator_desc-structure-directmlh"></a>DML_DEPTH_TO_SPACE1_OPERATOR_DESC-Struktur (directml.h)

Ordnet (permutiert) Daten aus der Tiefe in Blöcke räumlicher Daten neu. Der Operator gibt eine Kopie des Eingabe-Tensors aus, bei dem Werte aus der Tiefendimension in räumliche Blöcke in die Höhe und Breite verschoben werden.

Dies ist die umgekehrte Transformation von [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_DEPTH_TO_SPACE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, aus dem gelesen werden soll. Die Dimensionen des Eingabe-Tensors sind `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, in den die Ergebnisse geschrieben werden sollen. Die Dimensionen des Ausgabe-Tensors sind `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` , wobei:

* OutputChannelCount wird als InputChannelCount /( ) berechnet. `BlockSize`  *  `BlockSize`
* OutputHeight wird als InputHeight * berechnet. `BlockSize`
* OutputWidth wird als InputWidth * berechnet. `BlockSize`


`BlockSize`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Breite und Höhe der Blöcke, die verschoben werden.


`Order`

Typ: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**

Weitere Informationen finden Sie [unter DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).

## <a name="examples"></a>Beispiele

In den Beispielen in diesem Abschnitt wird die folgende Eingabe verwendet.

```
InputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

### <a name="example-1-depth-column-row-order"></a>Beispiel 1: Reihenfolge der Tiefenspaltenzeilen

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a>Beispiel 2: Reihenfolge der Spaltenzeilentiefe

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
```


## <a name="remarks"></a>Hinweise
Wenn *Order* auf [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md)festgelegt **ist,** entspricht DML_DEPTH_TO_SPACE1_OPERATOR_DESC [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Dimensionen | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Eingabe | { BatchCount, InputChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Ausgabe | { BatchCount, OutputChannelCount, OutputHeight, OutputWidth } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Siehe auch

* [DML_DEPTH_TO_SPACE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc)
* [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md)