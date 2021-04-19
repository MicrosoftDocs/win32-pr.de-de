---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Führt eine Mean-Varianz Normalisierungsfunktion für den eingabetensor aus. Dieser Operator berechnet den Mittelwert und die Varianz des Eingabe Mandanten, um die Normalisierung auszuführen.
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
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106373409"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC-Struktur (directml. h)
Führt eine Mean-Varianz Normalisierungsfunktion für den eingabetensor aus. Dieser Operator berechnet den Mittelwert und die Varianz des Eingabe Mandanten, um die Normalisierung auszuführen. Dieser Operator führt die folgende Berechnung aus.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Eingabedaten enthält. Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, Height, Width }` .


`ScaleTensor`

Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Skalierungs Daten enthält. Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, Height, Width }` . Jede Dimension kann durch 1 ersetzt werden, um Sie in dieser Dimension zu übertragen. Dieser tensorflow ist erforderlich, wenn der *biastensor* verwendet wird.


`BiasTensor`

Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler tensorflow, der die Daten der Bias enthält. Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, Height, Width }` . Jede Dimension kann durch 1 ersetzt werden, um Sie in dieser Dimension zu übertragen. Dieser tensorflow ist erforderlich, wenn der *scaletensor* verwendet wird.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, in den die Ergebnisse geschrieben werden sollen. Die Dimensionen dieses Mandanten sind `{ BatchCount, ChannelCount, Height, Width }` .


`AxisCount`

Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

Die Anzahl der Achsen. Dieses Feld bestimmt die Größe des *Achsen* Arrays.


`Axes`

Type: \_ Field \_ size \_ (axiscount) **Konstanten [uint](/windows/desktop/WinProg/windows-data-types) \*** 

Die Achsen, an denen der Mittelwert und die Varianz berechnet werden sollen.


`NormalizeVariance`

Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b>

**True** , wenn die normalisierungs Ebene Abweichungen in der normalisierungs Berechnung einschließt. Andernfalls **false**. **False** gibt an, dass die normalisierungs Gleichung ist `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .


`Epsilon`

Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Der Epsilon-Wert, der verwendet wird, um die Division durch Null zu vermeiden. Der Wert 0,00001 wird als Standardwert empfohlen.


`FusedActivation`

Type: \_ maybenull \_ **Konstanten [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Eine optionale, bei der Normalisierung anzuwendende, Fused-Aktivierungs Schicht.


## <a name="remarks"></a>Bemerkungen
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** ist eine supermenge der Funktionen von [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). Hier ist das Festlegen des **Achsen** Arrays `{ 0, 2, 3 }` auf das Äquivalent der Einstellung von " *Crosschannel* " auf " **false** " in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; beim Festlegen des **Achsen** Arrays auf entspricht das Festlegen `{ 1, 2, 3 }` von " *Crosschannel* " auf " **true**".

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *Inputtensor* und *outputtensor* müssen über die gleichen *Größen* verfügen.
* ' *Biastensor*', ' *inputtensor*', ' *outputtensor*' und ' *scaletensor* ' müssen denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Dimensionen | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | {BatchCount, ChannelCount, Height, Width} | 4 | Float32, FLOAT16 |
| Scaletensor | Optionale Eingabe | {Scalebatchcount, scalechannelcount, ScaleHeight, ScaleWidth} | 4 | Float32, FLOAT16 |
| Biastensor | Optionale Eingabe | {Biasbatchcount, biaschannelcount, biasheight, biaswidth} | 4 | Float32, FLOAT16 |
| Outputtensor | Ausgabe | {BatchCount, ChannelCount, Height, Width} | 4 | Float32, FLOAT16 |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |

## <a name="see-also"></a>Siehe auch

[Verwenden von Fused-Operatoren zur Verbesserung der Leistung](../dml-fused-activations.md)