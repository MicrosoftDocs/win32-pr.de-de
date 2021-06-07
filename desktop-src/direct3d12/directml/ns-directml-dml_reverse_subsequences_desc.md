---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Kehrt die Elemente einer oder mehrere *Teilsequenten eines* Tensors um. Der Satz von Teilsequenzen, die umgekehrt werden sollen, wird basierend auf der angegebenen Achse und Sequenzlänge ausgewählt.
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 3deddea3d60db1a8689ceabfac92ff17393b7606
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417224"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a>DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC -Struktur (directml.h)
Kehrt die Elemente einer oder mehrere *Teilsequenten eines* Tensors um. Der Satz von Teilsequenzen, die umgekehrt werden sollen, wird basierend auf der angegebenen Achse und Sequenzlänge ausgewählt.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Eingabetensor, der elemente enthält, die umgekehrt werden sollen.


`SequenceLengthsTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der einen Wert für jede zu umkehrende Unterzeichenfolge enthält, der die Länge in Elementen dieser Untersequence anklangt. Nur die Elemente innerhalb der Länge der Teilsequence werden umgekehrt. Die verbleibenden Elemente entlang dieser Achse werden unverändert in die Ausgabe kopiert.

Dieser Tensor muss dimensionsanzahl und -größen aufweisen, die dem *InputTensor* *entspricht,* mit Ausnahme der dimension, die durch den *Axis-Parameter angegeben* wird. Die Größe der *Achsendimension* muss 1 sein. Wenn der *InputTensor* z. B. die Größen hat und Die Achse 1 ist, müssen die Größen von `{2,3,4,5}` *SequenceLengthsTensor*  `{2,1,4,5}` sein.

Wenn die Länge einer Teilsequence die maximale Anzahl von Elementen entlang dieser Achse überschreitet, verhält sich dieser Operator so, als ob der Wert an das Maximum angeklammert wäre.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe tensor, in den die Ergebnisse geschrieben werden. Dieser Tensor muss die gleichen Größen und Datentypen wie *inputTensor haben.*


`Axis`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Der Index der Dimension, um die Elemente umgekehrt werden. Dieser Wert muss kleiner als dimensionCount des *InputTensor sein.*

## <a name="examples"></a>Beispiele

### <a name="example-1"></a>Beispiel 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a>Beispiel 2: Umkehren entlang einer anderen Achse

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *InputTensor,* *OutputTensor* und *SequenceLengthsTensor* müssen denselben *DimensionCount aufweisen.*
* *InputTensor und* *OutputTensor* müssen denselben *Datentyp haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 bis 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| SequenceLengthsTensor | Eingabe | 4 bis 5 | UINT32 |
| OutputTensor | Ausgabe | 4 bis 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| SequenceLengthsTensor | Eingabe | 4 | UINT32 |
| OutputTensor | Ausgabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |