---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Berechnet backpropagierungs Gradienten für Slice (siehe [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 63ea67454965d976247c3cdd50aa183f6a676138
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106365212"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a>DML_SLICE_GRAD_OPERATOR_DESC-Struktur (directml. h)

Berechnet backpropagierungs Gradienten für Slice (siehe [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).

Denken Sie daran, dass [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) einen Unterbereich eines Eingabe Mandanten extrahiert. Wenn ein *inputgradienttensor* mit denselben Größen wie die *Ausgabe* eines äquivalenten **DML_SLICE1_OPERATOR_DESC** angegeben wird, erzeugt dieser Operator einen *outputgradienttensor* mit denselben Größen wie die *Eingabe* von **DML_SLICE1_OPERATOR_DESC**. Die in Slices aufgeschnittenen Elemente werden an die Ausgabe weitergegeben, und alle anderen Elemente werden auf 0 festgelegt.

Sehen Sie sich als Beispiel eine **DML_SLICE1_OPERATOR_DESC** an, die die folgenden Elemente aus einem Mandanten extrahiert:

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

Wenn sich die gleichen *inputwindowoffsets*- / *Größen* /  wie im obigen Beispiel befinden, führt dieser Operator die folgende Transformation aus.

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a>Member

`InputGradientTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingehende gradiententensor. Dies wird in der Regel aus der Ausgabe der Rück Propagierung einer vorangehenden Ebene abgerufen. In der Regel hat dieser tensorflow die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) im Forward-Pass.

`OutputGradientTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe Mandanten, der die zurückgegebenen Farbverläufe enthält. In der Regel hat dieser Mandanten die gleichen Größen wie die *Eingabe* des entsprechenden [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) im Forward-Durchlauf.

`DimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Elemente in den Arrays *inputwindowoffsets*, *inputwindowsizes* und *inputwindowclaims* . Dieser Wert muss mit der *DimensionCount* übereinstimmen, die in *inputgradienttensor* und *outputgradienttensor* bereitgestellt wird.

`InputWindowOffsets`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Weitere Informationen finden Sie unter *inputwindowoffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowSizes`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Weitere Informationen finden Sie unter *inputwindowsizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowStrides`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Weitere Informationen finden Sie unter *inputwindowclaims* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

Beachten Sie, dass dieser Operator im Gegensatz zu **DML_SLICE1_OPERATOR_DESC** Schritte ungleich 0 (null) erfordert. Das liegt daran, dass bei einem NULL-Stride nicht eindeutig ist, welche Eingabeelemente den einzelnen Ausgabe Elementen zugeordnet werden sollen. Daher kann die Rück Verbreitung nicht ausgeführt werden. Wie **DML_SLICE1_OPERATOR_DESC** kippen negative Fortschritte die Eingabefenster Richtung entlang dieser Achse.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*Inputgradienttensor* und *outputgradienttensor* müssen denselben *Datentyp* und *DimensionCount* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Input gradienttensor | Eingabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Outputgradienttensor | Ausgabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |