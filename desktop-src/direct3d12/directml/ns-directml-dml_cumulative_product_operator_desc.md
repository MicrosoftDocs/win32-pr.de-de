---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Multipliziert die Elemente eines Tensors entlang einer Achse und schreibt die laufende Zählung des Produkts in den Ausgabemandor.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 71a078ad0f47c19ad1964d8d21f22e06822b5d01
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550215"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a>DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)

Multipliziert die Elemente eines Tensors entlang einer Achse und schreibt die laufende Zählung des Produkts in den Ausgabemandor.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Eingabedaten enthält. Dies ist in der Regel der gleiche Tensor, der als *InputTensor* bereitgestellt wurde, um DML_BATCH_NORMALIZATION_OPERATOR_DESC [**vorwärts**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) zu übergeben.

Der Eingabetensor, der zu multiplizierte Elemente enthält.

`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe tensor, in den die resultierenden kumulativen Produkte geschrieben werden. Dieser Tensor muss die gleichen Größen und datentypen wie *InputTensor haben.*

`Axis`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Der Index der Dimension, über die Elemente multipliziert werden. Dieser Wert muss kleiner als *dimensionCount des* *InputTensor sein.*

`AxisDirection`

Typ: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Einer der Werte der [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) Enumeration. Wenn auf **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, wird das Produkt durch Durchlaufen des Tensors entlang der angegebenen Achse durch den aufsteigenden Elementindex angezeigt. Wenn auf **DML_AXIS_DIRECTION_DECREASING** festgelegt ist, ist die Umkehrung true, und das Produkt tritt auf, indem Elemente durch einen absteigenden Index durchlaufen werden.

`HasExclusiveProduct`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

True gibt an, dass der Wert des aktuellen Elements beim Schreiben der ausgeführten Tally in den Ausgabe-Tensor ausgeschlossen wird. False gibt an, dass der Wert des aktuellen Elements in der ausgeführten Tally enthalten ist.

## <a name="examples"></a>Beispiele

In den Beispielen in diesem Abschnitt wird der gleiche Eingabe-Tensor verwendet.

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a>Beispiel 1: Kumulatives Produkt über horizontale Splitter hinweg

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a>Beispiel 2: Exklusive Produkte

Wenn *HasExclusiveProduct* auf **TRUE** festgelegt wird, wird der Wert des aktuellen Elements beim Schreiben in den Ausgabe-Tensor von der ausgeführten Tally ausgeschlossen.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a>Beispiel 3: Achsenrichtung

Wenn *AxisDirection* auf [**DML_AXIS_DIRECTION_DECREASING**](./ne-directml-dml_axis_direction.md) festgelegt wird, wird die Durchlaufreihenfolge von Elementen umgekehrt, wenn die ausgeführte tally-Berechnung erfolgt.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a>Beispiel 4. Multiplizieren auf einer anderen Achse

In diesem Beispiel tritt das Produkt vertikal entlang der Höhenachse (zweite Dimension) auf.

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a>Hinweise
Dieser Operator unterstützt die direkt ausgeführte Ausführung, was bedeutet, dass der Ausgabe-Tensor während der Bindung den Alias *InputTensor* aliasen darf.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp* und die gleichen *Größen* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Ausgabe | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |