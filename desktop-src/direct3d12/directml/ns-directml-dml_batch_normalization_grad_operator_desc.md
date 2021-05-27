---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Berechnet Backpropagation-Farbverläufe für [die Batchnormalisierung.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550435"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a>DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)

Berechnet Backpropagation-Farbverläufe für [die Batchnormalisierung.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) **DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** führt mehrere Berechnungen aus, die in den separaten Ausgabebeschreibungen beschrieben werden.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Eingabedaten enthält. Dies ist in der Regel derselbe Tensor, der als *InputTensor* für [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) im Vorwärtsdurchlauf bereitgestellt wurde.

`InputGradientTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingehende Farbverlaufs-Tensor. Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorangehenden Ebene abgerufen. Dieser Tensor muss die gleichen Dimensionsgrößen wie *InputTensor aufweisen.*

`MeanTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die mittleren Daten enthält. Dies ist in der Regel derselbe Tensor, der als *MeanTensor* für [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) im Vorwärtsdurchlauf bereitgestellt wurde.

Alle Dimensionen, die nicht die gleiche Größe wie die entsprechende Dimension von *InputTensor* haben, müssen eine Größe von 1 aufweisen, damit sie an die Eingabe gesendet werden können.

Beispielsweise sind die folgenden Größen akzeptabel.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

Im Folgenden wird ein Fehler angezeigt, da alle Dimensionen, die nicht übereinstimmen, größe 1 aufweisen müssen, um broadcastkompatibel zu sein.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Varianzdaten enthält. Dies ist in der Regel der gleiche Tensor, der als *VarianceTensor* bereitgestellt wurde, um DML_BATCH_NORMALIZATION_OPERATOR_DESC [**vorwärts**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) zu übergeben. Dieser Tensor muss die gleichen Dimensionsgrößen wie *MeanTensor aufweisen.*

`ScaleTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Skalierungsdaten enthält. Dies ist in der Regel der gleiche Tensor, der als *ScaleTensor* bereitgestellt wurde, um DML_BATCH_NORMALIZATION_OPERATOR_DESC [**Vorwärtspass**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) zu verwenden. Dieser Tensor muss die gleichen Dimensionsgrößen wie *MeanTensor aufweisen.*

`OutputGradientTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Für jeden entsprechenden Wert in den Eingaben ist `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .

Dieser Tensor muss die gleichen Dimensionsgrößen wie *InputTensor* / *InputGradientTensor aufweisen.*

`OutputScaleGradientTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Dieser Tensor muss die gleichen Dimensionsgrößen wie *MeanTensor* / *VarianceTensor* / *ScaleTensor' aufweisen.*

Die folgende Berechnung erfolgt oder jeder entsprechende Wert in den Eingaben.

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

Die `sum` wird für alle Dimensionen berechnet, die übertragen werden müssen. Wenn keine Übertragung erforderlich ist, ist keine Summe erforderlich.

Hier ist ein Beispiel.

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

Das Element [0, **0**, 0, 0] von ist die Summe aller `OutputScaleGradientTensor` `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` 90 (3 \* 5 \* 6) Elemente [[0,2], **0**, [0,4], [0,5]].

`OutputBiasGradientTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Dieser Tensor muss die gleichen Dimensionsgrößen wie *MeanTensor* / *VarianceTensor* / *ScaleTensor' aufweisen.*

Die folgende Berechnung erfolgt oder jeder entsprechende Wert in den Eingaben.

`OutputBiasGradient = sum(InputGradient)`  

Die `sum` wird für alle Dimensionen berechnet, die übertragen werden müssen (siehe Beispiel für *OutputScaleGradientTensor*). Wenn keine Übertragung erforderlich ist, ist keine Summe erforderlich.

`Epsilon`

Typ: **[FLOAT](../../winprog/windows-data-types.md)**

Ein kleiner Wert, der der Varianz hinzugefügt wird, um 0 (null) zu vermeiden.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*InputGradientTensor,* *InputTensor,* *MeanTensor,* *OutputBiasGradientTensor,* *OutputGradientTensor,* *OutputScaleGradientTensor,* *ScaleTensor* und *VarianceTensor* müssen den gleichen *Datentyp* und *DimensionCount* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| InputGradientTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| MeanTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| VarianceTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16 |
| OutputScaleGradientTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16 |
| OutputBiasGradientTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |