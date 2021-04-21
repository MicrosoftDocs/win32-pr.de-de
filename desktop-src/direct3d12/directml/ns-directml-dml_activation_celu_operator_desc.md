---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Führt die AKTIVIERUNGsfunktion der kontinuierlich differenzierbaren exponentiellen linearen Einheit (EXPONENTIAL Linear Unit, CELU) für jedes Element in *InputTensor* aus und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*
helpviewer_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- DML_ACTIVATION_CELU_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_CELU_OPERATOR_DESC, DML_ACTIVATION_CELU_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
ms.openlocfilehash: b6497e995601d7e9e01696f39920672674be07c4
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803730"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a>DML_ACTIVATION_CELU_OPERATOR_DESC-Struktur (directml.h)

Führt die AKTIVIERUNGsfunktion der kontinuierlich differenzierbaren exponentiellen linearen Einheit (EXPONENTIAL Linear Unit, CELU) für jedes Element in *InputTensor* aus und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

Hierbei gilt:
* exp(x) ist die funktion "natural exponentiation"
* max(a,b) gibt den größeren der beiden Werte a,b zurück.
* min(a,b) gibt den kleineren der beiden Werte a,b zurück.

Dieser Operator unterstützt die direkt ausgeführte Ausführung, was bedeutet, dass der Ausgabe-Tensor während der Bindung den Alias *InputTensor* aliasen darf.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Eingabe-Tensor, aus dem gelesen werden soll.

`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.

`Alpha`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Der Alphakoeffizienten. Ein typischer Standardwert für diesen Wert ist 1,0.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*InputTensor* und *OutputTensor* müssen die gleichen *Datentypen*, *DimensionCount* und *Größen* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| OutputTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |