---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Gibt die Indizes der Minimalwertelemente innerhalb einer oder mehrere Dimensionen des Eingabetensors aus.
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
ms.openlocfilehash: da270ea5354e361067335ba1c789efe18310437a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417743"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a>DML_ARGMIN_OPERATOR_DESC -Struktur (directml.h)

Gibt die Indizes der Minimalwertelemente innerhalb einer oder mehrere Dimensionen des Eingabetensors aus.

Jedes Ausgabeelement ist das Ergebnis der Anwendung einer *Argminverringerung* auf eine Teilmenge des Eingabetensors. Die *argmin-Funktion* gibt den Index des Minimalwertelements in einem Satz von Eingabeelementen aus. Die an jeder Reduzierung beteiligten Eingabeelemente werden durch die bereitgestellten Eingabeachsen bestimmt. Ebenso gilt jeder Ausgabeindex in Bezug auf die bereitgestellten Eingabeachsen. Wenn alle Eingabeachsen angegeben sind, wendet der Operator eine einzelne *Argminverringerung* an und erzeugt ein einzelnes Ausgabeelement.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

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

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, aus dem gelesen werden soll.

`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, in den die Ergebnisse geschrieben werden. Jedes Ausgabeelement ist das Ergebnis einer *Argminverringerung* für eine Teilmenge von Elementen aus *dem InputTensor.*

- *DimensionCount* muss mit *InputTensor.DimensionCount übereinstimmen* (der Rang des Eingabetensors wird beibehalten).
- *Größen müssen* mit *InputTensor.Sizes übereinstimmen,* mit Ausnahme der Dimensionen, die in den reduzierten Achsen enthalten *sind,* die die Größe 1 haben müssen.

`AxisCount`

Typ: **[UINT](../../winprog/windows-data-types.md)**

Die Anzahl der zu reduzierenden Achsen. Dieses Feld bestimmt die Größe des *Achsenarrays.*

`Axes`

Typ: \_ Field_size \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***

Die Achsen, entlang derer reduziert werden soll. Werte müssen im Bereich `[0, InputTensor.DimensionCount - 1]` liegen.

`AxisDirection`

DML_AXIS_DIRECTION AxisDirection;

Typ: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Bestimmt, welcher Index ausgewählt werden soll, wenn mehrere Eingabeelemente denselben Wert haben.
- **DML_AXIS_DIRECTION_INCREASING** gibt den Index des ersten Minimumwertelements zurück (z. B. `argmin({1,2,3,2,1}) = 0` ).
- **DML_AXIS_DIRECTION_DECREASING** gibt den Index des letzten Minimumwertelements zurück (z. B. `argmin({1,2,3,2,1}) = 4` ).

## <a name="examples"></a>Beispiele

In den Beispielen in diesem Abschnitt wird der gleiche zweidimensionale Eingabetensor verwendet.

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a>Beispiel 1: Anwenden *von argmin* auf Spalten

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a>Beispiel 2: Anwenden *von Argmin* auf Zeilen

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a>Beispiel 3: Anwenden *von argmin* auf alle Achsen (den gesamten Tensor)

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a>Hinweise
Die Ausgabetensorgrößen müssen mit den Eingabetensorgrößen identisch sein, mit Ausnahme der reduzierten Achsen, die 1 sein müssen.

Wenn *AxisDirection* [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction)ist, entspricht diese API [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) mit [DML_REDUCE_FUNCTION_ARGMIN.](/windows/win32/api/directml/ne-directml-dml_reduce_function)

Eine Teilmenge dieser Funktionalität wird [](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) über den DML_REDUCE_OPERATOR_DESC verfügbar gemacht und auf früheren DirectML-Featureebenen unterstützt.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*InputTensor und* *OutputTensor* müssen denselben *DimensionCount aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Ausgabe | 1 bis 8 | INT64, INT32, UINT64, UINT32 |

## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |