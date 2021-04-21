---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Führt eine Konvolution des *FilterTensor mit* dem *InputTensor aus.* Dieser Operator führt die Vorwärtskonvolution für ganzzahlige Daten aus.
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
ms.openlocfilehash: 07406155be9ae5f78fbf5f3b7fcd750aa4631dbc
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803375"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a>DML_CONVOLUTION_INTEGER_OPERATOR_DESC -Struktur (directml.h)

Führt eine Konvolution des *FilterTensor mit* dem *InputTensor aus.* Dieser Operator führt die Vorwärtskonvolution für ganzzahlige Daten aus. Optionale Nullpunkt-Tensoren können auch verwendet werden, um Nullpunktwerte vom Eingabe- und Filtertensor zu subtrahieren.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

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

Ein Tensor, der die Eingabedaten enthält. Die erwarteten Dimensionen des *InputTensor sind* `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputZeroPointTensor`

Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Nullpunktdaten der Eingabe enthält. Die erwarteten Dimensionen des *InputZeroPointTensor sind* `{ 1, 1, 1, 1 }` .


`FilterTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Filterdaten enthält. Die erwarteten Dimensionen des *FilterTensor sind* `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterZeroPointTensor`

Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält. Die erwarteten Dimensionen des *FilterZeroPointTensor* sind , wenn eine Tensorquantisierung erforderlich ist oder wenn eine Quantisierung pro Kanal `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` erforderlich ist.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, in den die Ergebnisse geschrieben werden sollen. Die erwarteten Dimensionen des *OutputTensor* sind `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der räumlichen Dimensionen für den Konvolutionsvorgang. Räumliche Dimensionen sind die unteren Dimensionen der Konvolution *FilterTensor*. Dieser Wert bestimmt auch die Größe der Arrays *Strides*, *Dilations*, *StartPadding* und *EndPadding.* Es wird nur der Wert 2 unterstützt.


`Strides`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Ein Array, das die Schritte des Konvolutionsvorgangs enthält. Diese Schritte werden auf den Konvolutionsfilter angewendet. Sie sind von den Tensorschritten getrennt, die in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)enthalten sind.


`Dilations`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Ein Array, das die Sortierungen des Konvolutionsvorgangs enthält. Dilations sind Schritte, die auf die Elemente des Filterkernels angewendet werden. Dies hat den Effekt, dass ein größerer Filterkernel simuliert wird, indem die internen Filterkernelelemente mit Nullen auffüllt werden.


`StartPadding`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Ein Array, das die Auffüllwerte enthält, die am Anfang jeder räumlichen Dimension des Filters und eingabe tensor des Konvolutionsvorgangs angewendet werden sollen.


`EndPadding`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Ein Array, das die Auffüllwerte enthält, die am Ende jeder räumlichen Dimension des Filters und eingabe tensor des Konvolutionsvorgangs angewendet werden sollen.


`GroupCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Gruppen, in die der Konvolutionsvorgang unterteilt werden soll. *GroupCount* kann verwendet werden, um eine tiefenweise Konvolution zu erreichen, indem *GroupCount* auf die Anzahl der Eingabekanäle gesetzt wird. Dadurch wird die Konvolution in eine separate Konvolution pro Eingabekanal unterteilt.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *FilterTensor und* *FilterZeroPointTensor* müssen denselben *Datentyp haben.*
* *InputTensor* und *InputZeroPointTensor* müssen denselben *Datentyp haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Dimensionen | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
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