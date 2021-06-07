---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Resamples von Elementen von der Quelle zum Ziel-Tensor unter Verwendung der Skalierungsfaktoren zum Berechnen der Ziel-Tensorgröße. Sie können einen linearen oder nächsten Nachbarinterpolationsmodus verwenden.
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 3cf5a49f5c92b835646e146b631abd18b4b19e6b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417802"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a>DML_RESAMPLE1_OPERATOR_DESC-Struktur (directml.h)
Resamples von Elementen von der Quelle zum Ziel-Tensor unter Verwendung der Skalierungsfaktoren zum Berechnen der Ziel-Tensorgröße. Sie können einen linearen oder nächsten Nachbarinterpolationsmodus verwenden. Der -Operator unterstützt die Interpolation über mehrere Dimensionen hinweg, nicht nur 2D. Sie können also die gleiche räumliche Größe beibehalten, aber über Kanäle oder Batches hinweg interpolieren. Die Beziehung zwischen den Eingabe- und Ausgabekoordinaten lautet wie folgt.

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, der die Eingabedaten enthält.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der Tensor, in den die Ausgabedaten geschrieben werden sollen.


`InterpolationMode`

Typ: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Dieses Feld bestimmt die Art der Interpolation, die zum Auswählen von Ausgabepixeln verwendet wird.

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**. Verwendet den *Nearest* Neighbor-Algorithmus, mit dem das Eingabeelement ausgewählt wird, das dem entsprechenden Pixelmittelpunkt für jedes Ausgabeelement am nächsten ist.

- **DML_INTERPOLATION_MODE_LINEAR**. Verwendet den *Quadrilinear-Algorithmus,* der das Ausgabeelement berechnet, indem der gewichtete Durchschnitt der 2 nächsten benachbarten Eingabeelemente pro Dimension durchgeführt wird. Da alle vier Dimensionen neu formatiert werden können, wird der gewichtete Durchschnitt auf insgesamt 16 Eingabeelementen für jedes Ausgabeelement berechnet.


`DimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Werte in den Arrays, auf die *Scales*, *InputPixelOffsets* und *OutputPixelOffsets* zeigen. Dieser Wert muss mit der Dimensionsanzahl von *InputTensor* und *OutputTensor* übereinstimmen, die 4 sein muss.


`Scales`

Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Die beim Resampling der Eingabe zu übernehmenden Skalierungen, wobei > 1 das Bild hochskaliert und < 1 das Bild für diese Dimension herunterskaliert. Beachten Sie, dass die Skalierungen nicht genau sein `OutputSize / InputSize` müssen. Wenn die Eingabe nach der Skalierung größer als die Ausgabegrenze ist, wird sie auf die Ausgabegröße zugeschnitten. Wenn die Eingabe nach der Skalierung jedoch kleiner als die Ausgabegrenze ist, werden die Ausgaberänder gebunden.


`InputPixelOffsets`

Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Die Offsets, die vor dem Resampling auf die Eingabepixel angewendet werden sollen. Wenn dieser Wert `0` ist, wird die obere linke Ecke des Pixels anstelle der Mitte verwendet, was normalerweise nicht das erwartete Ergebnis ergibt. Um das Bild mithilfe der Mitte der Pixel neu zusamplemieren und das gleiche Verhalten wie [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)zu erhalten, muss dieser Wert `0.5` sein.


`OutputPixelOffsets`

Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Die Offsets, die nach dem Resampling auf die Ausgabepixel angewendet werden sollen. Wenn dieser Wert `0` ist, wird die obere linke Ecke des Pixels anstelle der Mitte verwendet, was normalerweise nicht das erwartete Ergebnis ergibt. Um das Bild mithilfe der Mitte der Pixel neu zusamplemieren und das gleiche Verhalten wie [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)zu erhalten, muss dieser Wert `-0.5` sein.


## <a name="remarks"></a>Hinweise
Wenn *inputPixelOffsets* auf 0,5 und *OutputPixelOffsets* auf -0,5 festgelegt sind, entspricht dieser Operator [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Ausgabe | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |