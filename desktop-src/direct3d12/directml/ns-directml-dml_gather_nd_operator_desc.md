---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Sammelt Elemente aus dem Eingabe Mandanten, wobei der Indexe-tensorflow verwendet wird, um Indizes den gesamten Teil Blöcken der Eingabe zuzuordnen. | DML_GATHER_ND_OPERATOR_DESC
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
ms.openlocfilehash: 6a48fd19621bed100a13412dbb1992974d125323
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354333"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a>DML_GATHER_ND_OPERATOR_DESC-Struktur (directml. h)

Sammelt Elemente aus dem Eingabe Mandanten, wobei der Indexe-tensorflow verwendet wird, um Indizes den gesamten Teil Blöcken der Eingabe zuzuordnen. Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten dar, wobei das genaue Verhalten von der Eingabe-und Index Dimensions Anzahl abhängig ist.

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der zu lesende tensorflow.


`IndicesTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der tensorflow, der die Indizes enthält. Die *DimensionCount* dieses Mandanten muss mit " *inputtensor. DimensionCount*" verglichen werden. Die letzte Dimension von " *indicestensor* " ist tatsächlich die Anzahl der Koordinaten pro indextupel, die " *inputtensor. DimensionCount*" nicht überschreiten darf. Ein indexertensor der *Größen* `{1,4,5,2}` mit *indicesdimensioncount* = 3 bedeutet beispielsweise ein 4x5-Array von 2-Koordinaten-Tupeln, die in *inputtensor* indiziert werden.

Ab `DML_FEATURE_LEVEL_3_0` unterstützt dieser Operator negative Indexwerte, wenn ein ganzzahliger Typ mit Vorzeichen mit diesem Mandanten verwendet wird. Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert. Ein Index von-1 bezieht sich z. b. auf das letzte Element in dieser Dimension.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der tensorflow, in den die Ergebnisse geschrieben werden sollen. Die *DimensionCount* -und *DataType* -Elemente dieses Mandanten müssen mit " *inputtensor. DimensionCount*" verglichen werden. Der erwartete *outputtensor. sizes* -Parameter ist die Verkettung der " *indicestensor. sizes* "-Segmente und " *inputtensor. sizes* ", die das nachfolgende Segment ergibt:

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

Die Ausgabe Dimensionen werden rechtsbündig ausgerichtet, wobei bei Bedarf vorangehende 1-Werte vorangestellt werden, um bis zu *outputtensor. DimensionCount* zu erfüllen.

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

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der tatsächlichen Eingabe Dimensionen innerhalb von *inputtensor* , nachdem alle irreführenden, führenden Werte ignoriert wurden `[1, *InputTensor.DimensionCount*]` . Wenn beispielsweise " *inputtensor. sizes* " und "= 3" angegeben sind  =  `{1,1,4,6}` `InputDimensionCount` , sind die tatsächlichen aussagekräftigen Indizes `{1,4,6}` .


`IndicesDimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der tatsächlichen Index Dimensionen innerhalb von " *indicestensor* ", nachdem alle nicht relevanten führenden Werte im Bereich von [1, " *indicestensor. DimensionCount*") ignoriert wurden. Wenn beispielsweise " *indicestensor. sizes*"  =  `{1,1,4,6}` und " *indicesdimensioncount* = 3" angegeben sind, sind die tatsächlichen aussagekräftigen Indizes `{1,4,6}` .

## <a name="examples"></a>Beispiele

### <a name="example-1-1d-remapping"></a>Beispiel 1: Neuzuordnung von 1 d

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

### <a name="example-2-2d-remapping"></a>Beispiel 2: 2D-Neuzuordnung

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


## <a name="remarks"></a>Bemerkungen
Eine neuere Version dieses Operators, `DML_OPERATOR_GATHER_ND1` , wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* " *Indicestensor*", " *inputtensor*" und " *outputtensor* " müssen dieselbe *DimensionCount* aufweisen.
* *Inputtensor* und *outputtensor* müssen denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Indikator Geber | Eingabe | 1 bis 8 | Int64, Int32, UINT64, UInt32 |
| Outputtensor | Ausgabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Indikator Geber | Eingabe | 4 | UINT32 |
| Outputtensor | Ausgabe | 4 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |
