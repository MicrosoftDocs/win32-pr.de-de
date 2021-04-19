---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Kehrt die Elemente einer *oder mehrerer unter* Sequenzen eines Tensors um. Der Satz von unter Sequenzen, der umgekehrt werden soll, wird basierend auf der angegebenen Achse und den angegebenen Sequenz Längen ausgewählt.
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
ms.openlocfilehash: 5baf16c5acd1ce5c5f44e68420e93aabaa276ea7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106366541"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a>DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC-Struktur (directml. h)
Kehrt die Elemente einer *oder mehrerer unter* Sequenzen eines Tensors um. Der Satz von unter Sequenzen, der umgekehrt werden soll, wird basierend auf der angegebenen Achse und den angegebenen Sequenz Längen ausgewählt.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingabetensor mit Elementen, die umgekehrt werden sollen.


`SequenceLengthsTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der einen Wert für jede unter Sequenz enthält, die umgekehrt werden soll, wobei die Länge in Elementen dieser unter Sequenz angegeben wird. Nur die Elemente innerhalb der Länge der unter Sequenz werden umgekehrt. die übrigen Elemente auf dieser Achse werden unverändert in die Ausgabe kopiert.

Dieser Mandanten muss die Anzahl und die Größe der Dimensionen gleich dem *inputtensor* aufweisen, *außer* der durch den Parameter *Axis* angegebenen Dimension. Die Größe der *Achsen* Dimension muss 1 sein. Wenn z. b. die Größe von *inputtensor* `{2,3,4,5}` und die *Achse* 1 beträgt, muss die Größe von " *sequencelengthstensor* " lauten `{2,1,4,5}` .

Wenn die Länge einer unter Sequenz die maximale Anzahl von Elementen auf dieser Achse überschreitet, verhält sich dieser Operator so, als ob der Wert an den maximalen Wert gebunden wäre.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen. Dieser Mandanten muss dieselbe Größe und denselben Datentyp aufweisen wie der *inputtensor*.


`Axis`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Der Index der Dimension, über die Elemente umgekehrt werden sollen. Dieser Wert muss kleiner als die DimensionCount von " *inputtensor*" sein.

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

### <a name="example-2-reversing-along-a-different-axis"></a>Beispiel 2: Umkehren an einer anderen Achse

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
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* " *Inputtensor*", " *outputtensor*" und " *sequencelengthstensor* " müssen dieselbe *DimensionCount* aufweisen.
* *Inputtensor* und *outputtensor* müssen denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 bis 5 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Sequencelengthstensor | Eingabe | 4 bis 5 | UINT32 |
| Outputtensor | Ausgabe | 4 bis 5 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Sequencelengthstensor | Eingabe | 4 | UINT32 |
| Outputtensor | Ausgabe | 4 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |