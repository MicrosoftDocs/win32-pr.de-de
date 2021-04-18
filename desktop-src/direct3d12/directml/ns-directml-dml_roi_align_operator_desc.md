---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Führt einen ROI-align-Vorgang aus, wie im [Dokument Maske R-CNN](https://arxiv.org/abs/1703.06870)beschrieben. Zusammengefasst extrahiert der Vorgang die Ernten aus dem eingabebildintensor und ändert Sie in eine gängige Ausgabegröße, die durch die letzten 2 Dimensionen von *outputtensor* unter Verwendung des angegebenen *InterpolationMode* angegeben wird.
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: 987aef7d7002892b8af3167fb8da2b74dc80a12e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351829"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a>DML_ROI_ALIGN_OPERATOR_DESC-Struktur (directml. h)

Führt einen ROI-align-Vorgang aus, wie im [Dokument Maske R-CNN](https://arxiv.org/abs/1703.06870)beschrieben. Zusammengefasst extrahiert der Vorgang die Ernten aus dem eingabebildintensor und ändert Sie in eine gängige Ausgabegröße, die durch die letzten 2 Dimensionen von *outputtensor* unter Verwendung des angegebenen *InterpolationMode* angegeben wird.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a>Member

`InputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Eingabedaten mit Dimensionen enthält `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .

`ROITensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Mandanten, der die Datenbereiche (Region of Interest, ROI) enthält. Die zulässigen Dimensionen von `ROITensor` sind `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` oder `{ 1, 1, NumROIs, 4 }` . Bei jedem ROI sind die Werte die Koordinaten der oberen linken und der unteren rechten Ecke in der Reihenfolge `[x1, y1, x2, y2]` .

`BatchIndicesTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Batch Indizes enthält, aus denen die Rois extrahiert werden. Die zulässigen Dimensionen von `BatchIndicesTensor` sind `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` oder `{ 1, 1, 1, NumROIs }` . Jeder Wert ist der Index eines Batches von *inputtensor*. Das Verhalten ist nicht definiert, wenn die Werte nicht im Bereich [0, BatchCount) liegen.

`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die Ausgabedaten enthält. Die erwarteten Dimensionen von *outputtensor* sind `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .

`ReductionFunction`

Typ: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**

Die zu verwendende Reduzierungs Funktion, wenn alle Eingabe Beispiele reduziert werden, die zu einem Output-Element ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) oder **DML_REDUCE_FUNCTION_MAX**) beitragen. Die Anzahl der zu reduzierenden Eingabe Beispiele ist von *minimumsamplesperoutput* und *maximumsamplesperoutput* begrenzt.

`InterpolationMode`

Typ: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

Der Interpolations Modus, der verwendet werden soll, wenn die Größe der Bereiche geändert wird.

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode). Verwendet den *nächstgelegenen Nachbar* Algorithmus, der das Eingabe Element auswählt, das dem entsprechenden Pixel Center für jedes Output-Element am nächsten ist.
- **DML_INTERPOLATION_MODE_LINEAR**. Verwendet den *Bilinear* -Algorithmus, der das Output-Element berechnet, indem der gewichtete Durchschnitt der zwei nächstgelegenen benachbarten Eingabeelemente pro Dimension ausgeführt wird. Da die Größe von nur 2 Dimensionen geändert wird, wird der gewichtete Durchschnitt für jedes Ausgabe Element auf insgesamt vier Eingabeelemente berechnet.

`SpatialScaleX`

Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Die X-Komponente (oder Breite) des Skalierungsfaktors, um die *roitensor* -Koordinaten zu multiplizieren, damit Sie proportional zu *inputheight* und *inputwidth* werden. Wenn z. b. der *roitensor* normalisierte Koordinaten (Werte im Bereich [0.. 1]) enthält, hat *spatialscalex* normalerweise denselben Wert wie *Input Width*.

`SpatialScaleY`

Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Die Y-Komponente (oder Höhe) des Skalierungsfaktors, um die *roitensor* -Koordinaten zu multiplizieren, damit Sie proportional zu *inputheight* und *inputwidth* werden. Wenn z. b. der *roitensor* normalisierte Koordinaten (Werte im Bereich [0.. 1]) enthält, hat *spatialscaley* normalerweise denselben Wert wie *inputheight*.

`OutOfBoundsInputValue`

Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Der von *inputtensor* zu lesende Wert, wenn sich die Rois außerhalb der Grenzen von *inputtensor* befinden. Dies kann vorkommen, wenn die Werte, die nach dem Skalieren von *roitensor* von *spatialscalex* und *spatialscaley* abgerufen werden, größer als *Input Width* und *inputheight* sind.

`MinimumSamplesPerOutput`

Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

Die Mindestanzahl von Eingabe Beispielen, die für jedes Output-Element verwendet werden sollen. Der-Operator berechnet die Anzahl der Eingabe Proben, indem `ScaledCropSize / OutputSize` er Sie durchführt, und gibt ihn dann an *minimumsamplesperoutput* und *maximumsamplesperoutput* an.

`MaximumSamplesPerOutput`

Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

Die maximale Anzahl von Eingabe Beispielen, die für jedes Output-Element verwendet werden sollen. Der-Operator berechnet die Anzahl der Eingabe Proben, indem `ScaledCropSize / OutputSize` er Sie durchführt, und gibt ihn dann an *minimumsamplesperoutput* und *maximumsamplesperoutput* an.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
" *Inputtensor*", " *outputtensor*" und " *roitensor* " müssen denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 | Float32, FLOAT16 |
| Roitensor | Eingabe | 2 bis 4 | Float32, FLOAT16 |
| Batchindicestensor | Eingabe | 1 bis 4 | UINT32 |
| Outputtensor | Ausgabe | 4 | Float32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |