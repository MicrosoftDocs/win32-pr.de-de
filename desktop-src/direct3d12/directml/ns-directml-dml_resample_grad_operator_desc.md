---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Berechnet Rückeigenschaftenverläufe für Resample (siehe [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: ff2660257fa619edb72f10efb419f3c15f43fbde
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549725"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>DML_RESAMPLE_GRAD_OPERATOR_DESC -Struktur (directml.h)

Berechnet Rückeigenschaftenverläufe für Resample (siehe [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).

**DML_RESAMPLE1_OPERATOR_DESC** skaliert beliebige Dimensionen des Eingabetensors entweder mithilfe der Nächsten-Nachbar-Stichprobenentnahme oder der bilinealen Interpolation neu. Bei einem *InputGradientTensor* mit den  gleichen Größen wie die Ausgabe einer entsprechenden **DML_RESAMPLE1_OPERATOR_DESC** erzeugt dieser Operator einen *OutputGradientTensor* mit den gleichen Größen wie die **Eingabe DML_RESAMPLE1_OPERATOR_DESC**. 

Betrachten Sie als  Beispiel eine DML_RESAMPLE1_OPERATOR_DESC, die eine nächste Nachbarskalierung von 1,5-facher Breite und 0,5-facher Höhe ausführt.

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

Beachten Sie, dass das 0. Element des Eingabetensors (mit dem Wert 1) zu zwei Elementen in der Ausgabe beiträgt, das erste Element (mit dem Wert 2) zu einem Element in der Ausgabe beiträgt und das 2. und das dritte Element (mit den Werten 3 und 4) zu keinen Elementen der Ausgabe beitragen.

Die entsprechende **DML_RESAMPLE_GRAD_OPERATOR_DESC** würde Folgendes ausführen.

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

Beachten Sie, dass die Werte im *OutputGradientTensor* die gewichteten Beiträge dieses Elements zum *OutputTensor* während des ursprünglichen DML_RESAMPLE1_OPERATOR_DESC **darstellen.**

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a>Member

`InputGradientTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingehende Farbverlaufs-Tensor. Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorherigen Ebene ermittelt. In der Regel hat dieser Tensor  die gleichen Größen wie die Ausgabe des entsprechenden DML_RESAMPLE1_OPERATOR_DESC [im](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) Vorwärtspass.

`OutputGradientTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe tensor, der die zurückpropagierten Farbverläufe enthält. In der Regel hat dieser Tensor die gleichen Größen wie die *Eingabe* der entsprechenden [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) im Vorwärtsdurchlauf.

`InterpolationMode`

Typ: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Weitere Informationen finden Sie unter *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`DimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Elemente in den *Arrays Scales,* *InputPixelOffsets* und *OutputPixelOffsets.* Dieser Wert muss gleich dem *DimensionCount-Wert* sein, der in *InputGradientTensor* und *OutputGradientTensor* bereitgestellt wird.

`Scales`

Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Weitere Informationen finden Sie unter *Skalierungen* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`InputPixelOffsets`

Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Weitere Informationen finden Sie unter *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`OutputPixelOffsets`

Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Weitere Informationen finden Sie unter *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*InputGradientTensor* und *OutputGradientTensor* müssen den gleichen *Datentyp aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Eingabe | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Ausgabe | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |