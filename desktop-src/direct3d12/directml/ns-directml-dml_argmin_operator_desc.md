---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Gibt die Indizes der minimal wertigen Elemente innerhalb einer oder mehrerer Dimensionen des Eingabe Mandanten aus.
helpviewer_keywords:
- DML_ARGMIN_OPERATOR_DESC
- DML_ARGMIN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMIN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMIN_OPERATOR_DESC, DML_ARGMIN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
- directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
ms.openlocfilehash: 30d281c6ab35675e0cfce80b7eb025292c501041
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106367261"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a>DML_ARGMIN_OPERATOR_DESC-Struktur (directml. h)

Gibt die Indizes der minimal wertigen Elemente innerhalb einer oder mehrerer Dimensionen des Eingabe Mandanten aus.

Jedes Output-Element ist das Ergebnis der Anwendung einer *argmin* -Reduzierung auf eine Teilmenge des eingabetensors. Die *argmin* -Funktion gibt den Index des Minimalwert Elements innerhalb eines Satzes von Eingabe Elementen aus. Die Eingabeelemente, die an jeder Reduzierung beteiligt sind, werden durch die bereitgestellten Eingabe Achsen bestimmt. Ebenso ist jeder Ausgabe Index in Bezug auf die bereitgestellten Eingabe Achsen. Wenn alle Eingabe Achsen angegeben sind, wendet der Operator eine einzelne *argmin* -Reduzierung an und erzeugt ein einzelnes Output-Element.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax
```cpp
struct DML_ARGMIN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der zu lesende tensorflow.

`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der tensorflow, in den die Ergebnisse geschrieben werden sollen. Jedes Output-Element ist das Ergebnis einer *argmin* -Reduzierung für eine Teilmenge von Elementen aus dem *inputtensor*.

- *DimensionCount* muss mit *inputtensor. DimensionCount* (der Rang des Eingabe Mandanten beibehalten) identisch sein.
- *Größen* müssen mit " *inputtensor. sizes*" verglichen werden, mit Ausnahme der Dimensionen, die in den reduzierten *Achsen* enthalten sind, die die Größe 1 aufweisen müssen.

`AxisCount`

Typ: **[uint](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der zu reduzierenden Achsen. Dieses Feld bestimmt die Größe des *Achsen* Arrays.

`Axes`

Typ: \_ Field_size \_ (axiscount) **Konstanten [uint](/windows/desktop/WinProg/windows-data-types) \***

Die Achsen, auf die reduziert werden soll. Die Werte müssen im Bereich liegen `[0, InputTensor.DimensionCount - 1]` .

`AxisDirection`

DML_AXIS_DIRECTION axisdirection;

Typ: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Bestimmt, welcher Index ausgewählt werden soll, wenn mehrere Eingabeelemente denselben Wert aufweisen.
- **DML_AXIS_DIRECTION_INCREASING** gibt den Index des ersten Elements mit dem Minimalwert zurück (z. b. `argmin({1,2,3,2,1}) = 0` ).
- **DML_AXIS_DIRECTION_DECREASING** gibt den Index des letzten Minimalwert Elements zurück (z. b. `argmin({1,2,3,2,1}) = 4` ).

## <a name="examples"></a>Beispiele

In den Beispielen in diesem Abschnitt wird der gleiche zweidimensionale Eingabe Mandanten verwendet.

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a>Beispiel 1: Anwenden von *argmin* auf Spalten

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a>Beispiel 2: Anwenden von *argmin* auf Zeilen

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a>Beispiel 3: Anwenden von *argmin* auf alle Achsen (der gesamte Tensor)

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a>Bemerkungen
Die Ausgabe Mandanten Größen müssen mit den Eingabe-tensorflow-Größen identisch sein, mit Ausnahme der reduzierten Achsen, die 1 sein müssen.

Wenn *axisdirection* [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction)ist, entspricht diese API [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) mit [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).

Eine Teilmenge dieser Funktionalität wird durch den [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) -Operator verfügbar gemacht und auf früheren directml-featureebenen unterstützt.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*Inputtensor* und *outputtensor* müssen dieselbe *DimensionCount* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Outputtensor | Ausgabe | 1 bis 8 | Int64, Int32, UINT64, UInt32 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |