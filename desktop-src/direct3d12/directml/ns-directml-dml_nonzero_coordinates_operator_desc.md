---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Berechnet die N-dimensionalen Koordinaten aller Nicht-Null-Elemente des Eingabetensors.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: 39463ba57bc90b35d5ac5dc7fc43993169137221
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417236"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a>DML_NONZERO_COORDINATES_OPERATOR_DESC -Struktur (directml.h)

Berechnet die N-dimensionalen Koordinaten aller Nicht-Null-Elemente des Eingabetensors.

Dieser Operator erzeugt eine MxN-Matrix von Werten, wobei jede Zeile M eine N-dimensionale Koordinate eines Werts enthält, der nicht 0 (null) aus der Eingabe ist. Bei Verwendung **von FLOAT32-** oder **FLOAT16-Eingaben** werden sowohl negative als auch positive 0 (0,0f und -0,0f) im Rahmen dieses Operators als 0 (null) behandelt.

Der -Operator erfordert, dass *der OutputCoordinatesTensor* groß genug ist, um ein ungünstigstes Szenario zu bieten, bei dem jedes Element der Eingabe nicht 0 (null) ist. Dieser Operator gibt die Anzahl der Elemente, die nicht null sind, über den *OutputCountTensor* zurück, den Aufrufer überprüfen können, um die Anzahl der Koordinaten zu bestimmen, die in den *OutputCoordinatesTensor* geschrieben werden.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Eingabe tensor.

`OutputCountTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe-Tensor, der die Anzahl von Elementen enthält, die nicht 0 (null) im Eingabetensor sind. This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1. Der Typ dieses Tensors muss **UINT32 sein.**

`OutputCoordinatesTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe-Tensor, der die n-dimensionalen Koordinaten der Eingabeelemente enthält, die nicht 0 (null) sind. 

Dieser Tensor  muss größen von `{1,1,M,N}` (wenn *DimensionCount* gleich 4 ist) oder `{1,1,1,M,N}` (wenn *DimensionCount* 5  ist), wobei M die Gesamtzahl der Elemente im *InputTensor* und N größer oder gleich dem effektiven Rang von *InputTensor* bis zum *DimensionCount-Wert* der Eingabe ist.

Der effektive Rang eines Tensors wird durch *DimensionCount* dieses Tensors ohne führende Dimensionen der Größe 1 bestimmt. Beispielsweise hat ein Tensor mit größen von den effektiven Rang 3, ebenso wie ein `{1,2,3,4}` Tensor mit größen von `{1,1,5,5,5}` . Ein Tensor mit Größen hat `{1,1,1,1}` den effektiven Rang 0.

Stellen Sie sich *einen InputTensor mit* *größen von* `{1,1,12,5}` vor. Dieser Eingabetensor enthält 60 Elemente und hat einen effektiven Rang von 2. In diesem Beispiel haben alle gültigen Größen von *OutputCoordinatesTensor* das Format , wobei N >= 2, aber nicht größer als `{1,1,60,N}` *DimensionCount* (in diesem Beispiel 4) ist.

Die in diesen Tensor geschriebenen Koordinaten werden garantiert nach dem aufsteigenden Elementindex geordnet. Wenn der Eingabetensor z. B. drei Werte an den Koordinaten , und hat, sind die werte, die in {1,0} {1,2} den {0,5} *OutputCoordinatesTensor* geschrieben werden, `[[0,5], [1,0], [1,2]]` .

Während für diesen Tensor die Dimension M der Anzahl der Elemente im Eingabetensor entspricht, schreibt dieser Operator nur maximal OutputCount-Elemente in diesen Tensor. OutputCount wird über den skalaren *OutputCountTensor zurückgegeben.*

> [!NOTE]
> Die verbleibenden Elemente dieses Tensors außerhalb von OutputCount sind nach Abschluss dieses Operators nicht definiert. Sie sollten sich nicht auf die Werte dieser Elemente verlassen.

## <a name="example"></a>Beispiel

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*InputTensor*, *OutputCoordinatesTensor* und müssen `OutputCountTensor` denselben *DimensionCount aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Dimensionen | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Eingabe | { [D0], D1, D2, D3, D4 } | 4 bis 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputCountTensor | Ausgabe | { [1], 1, 1, 1, 1 } | 4 bis 5 | UINT32 |
| OutputCoordinatesTensor | Ausgabe | { [1], 1, 1, M, N } | 4 bis 5 | UINT32 |

## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |