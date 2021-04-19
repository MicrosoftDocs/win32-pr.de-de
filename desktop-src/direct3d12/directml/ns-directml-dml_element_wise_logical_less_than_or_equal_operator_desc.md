---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
description: Führt einen logischen *kleiner-als-oder gleich* -Wert für jedes Paar entsprechender Elemente der Eingabe-Tensoren aus, wobei das Ergebnis (1 für true, 0 für false) in das entsprechende Element von *outputtensor* gestellt wird.
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: 815c7ea148d6754cb410da6aeedaf31ab6cd7ece
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106349755"
---
# <a name="dml_element_wise_logical_less_than_or_equal_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC-Struktur (directml. h)

Führt einen logischen *kleiner-als-oder gleich* -Wert für jedes Paar entsprechender Elemente der Eingabe-Tensoren aus, wobei das Ergebnis (1 für true, 0 für false) in das entsprechende Element von *outputtensor* gestellt wird.

```
f(a, b) = (a <= b)
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax

```cpp
struct DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
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
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *Atensor* und *btensor* müssen denselben *Datentyp* aufweisen.
* *Atensor*, *btensor* und *outputtensor* müssen die gleiche *DimensionCount* und *Größe* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Atensor | Eingabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Btensor | Eingabe | 1 bis 8 | Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8 |
| Outputtensor | Ausgabe | 1 bis 8 | UInt32, Uint8 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |