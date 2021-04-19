---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Fasst die Elemente eines Mandanten auf einer Achse zusammen, wobei der laufende Zähler der Summierungs-in den Ausgabe Mandanten geschrieben wird.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106355095"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a>DML_CUMULATIVE_SUMMATION_OPERATOR_DESC-Struktur (directml. h)

Fasst die Elemente eines Mandanten auf einer Achse zusammen, wobei der laufende Zähler der Summierungs-in den Ausgabe Mandanten geschrieben wird.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a>Member

`InputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingabensor, der die zu summierenden Elemente enthält.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe Mandanten, in den die resultierenden kumulativen Summen geschrieben werden sollen. Dieser Mandanten muss dieselbe Größe und denselben Datentyp aufweisen wie der *inputtensor*.


`Axis`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Der Index der Dimension, über die Elemente zusammengefasst werden sollen. Dieser Wert muss kleiner als die *DimensionCount* von " *inputtensor*" sein.


`AxisDirection`

Typ: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Einer der Werte der [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) Enumeration. Wenn der Wert auf **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, erfolgt die Summe, indem der tensorflow entlang der angegebenen Achse durch den aufsteigenden Element Index durchlaufen wird. Wenn **DML_AXIS_DIRECTION_DECREASING** auf festgelegt ist, ist der umgekehrte Wert true, und die Summe erfolgt durch das Durchlaufen von Elementen nach absteigender Index.


`HasExclusiveSum`




## <a name="remarks"></a>Bemerkungen
Dieser Operator unterstützt die direkte Ausführung, d. h., der *outputtensor* ist berechtigt, den *inputtensor* während der Bindung zu Alias.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*Inputtensor* und *outputtensor* müssen über denselben *Datentyp* und dieselben *Größen* verfügen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 | Float32, FLOAT16, UInt32, UInt16 |
| Outputtensor | Ausgabe | 4 | Float32, FLOAT16, UInt32, UInt16 |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |