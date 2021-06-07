---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Führt eine Matrixmultiplikationsfunktion für ganzzahlige Daten aus.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417603"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC -Struktur (directml.h)
Führt eine Matrixmultiplikationsfunktion für ganzzahlige Daten aus.

Für diesen Operator müssen die Matrix-Multiplikationseingabetensoren 4D sein, die als formatiert `{ BatchCount, ChannelCount, Height, Width }` sind. Der Matrixmultiplikationsoperator führt BatchCount * ChannelCount number of independent matrix multiplications (Anzahl unabhängiger Matrixmultiplikationen) aus.

Wenn *ATensor* beispielsweise  über Größen von verfügt und BTensor über Größen von verfügt und OutputTensor größen von hat, führt der Matrixmultiplikationsoperator batchCount * ChannelCount unabhängige Matrixmultiplikationen von Dimensionen `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N} aus.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Member

`ATensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die A-Daten enthält. Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, M, K }` sein.


`AZeroPointTensor`

Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die ATensor-Nullpunktdaten enthält. Die erwarteten Dimensionen von sind `AZeroPointTensor` , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine Quantisierung pro Zeile `{ 1, 1, 1, 1 }` `{ 1, 1, M, 1 }` erforderlich ist. Diese Nullpunktwerte werden zum Dequantisieren der *ATensor-Werte* verwendet.


`BTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die B-Daten enthält. Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, K, N }` sein.


`BZeroPointTensor`

Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die *BTensor-Nullpunktdaten* enthält. Die erwarteten Dimensionen von sind `BZeroPointTensor` , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine `{ 1, 1, 1, 1 }` Quantisierung pro Spalte erforderlich `{ 1, 1, 1, N }` ist. Diese Nullpunktwerte werden zum Dequantisieren der BTensor-Werte verwendet.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, in den die Ergebnisse geschrieben werden. Die Dimensionen dieses Tensors sind `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *ATensor und* `AZeroPointTensor` müssen den gleichen Datentyp *haben.*
* *BTensor* und `BZeroPointTensor` müssen den gleichen Datentyp *haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Dimensionen | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| ATensor | Eingabe | { BatchCount, ChannelCount, M, K } | 4 | INT8, UINT8 |
| AZeroPointTensor | Optionale Eingabe | { 1, 1, AZeroPointCount, 1 } | 4 | INT8, UINT8 |
| BTensor | Eingabe | { BatchCount, ChannelCount, K, N } | 4 | INT8, UINT8 |
| BZeroPointTensor | Optionale Eingabe | { 1, 1, 1, BZeroPointCount } | 4 | INT8, UINT8 |
| OutputTensor | Ausgabe | { BatchCount, ChannelCount, M, N } | 4 | INT32 |



## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |