---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Führt eine Konvolution des *FilterTensor* mit dem *InputTensor aus.* Dieser Operator führt die Vorwärtskonvolution für ganzzahlige Daten aus.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f4045598dd1aa050479fec8e5732fe5c0a4e77ee
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550416"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a>DML_CONVOLUTION_INTEGER_OPERATOR_DESC-Struktur (directml.h)

Führt eine Konvolution des *FilterTensor* mit dem *InputTensor aus.* Dieser Operator führt die Vorwärtskonvolution für ganzzahlige Daten aus. Optionale Nullpunkt-Tensoren können auch verwendet werden, um Nullpunktwerte vom Eingabe- und Filter-Tensor zu subtrahieren.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Eingabedaten enthält. Die erwarteten Dimensionen des *InputTensor* sind `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputZeroPointTensor`

Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Eingabe-Nullpunktdaten enthält. Die erwarteten Dimensionen von *InputZeroPointTensor* sind `{ 1, 1, 1, 1 }` .


`FilterTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Filterdaten enthält. Die erwarteten Dimensionen von *FilterTensor* sind `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterZeroPointTensor`

Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält. Die erwarteten Dimensionen von *FilterZeroPointTensor* sind `{ 1, 1, 1, 1 }` , wenn eine Tensorquantisierung erforderlich ist, oder wenn eine `{ 1, OutputChannelCount, 1, 1 }` Pro-Kanal-Quantisierung erforderlich ist.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, in den die Ergebnisse geschrieben werden. Die erwarteten Dimensionen des *OutputTensor sind* `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der räumlichen Dimensionen für den Konvolutionsvorgang. Räumliche Dimensionen sind die unteren Dimensionen des *Konvolutionsfiltertensors*. Dieser Wert bestimmt auch die Größe der *Arrays Strides,* *Dilations,* *StartPadding* und *EndPadding.* Nur der Wert 2 wird unterstützt.


`Strides`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Ein Array, das die Schritte des Konvolutionsvorgang enthält. Diese Schritte werden auf den Konvolutionsfilter angewendet. Sie sind getrennt von den Tensorschritten, [](/windows/win32/api/directml/ns-directml-dml_tensor_desc)die in DML_TENSOR_DESC.


`Dilations`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Ein Array, das die Dilationen des Konvolutionsvorgang enthält. Dilationen sind Schritte, die auf die Elemente des Filterkernels angewendet werden. Dies hat den Effekt, dass ein größerer Filterkernel simuliert wird, indem die internen Filterkernelelemente mit Nullen aufschlossen werden.


`StartPadding`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Ein Array, das die Auf padding-Werte enthält, die am Anfang jeder räumlichen Dimension des Filters und des Eingabetensors des Konvolutionsvorgang angewendet werden sollen.


`EndPadding`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Ein Array mit den Auf padding-Werten, die auf das Ende jeder räumlichen Dimension des Filters und des Eingabetensors des Konvolutionsvorgang angewendet werden sollen.


`GroupCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Gruppen, in die der Konvolutionsvorgang unterteilt werden soll. *GroupCount* kann verwendet werden, um eine tiefenweise Konvolution zu erreichen, indem *GroupCount* auf die Anzahl der Eingabekanäle festgelegt wird. Dadurch wird die Konvolution in eine separate Konvolution pro Eingabekanal unterteilt.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
* *FilterTensor* und *FilterZeroPointTensor* müssen den gleichen *Datentyp aufweisen.*
* *InputTensor* und *InputZeroPointTensor* müssen den gleichen *Datentyp aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Dimensionen | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Eingabe | { BatchCount, InputChannelCount, InputHeight, InputWidth } | 4 | INT8, UINT8 |
| InputZeroPointTensor | Optionale Eingabe | { 1, 1, 1, 1 } | 4 | INT8, UINT8 |
| FilterTensor | Eingabe | { FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth } | 4 | INT8, UINT8 |
| FilterZeroPointTensor | Optionale Eingabe | { 1, FilterZeroPointChannelCount, 1, 1 } | 4 | INT8, UINT8 |
| OutputTensor | Ausgabe | { BatchCount, OutputChannelCount, OutputHeight, OutputWidth } | 4 | INT32 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |