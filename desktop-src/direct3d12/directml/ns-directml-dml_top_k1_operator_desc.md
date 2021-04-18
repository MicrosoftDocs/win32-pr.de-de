---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Wählt die größten oder kleinsten *K* -Elemente aus jeder Sequenz entlang einer Achse von *inputtensor* aus und gibt die Werte und Indizes dieser Elemente in *outputvaluetensor* bzw. *outputindextensor* zurück.
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
ms.openlocfilehash: 8c5b9bf58a8582588d19878c7e06c602584777fa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351191"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a>DML_TOP_K1_OPERATOR_DESC-Struktur (directml. h)
Wählt die größten oder kleinsten *K* -Elemente aus jeder Sequenz entlang einer Achse von *inputtensor* aus und gibt die Werte und Indizes dieser Elemente in *outputvaluetensor* bzw. *outputindextensor* zurück. Eine *Sequenz* verweist auf eine Reihe von Elementen, die entlang der *Achsen* Dimension von *inputtensor* vorhanden sind.

Die Auswahl, ob die größten k-Elemente oder die kleinsten k-Elemente ausgewählt werden sollen, kann mithilfe von *axisdirection* gesteuert werden.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingabensor mit den Elementen, die ausgewählt werden sollen.


`OutputValueTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe Mandanten, in den die Werte der obersten *K* Elemente geschrieben werden sollen. Abhängig vom Wert von *axisdirection* werden die obersten *K* Elemente basierend darauf ausgewählt, ob Sie der größte oder kleinste Wert sind. Dieser tensorflow muss Übergrößen verfügen, die mit dem *inputtensor* identisch sind, *mit Ausnahme* der durch den *Axis* -Parameter angegebenen Dimension, deren Größe gleich *K* sein muss.

Die aus jeder Eingabe Sequenz ausgewählten *K* -Werte werden garantiert absteigend sortiert (der größte zu kleinste Wert), wenn *axisdirection* [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md)ist. Andernfalls ist das Gegenteil der Fall, und die ausgewählten Werte werden garantiert aufsteigend sortiert (der kleinste zum größten Wert).


`OutputIndexTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe Mandanten, in den die Indizes der obersten *K* Elemente geschrieben werden sollen. Dieser tensorflow muss Übergrößen verfügen, die mit dem *inputtensor* identisch sind, *mit Ausnahme* der durch den *Axis* -Parameter angegebenen Dimension, deren Größe gleich *K* sein muss.

Die Indizes, die in diesem Mandanten zurückgegeben werden, werden relativ zum Anfang der Sequenz (im Gegensatz zum Anfang des Mandanten) gemessen. Beispielsweise verweist der Index 0 immer auf das erste Element für alle Sequenzen in einer Achse.

In Fällen, in denen zwei oder mehr Elemente im oberen-K denselben Wert aufweisen (d. h., wenn ein gleich geordnetes Element vorhanden ist), werden die Indizes beider Elemente eingeschlossen, und die Sortierung erfolgt nach dem aufsteigenden Element Index. Beachten Sie, dass dies unabhängig vom Wert von *axisdirection* true ist.


`Axis`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Der Index der Dimension, in der Elemente ausgewählt werden sollen. Dieser Wert muss kleiner als die *DimensionCount* von " *inputtensor*" sein.


`K`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Elemente, die ausgewählt werden sollen. *K* muss größer als 0 (null) sein, aber kleiner als die Anzahl der Elemente im *inputtensor* entlang der durch die *Achse* angegebenen Dimension.


`AxisDirection`

Typ: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Ein Wert aus der [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) Enumeration. Wenn **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, gibt dieser Operator die *kleinsten* *K* Elemente in der Reihenfolge zurück, in der der Wert zunimmt. Andernfalls werden die *größten* *K* Elemente in absteigender Reihenfolge zurückgegeben.

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

### <a name="example-3-tied-values"></a>Beispiel 3: Gebundene Werte

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

### <a name="example-4-increasing-axis-direction"></a>Beispiel 4: Erhöhen der Achsen Richtung

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


## <a name="remarks"></a>Bemerkungen
Wenn *axisdirection* auf [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md)festgelegt ist, entspricht dieser Operator [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *Inputtensor* und *outputvaluetensor* müssen denselben *Datentyp* aufweisen.
* *Outputindextensor* und *outputvaluetensor* müssen die gleichen *Größen* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Dimensionen | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | { In0, In1, In2, In3 } | 4 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Outputvaluetensor | Ausgabe | { Out0, Out1, Out2, Out3 } | 4 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Outputindextensor | Ausgabe | { Out0, Out1, Out2, Out3 } | 4 | UINT32 |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |