---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Führt eine durchschnittliche Varianznormalisierungsfunktion für den Eingabe-Tensor aus. Dieser Operator berechnet den Mittelwert und die Varianz des Eingabe-Tensors, um eine Normalisierung durchzuführen.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: ae22b004f1e879eb020ddcfe39a5f26481a508b0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549776"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC-Struktur (directml.h)

Führt eine durchschnittliche Varianznormalisierungsfunktion für den Eingabe-Tensor aus. Dieser Operator berechnet den Mittelwert und die Varianz des Eingabe-Tensors, um eine Normalisierung durchzuführen. Dieser Operator führt die folgende Berechnung aus.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```
## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Eingabedaten enthält. Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, Height, Width }` sein.

`ScaleTensor`

Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Tensor, der die Skalierungsdaten enthält.

Wenn **DML_FEATURE_LEVEL** kleiner als **DML_FEATURE_LEVEL_4_0** ist, sollten die Dimensionen dieses Tensors `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` sein. Die Dimensionen ScaleBatchCount, ScaleHeight und ScaleWidth sollten entweder mit *InputTensor* übereinstimmen oder auf 1 festgelegt werden, um diese Dimensionen automatisch über die Eingabe zu übertragen.

Wenn **DML_FEATURE_LEVEL** größer oder gleich **DML_FEATURE_LEVEL_4_0** ist, kann jede Dimension auf 1 festgelegt und automatisch an *InputTensor* gesendet werden.

Dieser Tensor ist erforderlich, wenn *BiasTensor* verwendet wird.

`BiasTensor`

Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***


Ein optionaler Tensor, der die Bias-Daten enthält.

Wenn **DML_FEATURE_LEVEL** kleiner als **DML_FEATURE_LEVEL_4_0** ist, sollten die Dimensionen dieses Tensors `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` sein. Die Dimensionen BiasBatchCount, BiasHeight und BiasWidth sollten entweder *mit InputTensor* übereinstimmen oder auf 1 festgelegt werden, um diese Dimensionen automatisch über die Eingabe zu übertragen.

Wenn **DML_FEATURE_LEVEL** größer oder gleich DML_FEATURE_LEVEL_4_0 **ist,** kann jede Dimension auf 1 festgelegt und automatisch an *InputTensor übertragen werden.*

Dieser Tensor ist erforderlich, wenn *der ScaleTensor* verwendet wird.

`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, in den die Ergebnisse geschrieben werden. Die Dimensionen dieses Tensors sind `{ BatchCount, ChannelCount, Height, Width }` .

`AxisCount`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

Die Anzahl der Achsen. Dieses Feld bestimmt die Größe des *Achsenarrays.*

`Axes`

Typ: \_ \_ Feldgröße \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \*** 

Die Achsen, auf denen der Mittelwert und die Varianz berechnet werden.

`NormalizeVariance`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

**TRUE,** wenn die Normalisierungsebene Varianz in der Normalisierungsberechnung enthält. Andernfalls **FALSE.** False **gibt an,** dass die Normalisierungsgleichung `Output = FusedActivation(Scale * (Input - Mean) + Bias)` ist.

`Epsilon`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Der epsilon-Wert, der verwendet werden soll, um eine Division durch 0 (null) zu vermeiden. Als Standardwert wird der Wert 0,00001 empfohlen.

`FusedActivation`

Typ: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Eine optionale fused-Aktivierungsebene, die nach der Normalisierung angewendet werden soll.

## <a name="remarks"></a>Hinweise
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** ist eine Obermenge der Funktionalität [von DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). Hier entspricht  das Festlegen des Axes-Arrays auf `{ 0, 2, 3 }` dem Festlegen von *CrossChannel* auf **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**. Das Festlegen des **Axes-Arrays** auf entspricht dem `{ 1, 2, 3 }` Festlegen von *CrossChannel* auf **TRUE.**

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen

*BiasTensor,* *InputTensor,* *OutputTensor* und *ScaleTensor* müssen den gleichen *DataType* und *DimensionCount* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 und höher

| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Optionale Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| BiasTensor | Optionale Eingabe | 1 bis 8 | FLOAT32, FLOAT16 |
| OutputTensor | Ausgabe | 1 bis 8 | FLOAT32, FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher

| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Optionale Eingabe | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Optionale Eingabe | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Ausgabe | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Siehe auch

[Verwenden von Fused-Operatoren zur Verbesserung der Leistung](../dml-fused-activations.md)