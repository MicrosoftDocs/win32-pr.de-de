---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Rundet jedes Element von *InputTensor* auf einen ganzzahligen Wert und platziert das Ergebnis im entsprechenden Element von *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure
- direct3d12.dml_element_wise_round_operator_desc
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.openlocfilehash: cb9414d0c3e628fa95784480c7402b242d12095b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417855"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_ROUND_OPERATOR_DESC -Struktur (directml.h)

Rundet jedes Element von *InputTensor* auf einen ganzzahligen Wert und platziert das Ergebnis im entsprechenden Element von *OutputTensor*.

Dieser Operator unterstützt die ausführungsbasierte Ausführung, was bedeutet, dass *OutputTensor* während der Bindung einen *Alias für InputTensor* verwenden darf.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Eingabetensor, aus dem gelesen werden soll.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe tensor, in den die Ergebnisse geschrieben werden.


`RoundingMode`

Typ: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**

Ein [DML_ROUNDING_MODE,](/windows/win32/api/directml/ne-directml-dml_rounding_mode) der die Richtung bestimmt, auf die gerundet werden soll.

* Wenn **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN:** Werte werden auf die nächste ganze Zahl gerundet, und die Hälftenwerte (z. B. 0,5) werden auf die nächste gerade ganze Zahl gerundet.
* Wenn **DML_ROUNDING_MODE_TOWARD_ZERO:** Werte werden auf Null gerundet. Dadurch wird der Bruchteil effektiv abgeschnitten.
* Wenn **DML_ROUNDING_MODE_TOWARD_INFINITY:** Werte werden auf die nächste ganze Zahl gerundet, und die Hälftenwerte (z. B. 0,5) werden von 0 (in Richtung positiv oder negativ unendlich, je nach Vorzeichen des Werts) gerundet.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*InputTensor und* *OutputTensor* müssen denselben *DataType,* *DimensionCount* und *die gleichen Größen aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| OutputTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Ausgabe | 4 | FLOAT32, FLOAT16 |



## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |