---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Extrahiert einen einzelnen Unterbereich (einen "Slice") eines Eingabetensors.
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
ms.openlocfilehash: f34525865be9541da879e66e88c29d4a2ab74f00
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803954"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a>DML_SLICE1_OPERATOR_DESC -Struktur (directml.h)
Extrahiert einen einzelnen Unterbereich (einen "Slice") eines Eingabetensors.

Das *Eingabefenster* beschreibt die Begrenzungen des Eingabetensors, die im Slice zu berücksichtigen sind. Das Fenster wird mit drei Werten für jede Dimension definiert.

- Der *Offset* markiert den *Anfang des Fensters* in einer Dimension.
- Die *Größe* markiert den Bereich des Fensters in einer Dimension. Das *Ende des Fensters* in einer Dimension ist `offset + size - 1` .
- Der *-Schritt gibt* an, wie die Elemente in einer Dimension durchlaufen werden.
  - Die Größe des Schritts gibt an, wie viele Elemente beim Kopieren innerhalb des Fensters voranschritten werden.
  - Wenn ein Schritt positiv ist, werden Elemente beginnend am Anfang *des* Fensters in der Dimension kopiert.
  - Wenn ein Schritt negativ ist, werden Elemente beginnend am *Ende* des Fensters in der Dimension kopiert.

Der folgende Pseudocode veranschaulicht, wie Elemente mithilfe des Eingabefensters kopiert werden. Beachten Sie, wie Elemente in einer Dimension von Anfang bis Ende mit einem positiven Schritt kopiert und von Ende kopiert werden, um mit einem negativen Schritt zu beginnen.

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

Das Eingabefenster darf in einer Dimension nicht leer sein, und das Fenster darf nicht über die Dimensionen des Eingabetensors hinausgehen (lesegefängte Außerhalbgrenzen sind nicht zulässig). Die Fenstergröße und -strides begrenzen effektiv die Anzahl der Elemente, die aus jeder Dimension des `i` Eingabetensors kopiert werden können.

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

Der Ausgabe-Tensor ist nicht erforderlich, um alle erreichbaren Elemente innerhalb des Fensters zu kopieren. Der Slice ist gültig, solange `1 <= OutputSizes[i] <= MaxCopiedElements[i]` er ist.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

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

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, aus dem Slices extrahiert werden sollen.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, in den die Datenergebnisse in Slices geschrieben werden sollen.


`DimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Dimensionen. Dieses Feld bestimmt die Größe der *Arrays InputWindowOffsets,* *InputWindowSizes* und *InputWindowStrides.* Dieser Wert muss mit dem *DimensionCount-Wert* der Eingabe- und Ausgabe tensors übereinstimmen. Dieser Wert muss zwischen 1 und 8 liegen, einschließlich ab `DML_FEATURE_LEVEL_3_0` . Frühere Featureebenen erfordern einen Wert von 4 oder 5.


`InputWindowOffsets`

Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Ein Array, das den Anfang (in Elementen) des Eingabefensters in jeder Dimension enthält. Werte im Array müssen die Einschränkung erfüllen. `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowSizes`

Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Ein Array, das den Umfang (in Elementen) des Eingabefensters in jeder Dimension enthält. Werte im Array müssen die Einschränkung erfüllen. `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowStrides`

Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Ein Array, das den Schritt des Slices entlang jeder Dimension des Eingabe-Tensors in -Elementen enthält. Die Größe des Schritts gibt an, wie viele Elemente beim Kopieren innerhalb des Eingabefensters vorankommen sollen. Das Vorzeichen des Schritts bestimmt, ob Elemente beginnend am Anfang des Fensters (positiver Schritt) oder am Ende des Fensters (negativer Schritt) kopiert werden. Strides darf nicht 0 sein.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird der gleiche Eingabetensor verwendet.

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a>Beispiel 1: Strided slice with positive strides (Strided Slice mit positiven Schritten)

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

### <a name="example-2-strided-slice-with-negative-strides"></a>Beispiel 2: Strided slice with negative strides (Strided Slice mit negativen Schritten)

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

Denken Sie daran, dass Dimensionen mit negativen Fensterschritten am Ende des Eingabefensters für diese Dimension mit dem Kopieren beginnen. Dies erfolgt durch Hinzufügen `InputWindowSize[i] - 1` zum Fensteroffset. Dimensionen mit einem positiven Schritt beginnen einfach bei `InputWindowOffset[i]` .
- Achse 0 `+1` (Fensterschritt) beginnt mit dem Kopieren unter `InputWindowOffsets[0] = 0` . 
- Achse 1 `+1` (Fensterschritt) beginnt mit dem Kopieren unter `InputWindowOffsets[1] = 0` . 
- Achse 2 `-2` (Fensterschritt) beginnt mit dem Kopieren unter `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` . 
- Achse 3 ( `+2` Fensterschritt) beginnt mit dem Kopieren unter `InputWindowOffsets[3] = 1` . 

Die kopierten Elemente werden wie folgt berechnet. 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a>Hinweise
Dieser Operator ähnelt [der](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc)DML_SLICE_OPERATOR_DESC , unterscheidet sich jedoch auf zwei wichtige Arten.

- Slice-Strides können negativ sein, was das Umkehren von Werten entlang von Dimensionen ermöglicht.
- Die Größen des Eingabefensters sind nicht notwendigerweise mit den Ausgabe tensor-Größen identisch.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*InputTensor und* *OutputTensor* müssen denselben *DataType und* *DimensionCount aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 bis 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Ausgabe | 4 bis 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |