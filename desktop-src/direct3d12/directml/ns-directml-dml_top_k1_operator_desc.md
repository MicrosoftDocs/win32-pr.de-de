---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Wählt die größten oder kleinsten *K-Elemente* aus jeder Sequenz entlang einer Achse des *InputTensor* aus und gibt die Werte und Indizes dieser Elemente im *OutputValueTensor* bzw. *OutputIndexTensor* zurück.
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803817"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a>DML_TOP_K1_OPERATOR_DESC -Struktur (directml.h)
Wählt die größten oder kleinsten *K-Elemente* aus jeder Sequenz entlang einer Achse des *InputTensor* aus und gibt die Werte und Indizes dieser Elemente im *OutputValueTensor* bzw. *OutputIndexTensor* zurück. Eine *Sequenz* bezieht sich auf einen der Sätze von Elementen, die entlang der *Axis-Dimension* von *InputTensor vorhanden sind.*

Die Wahl, ob die größten K-Elemente oder die kleinsten K-Elemente ausgewählt werden sollen, kann mit *AxisDirection gesteuert werden.*

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Eingabetensor, der auszuwählende Elemente enthält.

`OutputValueTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe tensor, in den die Werte der obersten *K-Elemente geschrieben* werden. Die obersten *K-Elemente* werden abhängig vom Wert von *AxisDirection* ausgewählt, je nachdem, ob sie das größte oder das kleinste sind. Dieser Tensor muss größen gleich dem *InputTensor* *aufweisen,* mit Ausnahme der dimension, die durch den *Axis-Parameter* angegeben wird, der eine Größe von K *aufweisen muss.*

Die in jeder Eingabesequenz ausgewählten *K-Werte* werden garantiert absteigend sortiert (größte bis [kleinste),](./ne-directml-dml_axis_direction.md)wenn *AxisDirection* DML_AXIS_DIRECTION_DECREASING. Andernfalls ist das Gegenteil true, und die ausgewählten Werte sind garantiert aufsteigend sortiert (klein bis größten).

`OutputIndexTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe tensor, in den die Indizes der obersten *K-Elemente geschrieben* werden. Dieser Tensor muss größengleich mit *inputTensor* sein, *mit Ausnahme* der Dimension, die durch den *Axis-Parameter* angegeben wird und eine Größe von *gleich K* aufweisen muss.

Die in diesem Tensor zurückgegebenen Indizes werden relativ zum Anfang ihrer Sequenz gemessen (im Gegensatz zum Anfang des Tensors). Beispielsweise bezieht sich ein Index von 0 immer auf das erste Element für alle Sequenzen in einer Achse.

In Fällen, in denen zwei oder mehr Elemente im oberen K den gleichen Wert haben (d. h. wenn ein Gleichstand vorliegt), werden die Indizes beider Elemente eingeschlossen und werden garantiert nach aufsteigender Elementindex sortiert. Beachten Sie, dass dies unabhängig vom Wert von *AxisDirection* zutrifft.

`Axis`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Der Index der Dimension, über die Elemente ausgewählt werden sollen. Dieser Wert muss kleiner als *dimensionCount* des *InputTensor* sein.

`K`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der auszuwählende Elemente. *K* muss größer als 0 sein, aber kleiner als die Anzahl der Elemente im *InputTensor* entlang der Dimension, die von *Achse* angegeben wird.

`AxisDirection`

Typ: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Ein Wert [](./ne-directml-dml_axis_direction.md) aus der DML_AXIS_DIRECTION-Enumeration. Wenn auf **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, gibt dieser Operator die *kleinsten* *K-Elemente* in der Reihenfolge des erhöhenden Werts zurück. Andernfalls werden die *größten* *K-Elemente* in absteigender Reihenfolge zurückgegeben.

## <a name="examples"></a>Beispiele

### <a name="example-1"></a>Beispiel 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a>Beispiel 2: Verwenden einer anderen Achse

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a>Beispiel 3: Verknüpfte Werte

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a>Beispiel 4. Erhöhen der Achsenrichtung

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a>Hinweise
Wenn *AxisDirection* auf [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md)festgelegt ist, entspricht dieser Operator [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen

* *InputTensor,* *OutputIndexTensor* und *OutputValueTensor* müssen denselben *DimensionCount aufweisen.*
* *InputTensor und* *OutputValueTensor* müssen denselben *Datentyp haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 und höher

| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Ausgabe | 1 bis 8 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher

| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Ausgabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Ausgabe | 4 | UINT32 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |
