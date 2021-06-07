---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Überprüft jedes Element von *InputTensor* je nach dem angegebenen *InfinityMode* auf IEEE-754 -inf, inf oder beides und platziert das Ergebnis (1 für true, 0 für false) in das entsprechende Element von *OutputTensor.*
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417722"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC -Struktur (directml.h)

Überprüft jedes Element von *InputTensor* je nach dem angegebenen *InfinityMode* auf IEEE-754 -inf, inf oder beides und platziert das Ergebnis (1 für true, 0 für false) in das entsprechende Element von *OutputTensor.*

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Eingabetensor, aus dem gelesen werden soll.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe tensor, in den die Ergebnisse geschrieben werden.


`InfinityMode`

Typ: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**

Ein [DML_IS_INFINITY_MODE,](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) der das Vorzeichen der Unendlichkeit bestimmt, auf die überprüft werden soll.

* Wenn **DML_IS_INFINITY_MODE_EITHER,** wird 1 zurückgegeben, wenn das Element -inf oder inf ist, andernfalls 0.
* Wenn **DML_IS_INFINITY_MODE_POSITIVE,** wird 1 zurückgegeben, wenn das Element inf ist, andernfalls 0.
* Wenn **DML_IS_INFINITY_MODE_NEGATIVE** ist, wird 1 zurückgegeben, wenn das Element -inf ist, andernfalls 0.


## <a name="remarks"></a>Hinweise
## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*InputTensor und* *OutputTensor* müssen über die gleichen *DimensionCount-* und *Sizes-Größen verfügen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| OutputTensor | Ausgabe | 1 bis 8 | UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Ausgabe | 4 | UINT8 |


## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Version 2004 (10.0; Build 19041) |
| **Unterstützte Mindestversion (Server)** | Windows Server, Version 2004 (10.0; Build 19041) |
| **Header** | directml.h |