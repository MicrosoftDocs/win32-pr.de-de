---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Berechnet Backpropagation-Farbverläufe für Resample (siehe [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
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
ms.openlocfilehash: 0caba1a560b72a94ed04cacd824414964af82c35
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804053"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>DML_RESAMPLE_GRAD_OPERATOR_DESC-Struktur (directml.h)

Berechnet Backpropagation-Farbverläufe für Resample (siehe [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).

**DML_RESAMPLE1_OPERATOR_DESC** skaliert beliebige Dimensionen des Eingabe-Tensors mithilfe von Nearest-Neighbor-Sampling oder bilinearer Interpolation neu. Bei einem *InputGradientTensor* mit denselben Größen wie die *Ausgabe* eines entsprechenden **DML_RESAMPLE1_OPERATOR_DESC** erzeugt dieser Operator einen *OutputGradientTensor* mit den gleichen Größen wie die *Eingabe* des **DML_RESAMPLE1_OPERATOR_DESC**.

Betrachten Sie beispielsweise eine **DML_RESAMPLE1_OPERATOR_DESC,** die eine nächsthöheren Nachbarskalierung von 1,5x in der Breite und 0,5x in der Höhe ausführt.

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

Beachten Sie, dass das 0. Element des Eingabe-Tensors (mit dem Wert 1) zu zwei Elementen in der Ausgabe beiträgt, das erste Element (mit dem Wert 2) zu einem Element in der Ausgabe und das zweite und dritte Element (mit den Werten 3 und 4) zu keinen Elementen der Ausgabe beitragen.

Der entsprechende **DML_RESAMPLE_GRAD_OPERATOR_DESC** würde Folgendes ausführen.

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

Beachten Sie, dass die Werte im *OutputGradientTensor* die gewichteten Beiträge dieses Elements zum *OutputTensor* während des ursprünglichen **DML_RESAMPLE1_OPERATOR_DESC-Operators** darstellen.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

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

Der eingehende Farbverlaufs-Tensor. Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorangehenden Ebene abgerufen. In der Regel hat dieser Tensor die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) im Vorwärtsdurchlauf.

`OutputGradientTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe-Tensor, der die Zurückpropagierten Farbverläufe enthält. In der Regel hat dieser Tensor  die gleichen Größen wie die Eingabe des entsprechenden DML_RESAMPLE1_OPERATOR_DESC [im](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) Vorwärtspass.

`InterpolationMode`

Typ: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Weitere Informationen *finden Sie unter InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`DimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Elemente in den *Arrays Scales,* *InputPixelOffsets* und *OutputPixelOffsets.* Dieser Wert muss dem *DimensionCount-Wert in* *InputGradientTensor* und *OutputGradientTensor entspricht.*

`Scales`

Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***

Weitere Informationen finden Sie unter *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`InputPixelOffsets`

Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***

Weitere Informationen finden Sie unter *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`OutputPixelOffsets`

Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***

Weitere Informationen finden Sie unter *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*InputGradientTensor und* *OutputGradientTensor* müssen denselben *Datentyp haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Eingabe | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Ausgabe | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |