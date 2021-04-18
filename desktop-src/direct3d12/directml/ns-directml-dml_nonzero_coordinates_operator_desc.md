---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Berechnet die N-dimensionalen Koordinaten aller Elemente ungleich 0 (null) des eingabetensors.
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
ms.openlocfilehash: a662ac3b341c07e512e11dcc15cbc9b11ec5f405
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106354896"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a>DML_NONZERO_COORDINATES_OPERATOR_DESC-Struktur (directml. h)

Berechnet die N-dimensionalen Koordinaten aller Elemente ungleich 0 (null) des eingabetensors.

Dieser Operator erzeugt eine MXN-Matrix mit Werten, wobei jede Zeile M eine N-dimensionale Koordinate eines Werts ungleich 0 (null) aus der Eingabe enthält. Bei Verwendung von **float32** -oder **FLOAT16** -Eingaben werden sowohl negative als auch positive 0 (0,0 f und-0,0 f) für die Zwecke dieses Operators als 0 (null) behandelt.

Der Operator erfordert, dass der *outputcoordinatestensor* eine Größe hat, die groß genug ist, um einem Worst-Case-Szenario Rechnung zu tragen, bei dem jedes Element der Eingabe ungleich 0 (null) ist. Dieser Operator gibt die Anzahl von Elementen ungleich 0 (null) über den *outputzählensor* zurück, die Aufrufer überprüfen können, um die Anzahl der Koordinaten zu ermitteln, die in *outputcoordinatestensor* geschrieben werden.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein eingabetensor.

`OutputCountTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe Mandanten, der die Anzahl der Elemente ungleich 0 (null) im Eingabe Mandanten enthält. Dieser Mandanten muss ein Skalar sein, d &mdash; . h. die Größe dieses Mandanten muss 1 sein. Der Typ dieses Mandanten muss **UInt32** lauten.

`OutputCoordinatesTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe-tensorflow, der die N-dimensionalen Koordinaten der Eingabeelemente enthält, die ungleich 0 (null) sind. 

Dieser tensorflow muss über *Größen* von `{1,1,M,N}` verfügen ( *Wenn DimensionCount* gleich 4 ist), oder `{1,1,1,M,N}` (wenn *DimensionCount* gleich 5 ist), wobei M die Gesamtzahl der Elemente in *inputtensor* ist, und N größer oder gleich dem *effektiven Rang* von *inputtensor* ist, bis zur *DimensionCount* der Eingabe.

Der effektive Rang eines Mandanten wird durch die *DimensionCount* dieses Mandanten mit Ausnahme der führenden Dimensionen der Größe 1 festgelegt. Ein tensorflow mit Größen von hat beispielsweise `{1,2,3,4}` einen effektiven Rang 3, ebenso wie ein tensorflow mit den Größen von `{1,1,5,5,5}` . Ein tensorflow mit Größen `{1,1,1,1}` hat den gültigen Rang 0.

Stellen Sie sich einen *inputtensor* mit *Größen* von vor `{1,1,12,5}` . Dieser eingabetensor enthält 60 Elemente und hat einen effektiven Rang von 2. In diesem Beispiel weisen alle gültigen Größen von *outputcoordinatestensor* das Format auf `{1,1,60,N}` , wobei N >= 2, aber nicht größer als die *DimensionCount* (in diesem Beispiel 4) ist.

Die in diesen Mandanten geschriebenen Koordinaten werden garantiert nach dem aufsteigenden Element Index sortiert. Wenn der Eingabe-tensorflow z. b. drei Werte ungleich NULL bei den Koordinaten {1,0} , {1,2} und enthält {0,5} , werden die Werte, die in den *outputcoordinatestensor* geschrieben werden, gleich sein `[[0,5], [1,0], [1,2]]` .

Während dieser Mandanten erfordert, dass die Dimension M mit der Anzahl der Elemente im eingabetensor identisch ist, schreibt dieser Operator nur maximal die outputcount-Elemente in diesen Mandanten. Outputcount wird durch den skalaren *outputzählensor* zurückgegeben.

> [!NOTE]
> Die übrigen Elemente dieses Mandanten außerhalb von outputcount sind nach Abschluss dieses Operators nicht definiert. Sie sollten sich nicht auf die Werte dieser Elemente verlassen.

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
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
" *Inputtensor*", " *outputcoordinatestensor*" und "" `OutputCountTensor` müssen dieselbe *DimensionCount* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Dimensionen | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | {[D0], D1, D2, D3, D4} | 4 bis 5 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Outputzählensor | Ausgabe | {[1], 1, 1, 1, 1} | 4 bis 5 | UINT32 |
| Outputcoordinatestensor | Ausgabe | {[1], 1, 1, M, N} | 4 bis 5 | UINT32 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |