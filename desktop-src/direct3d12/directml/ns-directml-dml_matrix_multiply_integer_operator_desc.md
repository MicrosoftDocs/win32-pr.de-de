---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Führt eine Matrix Multiplikations Funktion für ganzzahlige Daten aus.
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
ms.openlocfilehash: f6ecccf49b0d7123e6f41321c7ba1bf8e8d4ad87
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351188"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC-Struktur (directml. h)
Führt eine Matrix Multiplikations Funktion für ganzzahlige Daten aus.

Dieser Operator erfordert, dass die Eingabe-Tensoren der Matrix als 4D-Wert vorliegen, die als formatiert sind `{ BatchCount, ChannelCount, Height, Width }` . Der Matrix Multiplikations Operator führt die BatchCount * ChannelCount-Anzahl unabhängiger Matrix Multiplikationen durch.

Wenn *atensor* z. b. *Größen* von hat `{ BatchCount, ChannelCount, M, K }` und *btensor* die *Größe* hat `{ BatchCount, ChannelCount, K, N }` und *outputtensor* über *Größen* von verfügt `{ BatchCount, ChannelCount, M, N }` , führt der Matrix Multiplikations Operator BatchCount * ChannelCount unabhängige Matrix Multiplikationen der Dimensionen {m, K} x {K, n} = {M, n} aus.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Daten enthält. Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, M, K }` .


`AZeroPointTensor`

Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Daten des atensor-NULL-Punkts enthält. Die erwarteten Dimensionen von `AZeroPointTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, M, 1 }` Wenn die pro-Zeilen-Quantifizierung erforderlich ist. Diese nullpunktwerte werden zum decomieren der *atensor* -Werte verwendet.


`BTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die B-Daten enthält. Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, K, N }` .


`BZeroPointTensor`

Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Daten des *btensor* -NULL-Punkts enthält. Die erwarteten Dimensionen von `BZeroPointTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, 1, N }` Wenn pro Spalten Quantifizierung erforderlich ist. Diese nullpunktwerte werden zum decomieren der btensor-Werte verwendet.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, in den die Ergebnisse geschrieben werden sollen. Die Dimensionen dieses Mandanten sind `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *Atensor* und `AZeroPointTensor` muss denselben *Datentyp* aufweisen.
* *Btensor* und `BZeroPointTensor` muss denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Dimensionen | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| Atensor | Eingabe | {BatchCount, ChannelCount, M, K} | 4 | Int8, Uint8 |
| Azeropointtensor | Optionale Eingabe | {1, 1, azeropointcount, 1} | 4 | Int8, Uint8 |
| Btensor | Eingabe | {BatchCount, ChannelCount, K, N} | 4 | Int8, Uint8 |
| Bzeropointtensor | Optionale Eingabe | {1, 1, 1, bzeropointcount} | 4 | Int8, Uint8 |
| Outputtensor | Ausgabe | {BatchCount, ChannelCount, M, N} | 4 | INT32 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |