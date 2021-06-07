---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Kopiert den gesamten Eingabe tensor in die Ausgabe und überschreibt dann ausgewählte Indizes mit entsprechenden Werten aus dem Aktualisierungs tensor.
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: 6c987e01862d849c6215a2d25fe957ef0a22e7af
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417714"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a>DML_SCATTER_ND_OPERATOR_DESC -Struktur (directml.h)
Kopiert den gesamten Eingabe tensor in die Ausgabe und überschreibt dann ausgewählte Indizes mit entsprechenden Werten aus dem Aktualisierungs tensor. Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten dar, mit dem genauen Verhalten, das durch die Achsen- und Indexgröße bestimmt wird.

```
output = input
output[indices[...]] = updates[...]
```

Wenn sich zwei Ausgabeelementindizes überlappen (ungültig), gibt es keine Garantie dafür, welcher letzte Schreibzugriff gewinnt.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, aus dem gelesen werden soll.


`IndicesTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Indizes enthält. DimensionCount *dieses* Tensors muss mit *InputTensor.DimensionCount übereinstimmen.* Die letzte Dimension des *IndicesTensor* ist tatsächlich die Anzahl der Koordinaten pro Index-Tupel und darf *InputTensor.DimensionCount nicht überschreiten.* Beispielsweise bedeutet ein Indizestensor der Größe mit `{1,4,5,2}` *IndicesDimensionCount* = 3 ein 4x5-Array von Zwei-Wert-Koordinatentpeln, die in *InputTensor* indiziert werden.

Ab unterstützt dieser Operator negative Indexwerte, wenn ein integraler Typ mit `DML_FEATURE_LEVEL_3_0` Vorsignierung mit diesem Tensor verwendet wird. Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert. Ein Index von -1 bezieht sich beispielsweise auf das letzte Element in dieser Dimension.


`UpdatesTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die neuen Werte enthält, um die vorhandenen Eingabewerte an den entsprechenden Indizes zu ersetzen. DimensionCount *dieses* Tensors muss mit *InputTensor.DimensionCount übereinstimmen.* Die erwarteten *UpdatesTensor.Sizes* sind die Verkettung der führenden Segmente *IndicesTensor.Sizes* und *InputTensor.Sizes,* um Folgendes zu erzielen.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

Die Dimensionen sind rechtsbündig ausgerichtet, und führenden 1 Werten wird bei Bedarf vorgefertigt, um *UpdatesTensor.DimensionCount zu erfüllen.*

Hier ist ein Beispiel.

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, in den die Ergebnisse geschrieben werden. Die *Größen und* der Datentyp *dieses* Tensors müssen mit *InputTensor.Sizes übereinstimmen.*


`InputDimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der tatsächlichen Eingabedimensionen innerhalb des *InputTensor,* nachdem alle irrelevanten führenden Dimensionen im Bereich [1, *InputTensor.DimensionCount ) ignoriert wurden.* Wenn beispielsweise *InputTensor.Sizes* = {1,1,4,6} und *InputDimensionCount* = 3 angegeben sind, sind die tatsächlichen sinnvollen Indizes {1,4,6} .


`IndicesDimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der tatsächlichen Indexdimensionen innerhalb des *IndizesTensors,* nachdem alle irrelevanten führenden Dimensionen im Bereich [1, *IndicesTensor.DimensionCount ) ignoriert wurden.* Wenn beispielsweise *IndicesTensor.Sizes* = {1,1,4,6} und *IndicesDimensionCount* = 3 angegeben sind, sind die tatsächlichen sinnvollen Indizes {1,4,6} .

## <a name="examples"></a>Beispiele

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *IndicesTensor,* *InputTensor,* *OutputTensor* und müssen `UpdatesTensor` denselben *DimensionCount aufweisen.*
* *InputTensor*, *OutputTensor* und `UpdatesTensor` müssen denselben *Datentyp haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Eingabe | 1 bis 8 | INT64, INT32, UINT64, UINT32 |
| UpdatesTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Eingabe | 4 | UINT32 |
| UpdatesTensor | Eingabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Ausgabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |