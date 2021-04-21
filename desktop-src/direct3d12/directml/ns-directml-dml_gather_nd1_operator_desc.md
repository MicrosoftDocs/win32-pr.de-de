---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Erfasst Elemente aus dem Eingabetensor und verwendet dabei den Indizestensor, um Indizes vollständigen Teilblöcken der Eingabe neu zuordnen. | DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: b92c8aece88d8466357bb8e48fd3ce5a3b73d2e3
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802859"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a>DML_GATHER_ND1_OPERATOR_DESC -Struktur (directml.h)

Erfasst Elemente aus dem Eingabetensor und verwendet den Indizestensor, um Indizes vollständigen Teilblöcken der Eingabe neu zuordnen. Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten dar, deren genaues Verhalten von der Anzahl der Batch-, Eingabe- und Indizesdimensionen abhängig ist.

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, aus dem gelesen werden soll.

`IndicesTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, der die Indizes enthält. DimensionCount *dieses* Tensors muss mit *InputTensor.DimensionCount übereinstimmen.* Die letzte Dimension des *IndicesTensor* ist tatsächlich die Anzahl der Koordinaten pro Index-Tupel und darf *InputTensor.DimensionCount nicht überschreiten.* Beispielsweise bedeutet ein *Indizestensor* von Größen mit `{1,4,5,2}` *IndicesDimensionCount* = 3 ein 4x5-Array von Zweikoordinaten-Tupeln, die in *InputTensor* indiziert werden.

Ab unterstützt dieser Operator negative Indexwerte, wenn ein integraler Typ mit `DML_FEATURE_LEVEL_3_0` Vorsignierung mit diesem Tensor verwendet wird. Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert. Ein Index von -1 bezieht sich beispielsweise auf das letzte Element in dieser Dimension.

`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, in den die Ergebnisse geschrieben werden. *DimensionCount und* *DataType dieses* Tensors müssen mit *InputTensor.DimensionCount übereinstimmen.* Die *erwarteten OutputTensor.Sizes* sind die Verkettung der führenden *IndizesTensor.Sizes* und des nachgestellten Segments *InputTensor.Sizes,* was Folgendes ergibt.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

Die Dimensionen sind rechtsbündig ausgerichtet, wobei bei Bedarf führende 1 Werte voranstellen, um *OutputTensor.DimensionCount* zu erfüllen.

Hier sehen Sie ein Beispiel.

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```

`InputDimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der tatsächlichen Eingabedimensionen innerhalb des *InputTensor,* nachdem irrelevante führende Dimensionen ignoriert wurden, die im Bereich von `[1, *InputTensor.DimensionCount*]` sind. Wenn beispielsweise *InputTensor.Sizes* und = 3 angegeben  =  `{1,1,4,6}` `InputDimensionCount` sind, sind die tatsächlichen aussagekräftigen Indizes `{1,4,6}` .

`IndicesDimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der tatsächlichen Indexdimensionen innerhalb des *Indextensors* nach dem Ignorieren irrelevanter führender Dimensionen im Bereich [1, *IndizesTensor.DimensionCount*]. Bei *IndizesTensor.Sizes*  =  `{1,1,4,6}` und *IndizesDimensionCount* = 3 sind die tatsächlichen aussagekräftigen Indizes beispielsweise `{1,4,6}` .

`BatchDimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Dimensionen innerhalb jedes Tensors (*InputTensor*, *IndicesTensor*, *OutputTensor*), die als unabhängige Batches betrachtet werden und sowohl innerhalb von [0, *InputTensor.DimensionCount*) als auch [0, *IndicesTensor.DimensionCount*) liegen. Die Batchanzahl kann 0 sein, was einen einzelnen Batch impliziert. Bei *IndizesTensor.Sizes*  =  `{1,3,4,5,6,7}` und *IndizesDimensionCount* = 5 und = 2 gibt es beispielsweise `BatchDimensionCount` Batches und aussagekräftige `{3,4}` `{5,6,7}` Indizes.

## <a name="remarks"></a>Hinweise
**DML_GATHER_ND1_OPERATOR_DESC** fügt *BatchDimensionCount* hinzu und entspricht [DML_GATHER_ND_OPERATOR_DESC,](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) wenn *BatchDimensionCount* = 0 ist.

## <a name="examples"></a>Beispiele

### <a name="example-1-1d-remapping"></a>Beispiel 1: 1D-Neuzuordnung

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a>Beispiel 2: 2D-Neuzuordnung mit Batchanzahl

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
* *IndicesTensor,* *InputTensor* und *OutputTensor* müssen über den gleichen *DimensionCount verfügen.*
* *InputTensor* und *OutputTensor* müssen den gleichen *Datentyp aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Eingabe | 1 bis 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |
