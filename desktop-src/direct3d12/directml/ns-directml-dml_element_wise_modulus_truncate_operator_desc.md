---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
description: Berechnet den C-Modulusoperator für jedes Paar der entsprechenden Elemente der Eingabe tensors und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_truncate_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
ms.openlocfilehash: 461a7882e17d86b25cf27e0a28c05673f8899cea
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417616"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC-Struktur (directml.h)

Berechnet den C-Modulusoperator für jedes Paar der entsprechenden Elemente der Eingabe tensors und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*

Da der Quotient auf 0 gerundet wird, hat das Ergebnis das gleiche Vorzeichen wie der Dividend.

```
f(a, b) = a - (b * trunc(a / b))
```

Dieser Operator unterstützt die direkt ausgeführte Ausführung, d. h., *OutputTensor* darf während der Bindung einen der Eingabe-Tensoren mit einem Alias verbinden.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Member

`ATensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die linken Eingaben enthält.


`BTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die rechten Eingaben enthält.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*ATensor,* *BTensor* und *OutputTensor* müssen die gleichen *Datentypen*, *DimensionCount* und *Größen* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| BTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Eingabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| BTensor | Eingabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Ausgabe | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |