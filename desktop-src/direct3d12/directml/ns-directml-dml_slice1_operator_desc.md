---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Extrahiert einen einzelnen Unterbereich (einen "Slice") eines Eingabe Mandanten.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: 06721a7484426eb293494156a2ec23db6fbf0a6b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106353244"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a>DML_SLICE1_OPERATOR_DESC-Struktur (directml. h)
Extrahiert einen einzelnen Unterbereich (einen "Slice") eines Eingabe Mandanten.

Das *Eingabefenster* beschreibt die Begrenzungen des Eingabe Mandanten, der im Slice berücksichtigt werden soll. Das Fenster wird mit drei Werten für jede Dimension definiert.

- Der *Offset* markiert den *Anfang des Fensters* in einer Dimension.
- Die *Größe* markiert den Umfang des Fensters in einer Dimension. Das *Ende des Fensters* in einer Dimension ist `offset + size - 1` .
- Der *Stride-Schritt* gibt an, wie die Elemente in einer Dimension durchlaufen werden.
  - Die Größe des Schritts gibt an, wie viele Elemente beim Kopieren innerhalb des Fensters zu tun sind.
  - Wenn ein Schritt positiv ist, werden Elemente beginnend am *Anfang* des Fensters in der Dimension kopiert.
  - Wenn ein Stride-Wert negativ ist, werden Elemente beginnend am *Ende* des Fensters in der Dimension kopiert.

Der folgende Pseudo Code veranschaulicht, wie Elemente mithilfe des Eingabe Fensters kopiert werden. Beachten Sie, wie Elemente in einer Dimension von Anfang bis Ende mit einem positiven Stride kopiert und von End auf Start mit einem negativen Stride kopiert werden.

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

Das Eingabefenster darf in keiner Dimension leer sein, und das Fenster darf nicht über die Abmessungen des Eingabe Mandanten hinaus erweitert werden (Lesevorgänge außerhalb des gültigen Bereichs sind nicht zulässig). Durch die Größe und den Fortschritten des Fensters wird die Anzahl der Elemente, die aus jeder Dimension des Eingabe Mandanten kopiert werden können, effektiv eingeschränkt `i` .

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

Der ausgabetensor ist nicht erforderlich, um alle erreichbaren Elemente innerhalb des Fensters zu kopieren. Der Slice ist gültig, solange `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a>Member

`InputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der tensorflow, aus dem Slices extrahiert werden.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der tensorflow, in den die in Slices aufgeschnittenen Daten geschrieben werden sollen.


`DimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Dimensionen. Dieses Feld bestimmt die Größe der Arrays *inputwindowoffsets*, *inputwindowsizes* und *inputwindowclaims* . Dieser Wert muss mit der *DimensionCount* der Eingabe-und Ausgabe Tensoren identisch sein. Dieser Wert muss zwischen 1 und 8 liegen, beginnend ab `DML_FEATURE_LEVEL_3_0` ; für frühere featureebenen ist entweder der Wert 4 oder 5 erforderlich.


`InputWindowOffsets`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Ein Array, das den Anfang (in-Elementen) des Eingabe Fensters in jeder Dimension enthält. Werte im Array müssen die Einschränkung erfüllen. `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowSizes`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Ein Array, das den Wertebereich (in-Elementen) des Eingabe Fensters in jeder Dimension enthält. Werte im Array müssen die Einschränkung erfüllen. `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowStrides`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Ein Array, das den Slice entlang der einzelnen Dimensionen des Eingabe-Tensors in-Elementen enthält. Die Größe des STRIDE gibt an, wie viele Elemente beim Kopieren innerhalb des Eingabe Fensters fortzufahren sind. Das Vorzeichen des STRIDE bestimmt, ob Elemente beginnend am Anfang des Fensters (positiver stride) oder am Ende des Fensters (negativer stride) kopiert werden. Die Schritte dürfen nicht 0 sein.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird derselbe Eingabe Mandanten verwendet.

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a>Beispiel 1: Strichstrichs mit positiven Schritten

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

Die kopierten Elemente werden wie folgt berechnet. 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a>Beispiel 2: Stricing Slice mit negativen Schritten

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

Denken Sie daran, dass Dimensionen mit negativen Fenster Schritten am Ende des Eingabe Fensters für diese Dimension kopiert werden. Dies erfolgt durch Hinzufügen `InputWindowSize[i] - 1` zum Fenster Offset. Dimensionen mit einem positiven Stride beginnen einfach bei `InputWindowOffset[i]` .
- Achse 0 ( `+1` Fenster stride) beginnt mit dem Kopieren von `InputWindowOffsets[0] = 0` . 
- Achse 1 ( `+1` Fenster stride) beginnt mit dem Kopieren von `InputWindowOffsets[1] = 0` . 
- Achse 2 ( `-2` Fenster stride) beginnt mit dem Kopieren von `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` . 
- Achse 3 ( `+2` Fenster stride) beginnt mit dem Kopieren von `InputWindowOffsets[3] = 1` . 

Die kopierten Elemente werden wie folgt berechnet. 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a>Bemerkungen
Dieser Operator ähnelt [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), aber er unterscheidet sich in zwei wichtigen Punkten.

- Slice-Schritte können negativ sein, was das Umkehren von Werten entlang Dimensionen ermöglicht.
- Die Eingabefenster Größen sind nicht notwendigerweise identisch mit den Ausgabe-tensorflow-Größen.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*Inputtensor* und *outputtensor* müssen über denselben *Datentyp* und *DimensionCount* verfügen.

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Outputtensor | Ausgabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 bis 5 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Outputtensor | Ausgabe | 4 bis 5 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |