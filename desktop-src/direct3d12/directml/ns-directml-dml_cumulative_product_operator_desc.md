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
ms.openlocfilehash: cb4006a20dd25751c027ba97e63dcfc60c25faf6
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282559"
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

Der Ausgabe tensor, in den die resultierenden kumulativen Produkte geschrieben werden. Dieser Tensor muss die gleichen Größen und Datentypen wie *InputTensor haben.*

`Axis`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Der Index der Dimension, über die Elemente multipliziert werden. Dieser Wert muss kleiner als *dimensionCount des* *InputTensor-Werts sein.*

`AxisDirection`

Typ: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Einer der Werte der [DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction) Enumeration. Wenn auf **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, wird das Produkt durch Durchlaufen des Tensors entlang der angegebenen Achse durch den aufsteigenden Elementindex angezeigt. Wenn auf **DML_AXIS_DIRECTION_DECREASING** festgelegt ist, ist die Umkehrung true, und das Produkt tritt auf, indem Elemente durch einen absteigenden Index durchlaufen werden.

`HasExclusiveProduct`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

True **gibt** an, dass der Wert des aktuellen Elements ausgeschlossen wird, wenn die laufende Klammer in den Ausgabemandator geschrieben wird. False **gibt** an, dass der Wert des aktuellen Elements in der ausgeführten Zählung enthalten ist.

## <a name="examples"></a>Beispiele

In den Beispielen in diesem Abschnitt wird der gleiche Eingabetensor verwendet.

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a>Beispiel 1: Kumulatives Produkt über horizontale Schrägstriche

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

Das *Festlegen von HasExclusiveProduct* auf **TRUE** hat den Effekt, dass der Wert des aktuellen Elements beim Schreiben in den Ausgabemandor von der ausgeführten Zählung ausgenommen wird.

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

Das Festlegen *von AxisDirection* auf [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) hat den Effekt, dass die Durchlaufrichtung der Elemente beim Berechnen der laufenden Zählung umkehrt.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a>Beispiel 4. Multiplizieren entlang einer anderen Achse

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

## <a name="remarks"></a>Bemerkungen
Dieser Operator unterstützt die in-place-Ausführung, was bedeutet, dass der Ausgabetensor während der Bindung den *Alias InputTensor* verwenden darf.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*InputTensor* und *OutputTensor* müssen denselben *DataType,* *DimensionCount* und *die gleichen Größen aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_4_0-and-above"></a>DML_FEATURE_LEVEL_4_0 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Output | 1 bis 8 | FLOAT32, FLOAT16, UINT32, UINT16 |

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |

## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |