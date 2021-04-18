---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
description: Führt eine logische linke Schicht der einzelnen Elemente des *atensor* durch eine Anzahl von Bits aus, die vom entsprechenden *btensor*-Element angegeben werden, und platziert das Ergebnis in das entsprechende Element von *outputtensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_left_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
ms.openlocfilehash: 24f58a5c235b6d67ca2dee712398dacc828d8f51
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106371814"
---
# <a name="dml_element_wise_bit_shift_left_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC-Struktur (directml. h)

Führt eine logische linke Schicht der einzelnen Elemente des *atensor* durch eine Anzahl von Bits aus, die vom entsprechenden *btensor*-Element angegeben werden, und platziert das Ergebnis in das entsprechende Element von *outputtensor*.

```
f(a, b) = (a << b)
```

Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass *outputtensor* bei der Bindung eine der Eingabe-Tensoren Alias zulässt.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Member

`ATensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Links neben Eingaben enthält.


`BTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Eingaben auf der rechten Seite enthält.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*Atensor*, *btensor* und *outputtensor* müssen denselben *Datentyp*, jede *DimensionCount* und jede *Größe* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Atensor | Eingabe | 1 bis 8 | UInt32, UInt16, Uint8 |
| Btensor | Eingabe | 1 bis 8 | UInt32, UInt16, Uint8 |
| Outputtensor | Ausgabe | 1 bis 8 | UInt32, UInt16, Uint8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Atensor | Eingabe | 4 | UInt32, UInt16, Uint8 |
| Btensor | Eingabe | 4 | UInt32, UInt16, Uint8 |
| Outputtensor | Ausgabe | 4 | UInt32, UInt16, Uint8 |



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |