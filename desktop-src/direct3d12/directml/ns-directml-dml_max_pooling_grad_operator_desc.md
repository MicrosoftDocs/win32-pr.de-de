---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Berechnet backpropagierungs Gradienten für Max Pooling (siehe [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: b7314cb6b9456d9ac9f99e90100085e86f88ffd9
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354285"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a>DML_MAX_POOLING_GRAD_OPERATOR_DESC-Struktur (directml. h)

Berechnet backpropagierungs Gradienten für Max Pooling (siehe [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).

Angenommen, ein 2 x 2- **DML_MAX_POOLING2_OPERATOR_DESC** ohne Auffüll-und Vergrößerungen und ein Schritt von 1, der Folgendes ausführt:

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

Das größte Element jedes 2 x 2-Fensters im Eingabe Mandanten erzeugt ein Element der Ausgabe. Im folgenden finden Sie ein Beispiel für die Ausgabe von **DML_MAX_POOLING_GRAD_OPERATOR_DESC** mit ähnlichen Parametern.

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

In der Tat verwendet dieser Operator den *inputtensor* , um den Index des größten Elements in jedem Fenster zu bestimmen, und verteilt die Werte von *inputgradienttensor* basierend auf diesen Indizes in den *outputgradienttensor* . Wenn Indizes überlappen, werden die Werte summiert. Alle nicht referenzierten Ausgabe Elemente werden nulgerert.

Im Fall einer Verknüpfung (bei der mehr als ein Element in einem Fenster denselben maximalen Wert aufweist), wird das Element mit dem niedrigsten logischen Element Index ausgewählt.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingabefeaturetensor. Dabei handelt es sich in der Regel um denselben tensorflow, der als *inputtensor* zur [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) im Forward-Durchlauf bereitgestellt wurde.

`InputGradientTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingehende gradiententensor. Dies wird in der Regel aus der Ausgabe der Rück Propagierung einer vorangehenden Ebene abgerufen. In der Regel hat dieser tensorflow die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) im Forward-Durchlauf.

`OutputGradientTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe Mandanten, der die zurückgegebenen Farbverläufe enthält. In der Regel hat dieser Mandanten die gleichen Größen wie die *Eingabe* der entsprechenden [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) im Forward-Durchlauf.

`DimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Elemente in den Arrays "Step", " *WindowSize*", " *startpadding* *", "* *endpadding*" und " *Vergrößerungen* ". Dieser Wert muss gleich der Anzahl räumlicher Dimensionen ("DimensionCount-2" von inputtensor) sein. Da dieser Operator nur 4D-Tensoren unterstützt, ist der einzige gültige Wert für diesen Parameter 2.

`Strides`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Siehe *Schritte* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`WindowSize`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Siehe *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`StartPadding`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Siehe *startpadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`EndPadding`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Siehe *endpadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`Dilations`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Weitere *Informationen* finden Sie unter [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *Inputtensor* und *outputgradienttensor* müssen die gleichen *Größen* aufweisen.
* *Inputgradienttensor*, *inputtensor* und *outputgradienttensor* müssen denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Dimensionen | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | {BatchCount, ChannelCount, inputheight, inputwidth} | 4 | Float32, FLOAT16 |
| Input gradienttensor | Eingabe | {BatchCount, ChannelCount, OutputHeight, OutputWidth} | 4 | Float32, FLOAT16 |
| Outputgradienttensor | Ausgabe | {BatchCount, ChannelCount, inputheight, inputwidth} | 4 | Float32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |