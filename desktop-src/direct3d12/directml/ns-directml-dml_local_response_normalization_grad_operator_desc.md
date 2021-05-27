---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Berechnet Rückeigenschaftenverläufe für die [lokale Antwortnormalisierung.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: e858b8ce20df4b1bf12ac9efe360941eb93c54d1
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550405"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a>DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)

Berechnet Rückeigenschaftenverläufe für die [lokale Antwortnormalisierung.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)

Der Datentyp und die Größe aller Tensoren müssen identisch sein.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, der die Eingabedaten enthält. Die Größen dieses Tensors *sollten* `{ BatchCount, ChannelCount, Height, Width }` sein.

`InputGradientTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingehende Farbverlaufs-Tensor. Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorherigen Ebene ermittelt.

`OutputGradientTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe tensor, der die zurückpropagierten Farbverläufe enthält.

`CrossChannel`

Typ: **[BOOL](../../winprog/windows-data-types.md)**

**TRUE,** wenn die LRN-Schicht kanalübergreifend summiert wird; **FALSE,** wenn die LRN-Schicht über räumliche Dimensionen summiert wird.

`LocalSize`

Typ: **[UINT](../../winprog/windows-data-types.md)**

Die maximale Anzahl von Elementen, die pro Dimension summiert werden sollen (der lokale Bereich wird abgeschnitten, sodass sich alle Elemente innerhalb der Grenzen befinden). Wenn *CrossChannel* **true ist,** ist dies die Breite und Höhe des lokalen Bereichs. Wenn *CrossChannel* **FALSE ist,** ist dies die Anzahl der Elemente in der lokalen Region. Dieser Wert muss mindestens 1 sein.

`Alpha`

Typ: **[FLOAT](../../winprog/windows-data-types.md)**

Der Wert des Skalierungsparameters. Es wird empfohlen, den Standardwert 0,0001 zu haben.

`Beta`

Typ: **[FLOAT](../../winprog/windows-data-types.md)**

Der Wert des Exponenten. Der Standardwert ist 0,75.

`Bias`

Typ: **[FLOAT](../../winprog/windows-data-types.md)**

Der Wert von Bias. Es wird empfohlen, standardmäßig den Wert 1 zu nutzen.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*InputGradientTensor,* *InputTensor* und *OutputGradientTensor* müssen den gleichen *Datentyp* und die gleichen *Größen* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16 |
| InputGradientTensor | Eingabe | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Ausgabe | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |