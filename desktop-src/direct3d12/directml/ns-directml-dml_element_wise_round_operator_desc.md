---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Rundet jedes Element von " *inputtensor* " auf einen ganzzahligen Wert, wobei das Ergebnis in das entsprechende Element von " *outputtensor*" platziert wird.
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
ms.openlocfilehash: f0964ae133c61b3a596b644630d363f902635585
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361740"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_ROUND_OPERATOR_DESC-Struktur (directml. h)

Rundet jedes Element von " *inputtensor* " auf einen ganzzahligen Wert, wobei das Ergebnis in das entsprechende Element von " *outputtensor*" platziert wird.

Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass *outputtensor* während der Bindung den Alias *inputtensor* zulässt.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingabetensor, aus dem gelesen wird.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.


`RoundingMode`

Typ: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**

Eine [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) die die Richtung bestimmt, zu der abgerundet werden soll.

* Wenn **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**:-Werte auf die nächste ganze Zahl gerundet werden, wobei die Hälfte der Werte (z. b. 0,5) auf die nächste gerade ganze Zahl gerundet wird.
* , Wenn **DML_ROUNDING_MODE_TOWARD_ZERO**:-Werte in Richtung NULL gerundet werden. Dadurch wird der Bruchteile effektiv abgeschnitten.
* Wenn **DML_ROUNDING_MODE_TOWARD_INFINITY**:-Werte auf die nächste ganze Zahl gerundet werden, wobei die Hälfte der Werte (z. b. 0,5) von 0 (null) gerundet wird (in Richtung positiv oder minus unendlich, je nach Vorzeichen des Werts).

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*Inputtensor* und *outputtensor* müssen denselben *Datentyp*, jede *DimensionCount* und jede *Größe* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 1 bis 8 | Float32, FLOAT16 |
| Outputtensor | Ausgabe | 1 bis 8 | Float32, FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 | Float32, FLOAT16 |
| Outputtensor | Ausgabe | 4 | Float32, FLOAT16 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |