---
UID: NS:directml.DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
description: Berechnet das bitweise NOT für jedes Element des Eingabe Mandanten und schreibt das Ergebnis in den Ausgabe Mandanten.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.openlocfilehash: bb42be1e1f00fcf749ed271d55a7958b43464f1a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106353247"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC-Struktur (directml. h)

Berechnet das bitweise NOT für jedes Element des Eingabe Mandanten und schreibt das Ergebnis in den Ausgabe Mandanten.

Der Eingabe-und Ausgabe Mandanten muss dieselbe *DimensionCount*, *Größe* und denselben *Datentyp* aufweisen.

Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass der ausgabetensor während der Bindung den Eingabe Mandanten als Alias zulässt.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingabetensor, aus dem gelesen wird.

`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.

## <a name="example"></a>Beispiel

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*Inputtensor* und *outputtensor* müssen denselben *Datentyp*, jede *DimensionCount* und jede *Größe* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 1 bis 8 | UInt32, UInt16, Uint8 |
| Outputtensor | Ausgabe | 1 bis 8 | UInt32, UInt16, Uint8 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |