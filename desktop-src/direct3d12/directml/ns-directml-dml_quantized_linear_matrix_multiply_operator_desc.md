---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Führt eine Matrixmultiplikationsfunktion für quantisierte Daten aus. Dieser Operator entspricht mathematisch der Dequantisierung der Eingaben, der anschließenden Matrixmultiplikation und der anschließenden Quantisierung der Ausgabe.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417810"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC-Struktur (directml.h)
Führt eine Matrixmultiplikationsfunktion für quantisierte Daten aus. Dieser Operator entspricht mathematisch der Dequantisierung der Eingaben, der anschließenden Matrixmultiplikation und der anschließenden Quantisierung der Ausgabe.

Dieser Operator erfordert, dass die Matrix-Multiplikationseingabe-Tensoren 4D sind, die als formatiert `{ BatchCount, ChannelCount, Height, Width }` sind. Der Matrixmultiplikationsoperator führt BatchCount * ChannelCount anzahl unabhängiger Matrixmultiplikationen aus. 

Wenn *ATensor* z. *B. Größen* von und `{ BatchCount, ChannelCount, M, K }` *BTensor* *größen* von `{ BatchCount, ChannelCount, K, N }` und *OutputTensor* *Größen* von aufweist, führt `{ BatchCount, ChannelCount, M, N }` der Multiplikationsoperator der Matrix BatchCount * ChannelCount unabhängige Matrixmultiplikationen der Dimensionen {M,K} x {K,N} = {M,N} aus. 

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
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Member

`ATensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die A-Daten enthält. Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, M, K }` sein.


`AScaleTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die ATensor-Skalierungsdaten enthält. Die erwarteten Dimensionen von `AScaleTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn eine Quantisierung pro Zeile erforderlich ist. Diese Skalierungswerte werden zum Dequantisieren der A-Werte verwendet.


`AZeroPointTensor`

Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Nullpunktdaten von *ATensor* enthält. Die erwarteten Dimensionen von AZeroPointTensor sind `{ 1, 1, 1, 1 }` , wenn eine Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn eine Quantisierung pro Zeile erforderlich ist. Diese Nullpunktwerte werden zum Dequantisieren der ATensor-Werte verwendet.


`BTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die B-Daten enthält. Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, K, N }` sein.


`BScaleTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die *BTensor-Skalierungsdaten* enthält. Die erwarteten Dimensionen von `BScaleTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, 1, N }` wenn eine Spaltenquantisierung erforderlich ist. Diese Skalierungswerte werden zum Dequantisieren der *BTensor-Werte* verwendet.


`BZeroPointTensor`

Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Nullpunktdaten von *BTensor* enthält. Die erwarteten Dimensionen von `BZeroPointTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, 1, N }` wenn eine Spaltenquantisierung erforderlich ist. Diese Nullpunktwerte werden zum Dequantisieren der *BTensor-Werte* verwendet.


`OutputScaleTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Filterskalierdaten enthält. Die erwarteten Dimensionen von `OutputScaleTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn eine Quantisierung pro Zeile erforderlich ist. Dieser Skalierungswert wird zum Dequantisieren der Filterwerte verwendet.


`OutputZeroPointTensor`

Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält. Die erwarteten Dimensionen von `OutputZeroPointTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn eine Quantisierung pro Zeile erforderlich ist. Dieser Nullpunktwert wird zum Dequantisieren der Filterwerte verwendet.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, in den die Ergebnisse geschrieben werden sollen. Die Dimensionen dieses Tensors sind `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
* *ATensor* und `AZeroPointTensor` müssen den gleichen *DataType aufweisen.*
* *BTensor* und `BZeroPointTensor` müssen den gleichen Datentyp *aufweisen.*
* *OutputTensor* und `OutputZeroPointTensor` müssen den gleichen Datentyp *aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Eingabe | 4 | INT8, UINT8 |
| AScaleTensor | Eingabe | 4 | FLOAT32 |
| AZeroPointTensor | Optionale Eingabe | 4 | INT8, UINT8 |
| BTensor | Eingabe | 4 | INT8, UINT8 |
| BScaleTensor | Eingabe | 4 | FLOAT32 |
| BZeroPointTensor | Optionale Eingabe | 4 | INT8, UINT8 |
| OutputScaleTensor | Eingabe | 4 | FLOAT32 |
| OutputZeroPointTensor | Optionale Eingabe | 4 | INT8, UINT8 |
| OutputTensor | Ausgabe | 4 | INT8, UINT8 |



## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |