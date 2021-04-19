---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Führt eine Zusammenführung des *filtertensor* mit dem *inputtensor* aus. Dieser Operator führt vorwärts Vorgänge für ganzzahlige Daten aus.
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
ms.openlocfilehash: c16690ea1e3049ffeba398bbbaca2003f965a832
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106367265"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a>DML_CONVOLUTION_INTEGER_OPERATOR_DESC-Struktur (directml. h)

Führt eine Zusammenführung des *filtertensor* mit dem *inputtensor* aus. Dieser Operator führt vorwärts Vorgänge für ganzzahlige Daten aus. Optionale Null-Punkt-Tensoren können auch verwendet werden, um NULL-Punktwerte aus dem Eingabe-und Filter Tensor zu subtrahieren.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Eingabedaten enthält. Die erwarteten Dimensionen von " *inputtensor* " sind `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputZeroPointTensor`

Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Eingabedaten für den Nullpunkt enthält. Die erwarteten Dimensionen von *inputzeropointtensor* sind `{ 1, 1, 1, 1 }` .


`FilterTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Filterdaten enthält. Die erwarteten Dimensionen des *filtertensor* sind `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterZeroPointTensor`

Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Filter-NULL-Punktdaten enthält. Die erwarteten Dimensionen von " *filterzeropointtensor* " sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist oder `{ 1, OutputChannelCount, 1, 1 }` Wenn die pro-Kanal-Quantifizierung erforderlich ist.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der tensorflow, in den die Ergebnisse geschrieben werden sollen. Die erwarteten Dimensionen von *outputtensor* sind `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl räumlicher Dimensionen für den Vorgangs Vorgang. Räumliche Dimensionen sind die niedrigeren Dimensionen von "- *filtertensor*". Dieser Wert bestimmt auch die Größe der Felder " *fort* schreiten *", "Erweiterungen", "* *startpadding*" und " *endpadding* ". Nur der Wert 2 wird unterstützt.


`Strides`

Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***

Ein Array, das die Fortschritte der Zusammenführung des Vorgangs enthält. Diese Schritte werden auf den Konfigurations Filter angewendet. Sie sind von den in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)enthaltenen tensorflow-Schritten getrennt.


`Dilations`

Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***

Ein Array, das die Erweiterungen der Vorgangs Operation enthält. Erweiterungen sind Schritte, die auf die Elemente des Filter Kernels angewendet werden. Dies hat den Effekt, einen größeren Filter Kernel zu simulieren, indem die internen Filter-Kernel Elemente mit Nullen aufgefüllt werden.


`StartPadding`

Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***

Ein Array, das die Auffüll Werte enthält, die auf den Anfang jeder räumlichen Dimension des Filters und eingabetensors des Vorgangs angewendet werden sollen.


`EndPadding`

Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***

Ein Array, das die Auffüll Werte enthält, die auf das Ende jeder räumlichen Dimension des Filters und des Eingabe-Tensors der Konvolution-Operation angewendet werden sollen.


`GroupCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Gruppen, in die der Vorgang in den Vorgang aufgeteilt werden soll. *GroupCount* kann verwendet werden, um eine tiefgreifende Zusammenführung zu erzielen, indem *GroupCount* auf die Anzahl der Eingabe Kanäle festgelegt wird. Dadurch wird die zusammen Gabe in eine separate zusammen Gabe pro Eingabe Kanal aufgeteilt.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *Filtertensor* und *filterzeropointtensor* müssen denselben *Datentyp* aufweisen.
* *Inputtensor* und *inputzeropointtensor* müssen denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Dimensionen | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | {BatchCount, inputchannelcount, inputheight, inputwidth} | 4 | Int8, Uint8 |
| Inputzeropointtensor | Optionale Eingabe | {1, 1, 1} | 4 | Int8, Uint8 |
| Filtertensor | Eingabe | {Filterbatchcount, filterchannelcount, filterheight, filterwidth} | 4 | Int8, Uint8 |
| Filterzeropointtensor | Optionale Eingabe | {1, filterzerkopintchannelcount, 1, 1} | 4 | Int8, Uint8 |
| Outputtensor | Ausgabe | {BatchCount, outputchannelcount, OutputHeight, OutputWidth} | 4 | INT32 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |