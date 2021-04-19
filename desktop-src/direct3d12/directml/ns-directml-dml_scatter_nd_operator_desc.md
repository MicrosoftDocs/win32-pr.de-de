---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Kopiert den gesamten Eingabe Mandanten in die Ausgabe und überschreibt dann ausgewählte Indizes mit entsprechenden Werten aus dem Aktualisierungs Mandanten.
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
ms.openlocfilehash: ae9a3022a7070bbf0253e71550f2ca1ceced6768
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351831"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a>DML_SCATTER_ND_OPERATOR_DESC-Struktur (directml. h)
Kopiert den gesamten Eingabe Mandanten in die Ausgabe und überschreibt dann ausgewählte Indizes mit entsprechenden Werten aus dem Aktualisierungs Mandanten. Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten mit dem exakten Verhalten dar, das durch die Größe der Achse und der Indizes bestimmt wird.

```
output = input
output[indices[...]] = updates[...]
```

Wenn sich zwei Ausgabe Element Indizes überlappen (was ungültig ist), gibt es keine Garantie dafür, welcher letzte Schreibvorgang gewinnt.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der zu lesende tensorflow.


`IndicesTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Indizes enthält. Die *DimensionCount* dieses Mandanten muss mit " *inputtensor. DimensionCount*" verglichen werden. Die letzte Dimension von " *indicestensor* " ist tatsächlich die Anzahl der Koordinaten pro indextupel, die " *inputtensor. DimensionCount*" nicht überschreiten darf. Beispielsweise `{1,4,5,2}` bedeutet ein indextensor der Größe mit *indicesdimensioncount* = 3 ein 4x5-Array von 2-Wert-Koordinaten Tupeln, die in *inputtensor* indiziert werden.

Ab `DML_FEATURE_LEVEL_3_0` unterstützt dieser Operator negative Indexwerte, wenn ein ganzzahliger Typ mit Vorzeichen mit diesem Mandanten verwendet wird. Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert. Ein Index von-1 bezieht sich z. b. auf das letzte Element in dieser Dimension.


`UpdatesTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow mit den neuen Werten, mit denen die vorhandenen Eingabewerte in den entsprechenden Indizes ersetzt werden. Die *DimensionCount* dieses Mandanten muss mit " *inputtensor. DimensionCount*" verglichen werden. Die erwarteten *updatestensor. sizes* sind die Verkettung der führenden Segmente " *indicestensor. sizes* " und " *inputtensor. sizes* ", um Folgendes zu erzielen.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

Die Dimensionen sind rechtsbündig ausgerichtet, wobei bei Bedarf vorangehende 1-Werte vorangestellt werden, um *updatestensor. DimensionCount* zu erfüllen.

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der tensorflow, in den die Ergebnisse geschrieben werden sollen. Die *Größen* und der *Datentyp* dieses Mandanten müssen mit " *inputtensor. sizes*" verglichen werden.


`InputDimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der tatsächlichen Eingabe Dimensionen innerhalb von *inputtensor* , nachdem alle irreführenden, führenden Werte mit [1, *inputtensor. DimensionCount*) ignoriert wurden. Wenn z. b *. "inputtensor. sizes* =" {1,1,4,6} und " *inputdimensioncount* = 3" angegeben sind, sind die tatsächlichen aussagekräftigen Indizes {1,4,6} .


`IndicesDimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der tatsächlichen Index Dimensionen innerhalb des *bezeichungsgebers* , nachdem alle irreführenden, führenden Werte mit [1, *indicestensor. DimensionCount*) ignoriert wurden. Wenn beispielsweise " *indicestensor. sizes* =" {1,1,4,6} und " *indicesdimensioncount* = 3" angegeben sind, sind die tatsächlichen aussagekräftigen Indizes {1,4,6} .

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
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* " *Indicestensor*", " *inputtensor*", " *outputtensor*" und "" `UpdatesTensor` müssen dieselbe *DimensionCount* aufweisen.
* " *Inputtensor*", " *outputtensor*" und "" `UpdatesTensor` müssen denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Indikator Geber | Eingabe | 1 bis 8 | Int64, Int32, UINT64, UInt32 |
| Updatestensor | Eingabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Outputtensor | Ausgabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Indikator Geber | Eingabe | 4 | UINT32 |
| Updatestensor | Eingabe | 4 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Outputtensor | Ausgabe | 4 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |