---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Führt eine Matrix Multiplikations Funktion für quantifizierte Daten aus. Dieser Operator entspricht mathematisch der dequantifizierung der Eingaben, der anschließende Durchführung der Matrix Multiplikation und der anschließenden Quantifizierung der Ausgabe.
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
ms.openlocfilehash: d0b20a37bca6ddf6083b116b53290a6b6b2084f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106366358"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC-Struktur (directml. h)
Führt eine Matrix Multiplikations Funktion für quantifizierte Daten aus. Dieser Operator entspricht mathematisch der dequantifizierung der Eingaben, der anschließende Durchführung der Matrix Multiplikation und der anschließenden Quantifizierung der Ausgabe.

Für diesen Operator ist es erforderlich, dass die Eingabe-Tensoren der Matrix als 4D-Format multipliziert werden `{ BatchCount, ChannelCount, Height, Width }` . Der Matrix Multiplikations Operator führt die BatchCount * ChannelCount-Anzahl unabhängiger Matrix Multiplikationen durch. 

Wenn *atensor* z. b. *Größen* von hat `{ BatchCount, ChannelCount, M, K }` und *btensor* die *Größe* hat `{ BatchCount, ChannelCount, K, N }` und *outputtensor* über *Größen* von verfügt `{ BatchCount, ChannelCount, M, N }` , führt der Matrix Multiplikations Operator BatchCount * ChannelCount unabhängige Matrix Multiplikationen der Dimensionen {m, K} x {K, n} = {M, n} aus. 

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Daten enthält. Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, M, K }` .


`AScaleTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Daten der atensor-Skala enthält. Die erwarteten Dimensionen von `AScaleTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, M, 1 }` Wenn die pro-Zeilen-Quantifizierung erforderlich ist. Diese Skalierungs Werte werden zum dequantifialisieren der Werte verwendet.


`AZeroPointTensor`

Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Daten des *atensor* -NULL-Punkts enthält. Die erwarteten Dimensionen von azeropointtensor sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist oder `{ 1, 1, M, 1 }` Wenn pro Zeilen-Quantifizierung erforderlich ist. Diese nullpunktwerte werden zum decomieren der atensor-Werte verwendet.


`BTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die B-Daten enthält. Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, K, N }` .


`BScaleTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Daten der *btensor* -Skalierung enthält. Die erwarteten Dimensionen von `BScaleTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, 1, N }` Wenn pro Spalten Quantifizierung erforderlich ist. Diese Skalierungs Werte werden zum dequantifialisieren der *btensor* -Werte verwendet.


`BZeroPointTensor`

Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Daten des *btensor* -NULL-Punkts enthält. Die erwarteten Dimensionen von `BZeroPointTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, 1, N }` Wenn pro Spalten Quantifizierung erforderlich ist. Diese nullpunktwerte werden zum decomieren der *btensor* -Werte verwendet.


`OutputScaleTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Filter Skalierungs Daten enthält. Die erwarteten Dimensionen von `OutputScaleTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, M, 1 }` Wenn die pro-Zeilen-Quantifizierung erforderlich ist. Dieser Skalierungs Wert wird zum dequantifialisieren der Filter Werte verwendet.


`OutputZeroPointTensor`

Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Filter-NULL-Punktdaten enthält. Die erwarteten Dimensionen von `OutputZeroPointTensor` sind, `{ 1, 1, 1, 1 }` Wenn pro tensorflow-Quantifizierung erforderlich ist oder `{ 1, 1, M, 1 }` Wenn pro Zeilen-Quantifizierung erforderlich ist. Dieser Nullpunktwert wird zum decomieren der Filter Werte verwendet.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, in den die Ergebnisse geschrieben werden sollen. Die Dimensionen dieses Mandanten sind `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *Atensor* und `AZeroPointTensor` muss denselben *Datentyp* aufweisen.
* *Btensor* und `BZeroPointTensor` muss denselben *Datentyp* aufweisen.
* *Outputtensor* und `OutputZeroPointTensor` muss denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Atensor | Eingabe | 4 | Int8, Uint8 |
| Ascaletensor | Eingabe | 4 | Float32 |
| Azeropointtensor | Optionale Eingabe | 4 | Int8, Uint8 |
| Btensor | Eingabe | 4 | Int8, Uint8 |
| Bscaletensor | Eingabe | 4 | Float32 |
| Bzeropointtensor | Optionale Eingabe | 4 | Int8, Uint8 |
| Outputscaletensor | Eingabe | 4 | Float32 |
| Outputzeropointtensor | Optionale Eingabe | 4 | Int8, Uint8 |
| Outputtensor | Ausgabe | 4 | Int8, Uint8 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |