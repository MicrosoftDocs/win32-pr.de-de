---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Erfasst Elemente aus dem Eingabetensor und verwendet den Indizestensor, um Indizes vollständigen Teilblöcken der Eingabe neu zuordnen. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 8e74078eaf55f209fba92ba97737d22047a5e67c
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417606"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a>DML_GATHER_ND_OPERATOR_DESC -Struktur (directml.h)

Erfasst Elemente aus dem Eingabetensor und verwendet den Indizestensor, um Indizes vollständigen Teilblöcken der Eingabe neu zuordnen. Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten dar, deren genaues Verhalten von der Anzahl der Eingabe- und Indizesdimensionen abhängig ist.

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
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

Der Tensor, der die Indizes enthält. DimensionCount *dieses* Tensors muss mit *InputTensor.DimensionCount übereinstimmen.* Die letzte Dimension des *IndicesTensor* ist tatsächlich die Anzahl der Koordinaten pro Index-Tupel und darf *InputTensor.DimensionCount nicht überschreiten.* Beispielsweise bedeutet ein Indizes-Tensor von *Größen* mit `{1,4,5,2}` *IndicesDimensionCount* = 3 ein 4x5-Array von 2-Koordinaten-Tupeln, die in *InputTensor* indiziert werden.

Ab unterstützt dieser Operator negative Indexwerte, wenn ein integraler Typ mit `DML_FEATURE_LEVEL_3_0` Vorsignierung mit diesem Tensor verwendet wird. Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert. Beispielsweise bezieht sich ein Index von -1 auf das letzte Element in dieser Dimension.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, in den die Ergebnisse geschrieben werden. *DimensionCount und* *DataType dieses* Tensors müssen mit *InputTensor.DimensionCount übereinstimmen.* Die erwarteten *OutputTensor.Sizes* sind die Verkettung der führenden Segmente *IndicesTensor.Sizes* und *InputTensor.Sizes,* um die Ergebnisse zu erzielen:

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

Die Ausgabedimensionen sind rechtsbündig ausgerichtet, und führenden 1 Werten wird bei Bedarf vorgefertigt, um *OutputTensor.DimensionCount zu erfüllen.*

Hier ist ein Beispiel.

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

Die Anzahl der tatsächlichen Eingabedimensionen innerhalb des *InputTensor,* nachdem alle irrelevanten führenden Dimensionen mit dem Bereich ignoriert `[1, *InputTensor.DimensionCount*]` wurden. Wenn beispielsweise *InputTensor.Sizes* und = 3 angegeben werden, sind die  =  `{1,1,4,6}` `InputDimensionCount` tatsächlichen sinnvollen Indizes `{1,4,6}` .


`IndicesDimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der tatsächlichen Indexdimensionen innerhalb des *IndizesTensors,* nachdem irrelevante führende Dimensionen ignoriert wurden, die [1, *IndicesTensor.DimensionCount] reichen.* Wenn beispielsweise *IndicesTensor.Sizes und*  =  `{1,1,4,6}` *IndicesDimensionCount* = 3 angegeben werden, sind die tatsächlichen sinnvollen Indizes `{1,4,6}` .

## <a name="examples"></a>Beispiele

### <a name="example-1-1d-remapping"></a>Beispiel 1: 1D-Neuappapping

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a>Beispiel 2: 2D-Neuappapping

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a>Hinweise
Eine neuere Version dieses Operators, `DML_OPERATOR_GATHER_ND1` , wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *IndicesTensor,* *InputTensor* und *OutputTensor* müssen denselben *DimensionCount aufweisen.*
* *InputTensor und* *OutputTensor* müssen denselben *Datentyp haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Eingabe | 1 bis 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Eingabe | 4 | UINT32 |
| OutputTensor | Ausgabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |
