---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Führt eine Zusammenführung des *filtertensor* mit dem *inputtensor* aus. Dieser Operator führt vorwärts Vorgänge für quantifizierte Daten aus. Dieser Operator entspricht mathematisch dem dequantifialisieren der Eingaben, dem durchwinken und dem anschließenden quantifialisieren der Ausgabe.
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
ms.openlocfilehash: 01193b19744f413690a3cb5ecccbb8fa60626cb0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361109"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC-Struktur (directml. h)
Führt eine Zusammenführung des *filtertensor* mit dem *inputtensor* aus. Dieser Operator führt vorwärts Vorgänge für quantifizierte Daten aus. Dieser Operator entspricht mathematisch dem dequantifialisieren der Eingaben, dem durchwinken und dem anschließenden quantifialisieren der Ausgabe. 

Die von diesem Operator verwendeten linearen quantize-Funktionen sind die linearen quantifizierungsfunktionen.

### <a name="dequantize-function"></a>Funktion "Debug"

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Quantize-Funktion

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Eingabedaten enthält. Die erwarteten Dimensionen von " *inputtensor* " sind `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputScaleTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow mit den Eingabedaten der Skala. Die erwarteten Dimensionen von `InputScaleTensor` sind `{ 1, 1, 1, 1 }` . Dieser Skalierungs Wert wird zum dequantifialisieren der Eingabewerte verwendet.


`InputZeroPointTensor`

Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Eingabedaten für den Nullpunkt enthält. Die erwarteten Dimensionen von *inputzeropointtensor* sind `{ 1, 1, 1, 1 }` . Dieser Nullpunktwert wird zum decomieren der Eingabewerte verwendet.


`FilterTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Filterdaten enthält. Die erwarteten Dimensionen des *filtertensor* sind `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterScaleTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Filter Skalierungs Daten enthält. Die erwarteten Dimensionen von `FilterScaleTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, OutputChannelCount, 1, 1 }` Wenn die pro-Kanal-Quantifizierung erforderlich ist. Dieser Skalierungs Wert wird zum dequantifialisieren der Filter Werte verwendet.


`FilterZeroPointTensor`

Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Filter-NULL-Punktdaten enthält. Die erwarteten Dimensionen von " *filterzeropointtensor* " sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist oder `{ 1, OutputChannelCount, 1, 1 }` Wenn eine pro-Kanal-Quantifizierung erforderlich ist. Dieser Nullpunktwert wird zum decomieren der Filter Werte verwendet.


`BiasTensor`

Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Daten der Bias enthält. Der Bias-tensorflow ist ein tensorflow, der Daten enthält, die über den Ausgabe Mandanten am Ende der Konvolution übertragen werden, die dem Ergebnis hinzugefügt wird. Die erwarteten Dimensionen von biastensor sind `{ 1, OutputChannelCount, 1, 1 }` für 4D.


`OutputScaleTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Daten der Ausgabe Skala enthält. Die erwarteten Dimensionen von outputscaletensor sind `{ 1, 1, 1, 1 }` . Dieser Wert für die Eingabe Skala wird zum quantifialisieren der Ausgabewerte der-Werte verwendet.


`OutputZeroPointTensor`

Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Filter-NULL-Punktdaten enthält. Die erwarteten Dimensionen von outputzeropointtensor sind `{ 1, 1, 1, 1 }` . Dieser Wert für die Eingabe von null Punkten wird zum quantifialisieren der Ausgabewerte verwendet.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, in den die Ergebnisse geschrieben werden sollen. Die erwarteten Dimensionen von outputtensor sind `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl räumlicher Dimensionen für den Vorgangs Vorgang. Räumliche Dimensionen sind die unteren Dimensionen des tensorflow- *filtertensors* für den Verbindungs Filter. Dieser Wert bestimmt auch die Größe der Felder " *fort* schreiten *", "Erweiterungen", "* *startpadding*" und " *endpadding* ". Nur der Wert 2 wird unterstützt.


`Strides`

Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***

Die Fortschritte des Vorgangs. Diese Schritte werden auf den Konfigurations Filter angewendet. Sie sind von den in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)enthaltenen tensorflow-Schritten getrennt.


`Dilations`

Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***

Die Erweiterungen des Vorgangs. Erweiterungen sind Schritte, die auf die Elemente des Filter Kernels angewendet werden. Dies hat den Effekt, einen größeren Filter Kernel zu simulieren, indem die internen Filter-Kernel Elemente mit Nullen aufgefüllt werden.


`StartPadding`

Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***

Die Auffüll Werte, die auf den Anfang jeder räumlichen Dimension des Filters und des Eingabe-Tensors des Vorgangs angewendet werden sollen.


`EndPadding`

Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***

Die Auffüll Werte, die auf das Ende jeder räumlichen Dimension des Filters und des Eingabe-Tensors der Konvolution-Operation angewendet werden sollen.


`GroupCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Gruppen, in die der Vorgang unterteilt werden soll. *GroupCount* kann verwendet werden, um eine tiefgreifende Zusammenführung zu erzielen, indem *GroupCount* auf die Anzahl der Eingabe Kanäle festgelegt wird. Dadurch wird die zusammen Gabe in eine separate zusammen Gabe pro Eingabe Kanal aufgeteilt. 

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *Filtertensor* und *filterzeropointtensor* müssen denselben *Datentyp* aufweisen.
* *Inputtensor* und *inputzeropointtensor* müssen denselben *Datentyp* aufweisen.
* *Outputtensor* und `OutputZeroPointTensor` muss denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 | Int8, Uint8 |
| Inputscaletensor | Eingabe | 4 | Float32 |
| Inputzeropointtensor | Optionale Eingabe | 4 | Int8, Uint8 |
| Filtertensor | Eingabe | 4 | Int8, Uint8 |
| Filterscaletensor | Eingabe | 4 | Float32 |
| Filterzeropointtensor | Optionale Eingabe | 4 | Int8, Uint8 |
| Biastensor | Optionale Eingabe | 4 | INT32 |
| Outputscaletensor | Eingabe | 4 | Float32 |
| Outputzeropointtensor | Optionale Eingabe | 4 | Int8, Uint8 |
| Outputtensor | Ausgabe | 4 | Int8, Uint8 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |