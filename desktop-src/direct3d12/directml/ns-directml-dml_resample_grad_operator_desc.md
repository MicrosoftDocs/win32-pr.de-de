---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Berechnet backpropagierungs Gradienten für Resample (siehe [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
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
ms.openlocfilehash: 5808381f2e812ac20399b46672e51acd063bc6a5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351832"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>DML_RESAMPLE_GRAD_OPERATOR_DESC-Struktur (directml. h)

Berechnet backpropagierungs Gradienten für Resample (siehe [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).

**DML_RESAMPLE1_OPERATOR_DESC** beliebige Dimensionen des Eingabe Mandanten mithilfe von "Next-Neighbor"-Stichproben oder der bilinearen Interpolations Option neu. Wenn ein *inputgradienttensor* mit denselben Größen wie die *Ausgabe* eines äquivalenten **DML_RESAMPLE1_OPERATOR_DESC** angegeben wird, erzeugt dieser Operator einen *outputgradienttensor* mit denselben Größen wie die *Eingabe* des **DML_RESAMPLE1_OPERATOR_DESC**.

Nehmen Sie als Beispiel eine **DML_RESAMPLE1_OPERATOR_DESC** , die eine Skalierung mit dem nächstgelegenen Nachbar Wert von 1,5 x in der Breite und 0,5 x in der Höhe ausführt.

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

Beachten Sie, dass das nullten-Element des Eingabe Mandanten (mit Wert 1) zu zwei Elementen in der Ausgabe beiträgt, das erste Element (mit Wert 2) zu einem Element in der Ausgabe beiträgt und das 2. und dritte Element (mit den Werten 3 und 4) zu keinen Elementen der Ausgabe beiträgt.

Die entsprechende **DML_RESAMPLE_GRAD_OPERATOR_DESC** würde Folgendes ausführen:

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

Beachten Sie, dass die Werte im *outputgradienttensor* die gewichteten Beiträge dieses Elements für *outputtensor* während des ursprünglichen **DML_RESAMPLE1_OPERATOR_DESC** Operators darstellen.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Der eingehende gradiententensor. Dies wird in der Regel aus der Ausgabe der Rück Propagierung einer vorangehenden Ebene abgerufen. In der Regel hat dieser tensorflow die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) im Forward-Durchlauf.

`OutputGradientTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe Mandanten, der die zurückgegebenen Farbverläufe enthält. In der Regel hat dieser Mandanten die gleichen Größen wie die *Eingabe* der entsprechenden [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) im Forward-Durchlauf.

`InterpolationMode`

Typ: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Siehe *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`DimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Elemente in den Arrays *Skalen*, *inputpixeloffsets* und *outputpixeloffsets* . Dieser Wert muss mit der *DimensionCount* übereinstimmen, die in *inputgradienttensor* und *outputgradienttensor* bereitgestellt wird.

`Scales`

Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***

Siehe *Skalen* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`InputPixelOffsets`

Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***

Weitere Informationen finden Sie unter *inputpixeloffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`OutputPixelOffsets`

Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***

Weitere Informationen finden Sie unter *outputpixeloffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*Inputgradienttensor* und *outputgradienttensor* müssen denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Input gradienttensor | Eingabe | 4 | Float32, FLOAT16 |
| Outputgradienttensor | Ausgabe | 4 | Float32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |