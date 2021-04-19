---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Gibt Elemente aus der Quell-zum Ziel Mandanten erneut aus, wobei die Skalierungsfaktoren verwendet werden, um die Ziel-tensorflow-Größe zu berechnen. Sie können einen linearen oder nächstgelegenen Interpolations Modus verwenden.
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
ms.openlocfilehash: 669e828c4d8376e081ef6638aba4a13d517afd88
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106366539"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a>DML_RESAMPLE1_OPERATOR_DESC-Struktur (directml. h)
Gibt Elemente aus der Quell-zum Ziel Mandanten erneut aus, wobei die Skalierungsfaktoren verwendet werden, um die Ziel-tensorflow-Größe zu berechnen. Sie können einen linearen oder nächstgelegenen Interpolations Modus verwenden. Der-Operator unterstützt Interpolationen über mehrere Dimensionen, nicht nur über 2D. Sie können also die gleiche räumliche Größe beibehalten, aber über Kanäle oder Batches hinweg interpolieren. Die Beziehung zwischen der Eingabe-und der Ausgabe Koordinate lautet wie folgt:

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der tensorflow, der die Eingabedaten enthält.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der tensorflow, in den die Ausgabedaten geschrieben werden sollen.


`InterpolationMode`

Typ: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Dieses Feld bestimmt die Art der Interpolations, mit der Ausgabe Pixel ausgewählt werden.

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**. Verwendet den *nächstgelegenen Nachbar* Algorithmus, der das Eingabe Element auswählt, das dem entsprechenden Pixel Center für jedes Output-Element am nächsten ist.

- **DML_INTERPOLATION_MODE_LINEAR**. Verwendet den *vierlinear* -Algorithmus, der das Output-Element berechnet, indem der gewichtete Durchschnitt der zwei nächstgelegenen benachbarten Eingabeelemente pro Dimension ausgeführt wird. Da alle vier Dimensionen neu erstellt werden können, wird der gewichtete Durchschnitt für jedes Output-Element für insgesamt 16 Eingabeelemente berechnet.


`DimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Werte in den Arrays, die *skaliert*, *inputpixeloffsets* und *outputpixeloffsets* auf zeigen. Dieser Wert muss mit der Dimensions Anzahl von *inputtensor* und *outputtensor* identisch sein, die 4 sein muss.


`Scales`

Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***

Die Skalierungen, die beim erneuten Sampling der Eingabe angewendet werden, wobei Skalierung > 1 das Image zentral hochskalieren und Skalieren < 1 skalieren Sie das Bild für diese Dimension herunter. Beachten Sie, dass die Skalen nicht exakt sein müssen `OutputSize / InputSize` . Wenn die Eingabe nach der Skalierung größer als die Ausgabe Grenze ist, wird Sie in die Ausgabegröße übertragen. Wenn die Eingabe nach der Skalierung jedoch kleiner als die Ausgabe Grenze ist, werden die Ausgabe Kanten geklammert.


`InputPixelOffsets`

Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***

Die Offsets, die vor dem erneuten Sampling auf die Eingabe Pixel angewendet werden sollen. Wenn dieser Wert ist `0` , wird die linke obere Ecke des Pixels anstelle der Mitte verwendet, die in der Regel nicht das erwartete Ergebnis liefert. Um das Bild mithilfe der Mitte der Pixel neu zu formatieren und das gleiche Verhalten wie [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)zu erzielen, muss dieser Wert lauten `0.5` .


`OutputPixelOffsets`

Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***

Die Offsets, die nach dem erneuten Sampling auf die Ausgabe Pixel angewendet werden sollen. Wenn dieser Wert ist `0` , wird die linke obere Ecke des Pixels anstelle der Mitte verwendet, die in der Regel nicht das erwartete Ergebnis liefert. Um das Bild mithilfe der Mitte der Pixel neu zu formatieren und das gleiche Verhalten wie [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)zu erzielen, muss dieser Wert lauten `-0.5` .


## <a name="remarks"></a>Bemerkungen
Wenn *inputpixeloffsets* auf 0,5 und *outputpixeloffsets* auf-0,5 festgelegt sind, entspricht dieser Operator [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*Inputtensor* und *outputtensor* müssen denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 | Float32, FLOAT16 |
| Outputtensor | Ausgabe | 4 | Float32, FLOAT16 |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |