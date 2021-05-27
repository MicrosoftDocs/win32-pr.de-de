---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Führt eine Konvolution des *FilterTensor* mit dem *InputTensor aus.* Dieser Operator führt die Vorwärtskonvolution für quantisierte Daten aus. Dieser Operator entspricht mathematisch der Dequantisierung der Eingaben, der Verschachtelung und der anschließenden Quantisierung der Ausgabe.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 5b98e1f57268cab70c2fb672991bce3d67419db8
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549784"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC-Struktur (directml.h)
Führt eine Konvolution des *FilterTensor* mit dem *InputTensor aus.* Dieser Operator führt die Vorwärtskonvolution für quantisierte Daten aus. Dieser Operator entspricht mathematisch der Dequantisierung der Eingaben, der Verschachtelung und der anschließenden Quantisierung der Ausgabe. 

Die von diesem Operator verwendeten linearen Quantisierungsfunktionen sind die linearen Quantisierungsfunktionen.

### <a name="dequantize-function"></a>Dequantize-Funktion

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Quantize-Funktion

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
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

Ein Tensor, der die Eingabedaten enthält. Die erwarteten Dimensionen des *InputTensor* sind `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputScaleTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Eingabeskalierdaten enthält. Die erwarteten Dimensionen von `InputScaleTensor` sind `{ 1, 1, 1, 1 }` . Dieser Skalierungswert wird zum Dequantisieren der Eingabewerte verwendet.


`InputZeroPointTensor`

Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Nullpunktdaten der Eingabe enthält. Die erwarteten Dimensionen des *InputZeroPointTensor sind* `{ 1, 1, 1, 1 }` . Dieser Nullpunktwert wird zum Dequantisieren der Eingabewerte verwendet.


`FilterTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Filterdaten enthält. Die erwarteten Dimensionen des *FilterTensor sind* `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterScaleTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Filterskalierdaten enthält. Die erwarteten Dimensionen von sind `FilterScaleTensor` , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` Quantisierung pro Kanal erforderlich ist. Dieser Skalierungswert wird zum Dequantisieren der Filterwerte verwendet.


`FilterZeroPointTensor`

Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält. Die erwarteten Dimensionen des *FilterZeroPointTensor* sind , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine Quantisierung pro Kanal `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` erforderlich ist. Dieser Nullpunktwert wird zum Dequantisieren der Filterwerte verwendet.


`BiasTensor`

Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Biasdaten enthält. Der Bias-Tensor ist ein Tensor, der Daten enthält, die über den Ausgabetensor am Ende der Konvolution übertragen werden, der dem Ergebnis hinzugefügt wird. Die erwarteten Dimensionen des BiasTensor sind `{ 1, OutputChannelCount, 1, 1 }` für 4D.


`OutputScaleTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Ausgabeskalierdaten enthält. Die erwarteten Dimensionen von OutputScaleTensor sind `{ 1, 1, 1, 1 }` . Dieser Eingabeskalierungswert wird zum Quantisieren der Konvolutionsausgabewerte verwendet.


`OutputZeroPointTensor`

Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält. Die erwarteten Dimensionen von OutputZeroPointTensor sind `{ 1, 1, 1, 1 }` . Dieser Eingabe-Nullpunktwert wird zum Quantisieren der Konvolution der Ausgabewerte verwendet.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, in den die Ergebnisse geschrieben werden sollen. Die erwarteten Dimensionen des OutputTensor sind `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der räumlichen Dimensionen für den Konvolutionsvorgang. Räumliche Dimensionen sind die unteren Dimensionen des Konvolutionsfilters Tensor *FilterTensor*. Dieser Wert bestimmt auch die Größe der Arrays *Strides*, *Dilations*, *StartPadding* und *EndPadding.* Es wird nur der Wert 2 unterstützt.


`Strides`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Die Fortschritte des Konvolutionsvorgangs. Diese Schritte werden auf den Konvolutionsfilter angewendet. Sie sind von den Tensorschritten getrennt, die in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)enthalten sind.


`Dilations`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Die Dilationen des Konvolutionsvorgangs. Dilationen sind Schritte, die auf die Elemente des Filterkernels angewendet werden. Dies hat den Effekt, dass ein größerer Filterkernel simuliert wird, indem die internen Filterkernelelemente mit Nullen aufschlossen werden.


`StartPadding`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Die Auf padding-Werte, die am Anfang jeder räumlichen Dimension des Filters und des Eingabetensors des Konvolutionsvorgang angewendet werden sollen.


`EndPadding`

Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Die Auf padding-Werte, die auf das Ende jeder räumlichen Dimension des Filters und des Eingabetensors des Konvolutionsvorgang angewendet werden sollen.


`GroupCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Gruppen, in die der Konvolutionsvorgang unterteilt werden soll. *GroupCount* kann verwendet werden, um eine tiefenorientierte Konvolution zu erreichen, indem *GroupCount* auf die Anzahl der Eingabekanäle gesetzt wird. Dadurch wird die Konvolution in eine separate Konvolution pro Eingabekanal unterteilt. 

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *FilterTensor und* *FilterZeroPointTensor* müssen denselben *Datentyp haben.*
* *InputTensor* und *InputZeroPointTensor* müssen denselben *Datentyp haben.*
* *OutputTensor* und `OutputZeroPointTensor` müssen den gleichen Datentyp *haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | INT8, UINT8 |
| InputScaleTensor | Eingabe | 4 | FLOAT32 |
| InputZeroPointTensor | Optionale Eingabe | 4 | INT8, UINT8 |
| FilterTensor | Eingabe | 4 | INT8, UINT8 |
| FilterScaleTensor | Eingabe | 4 | FLOAT32 |
| FilterZeroPointTensor | Optionale Eingabe | 4 | INT8, UINT8 |
| BiasTensor | Optionale Eingabe | 4 | INT32 |
| OutputScaleTensor | Eingabe | 4 | FLOAT32 |
| OutputZeroPointTensor | Optionale Eingabe | 4 | INT8, UINT8 |
| OutputTensor | Ausgabe | 4 | INT8, UINT8 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |