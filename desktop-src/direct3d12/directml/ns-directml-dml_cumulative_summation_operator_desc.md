---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Summiert die Elemente eines Tensors entlang einer Achse und schreibt die laufende Tally der Summierung in den Ausgabe-Tensor.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 2862a2add207b0bb6c41f5c1aabbc390797cba23
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803349"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a>DML_CUMULATIVE_SUMMATION_OPERATOR_DESC-Struktur (directml.h)

Summiert die Elemente eines Tensors entlang einer Achse und schreibt die laufende Tally der Summierung in den Ausgabe-Tensor.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Eingabe-Tensor, der elemente enthält, die summiert werden sollen.

`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe-Tensor, in den die resultierenden kumulativen Summierungen geschrieben werden sollen. Dieser Tensor muss die gleichen Größen und denselben Datentyp wie *inputTensor aufweisen.*

`Axis`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Der Index der Dimension, über die Elemente summt werden sollen. Dieser Wert muss kleiner als *dimensionCount* des *InputTensor* sein.

`AxisDirection`

Typ: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Einer der Werte [](./ne-directml-dml_axis_direction.md) der DML_AXIS_DIRECTION-Enumeration. Wenn auf **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, erfolgt die Summierung durch Durchlaufen des Tensors entlang der angegebenen Achse durch aufsteigenden Elementindex. Wenn auf **DML_AXIS_DIRECTION_DECREASING** festgelegt ist, ist der umgekehrte Wert true, und die Summierung erfolgt durch Durchlaufen von Elementen durch absteigenden Index.

`HasExclusiveSum`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

True gibt an, dass der Wert des aktuellen Elements beim Schreiben der ausgeführten Tally in den Ausgabe-Tensor ausgeschlossen wird. False gibt an, dass der Wert des aktuellen Elements in der ausgeführten Tally enthalten ist.

## <a name="examples"></a>Beispiele

In den Beispielen in diesem Abschnitt wird ein Eingabe tensor mit den folgenden Eigenschaften verwendet.

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-summation-across-horizontal-slivers"></a>Beispiel 1: Kumulative Summe über horizontale Schrägstriche

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  3,  6, 11],     // i.e. [2, 2+1, 2+1+3, 2+1+3+5]
   [3, 11, 18, 21],     //      [...                   ]
   [9, 15, 17, 21]]]]   //      [...                   ]
```

### <a name="example-2-exclusive-sums"></a>Beispiel 2: Exklusive Summen

Das *Festlegen von HasExclusiveSum* auf **TRUE** hat den Effekt, dass der Wert des aktuellen Elements beim Schreiben in den Ausgabemandor von der ausgeführten Zählung ausgenommen wird.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[0, 2,  3,  6],      // Notice the sum is written before adding the input,
   [0, 3, 11, 18],      // and the final total is not written to any output.
   [0, 9, 15, 17]]]]
```

### <a name="example-3-axis-direction"></a>Beispiel 3: Achsenrichtung

Das Festlegen *von AxisDirection* auf [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) hat den Effekt, dass die Durchlaufrichtung der Elemente beim Berechnen der ausgeführten Zählung umkehrt.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[11,  9,  8,  5],    // i.e. [2+1+3+5, 1+3+5, 3+5, 5]
   [21, 18, 10,  3],    //      [...                   ]
   [21, 12,  6,  4]]]]  //      [...                   ]
```

### <a name="example-4-summing-along-a-different-axis"></a>Beispiel 4. Summieren entlang einer anderen Achse

In diesem Beispiel erfolgt die Summe vertikal entlang der Höhenachse (zweite Dimension).

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 5,  9, 10,  8],   //      [2+3,  ...]
   [14, 15, 12, 12]]]] //      [2+3+9 ...]
```

## <a name="remarks"></a>Hinweise
Dieser Operator unterstützt die ausführungsbasierte Ausführung, d. h., der *OutputTensor* darf während der Bindung einen Alias für *den InputTensor* verwenden.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp und* die *gleichen Größen haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Ausgabe | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |
