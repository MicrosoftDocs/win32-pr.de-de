---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Führt einen ROI-Ausrichtungsvorgang aus, wie im Dokument [Mask R-CNN (Maskieren von R-CNN) beschrieben.](https://arxiv.org/abs/1703.06870) Zusammenfassend lässt sich sehen, dass der Vorgang Diebungen aus dem Eingabebild-Tensor extrahiert und mithilfe des angegebenen *InterpolationMode* in eine gemeinsame Ausgabegröße geändert wird, die von den letzten 2 Dimensionen von *OutputTensor* angegeben wird.
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
ms.openlocfilehash: b9004a77d3b325dd3394d1a3a6b596e94997e9fd
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804006"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a>DML_ROI_ALIGN_OPERATOR_DESC -Struktur (directml.h)

Führt einen ROI-Ausrichtungsvorgang aus, wie im Dokument [Mask R-CNN (Maskieren von R-CNN) beschrieben.](https://arxiv.org/abs/1703.06870) Zusammenfassend lässt sich sehen, dass mit dem Vorgang Diesbeschnitte aus dem Eingabebild-Tensor extrahiert und mithilfe des angegebenen *InterpolationMode* in eine gemeinsame Ausgabegröße geändert werden, die von den letzten 2 Dimensionen von *OutputTensor* angegeben wird.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

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

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Eingabedaten mit den Dimensionen `{ BatchCount, ChannelCount, InputHeight, InputWidth }` enthält.

`ROITensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Roi-Daten (Regions of Interest) enthält. Die zulässigen Dimensionen `ROITensor` von sind , oder `{ NumROIs, 4 }` `{ 1, NumROIs, 4 }` `{ 1, 1, NumROIs, 4 }` . Für jeden ROI sind die Werte die Koordinaten der oberen linken und unteren rechten Ecken in der Reihenfolge `[x1, y1, x2, y2]` .

`BatchIndicesTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Batchindizes enthält, aus denen die ROIs extrahiert werden. Die zulässigen Dimensionen `BatchIndicesTensor` von sind , , oder `{ NumROIs }` `{ 1, NumROIs }` `{ 1, 1, NumROIs }` `{ 1, 1, 1, NumROIs }` . Jeder Wert ist der Index eines Batches aus *InputTensor.* Das Verhalten ist nicht definiert, wenn die Werte nicht im Bereich [0, BatchCount) liegen.

`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Ausgabedaten enthält. Die erwarteten Dimensionen von *OutputTensor* sind `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .

`ReductionFunction`

Typ: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**

Die Reduzierungsfunktion, die beim Reduzieren aller Eingabebeispiele verwendet werden soll, die zu einem Ausgabeelement beitragen ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) oder **DML_REDUCE_FUNCTION_MAX**). Die Anzahl der Eingabebeispiele, über die reduziert werden soll, wird durch *MinimumSamplesPerOutput* und *MaximumSamplesPerOutput* begrenzt.

`InterpolationMode`

Typ: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

Der Interpolationsmodus, der beim Ändern der Größe der Regionen verwendet werden soll.

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode). Verwendet den *Nearest* Neighbor-Algorithmus, mit dem das Eingabeelement ausgewählt wird, das dem entsprechenden Pixelmittelpunkt für jedes Ausgabeelement am nächsten ist.
- **DML_INTERPOLATION_MODE_LINEAR**. Verwendet den *bilinearen* Algorithmus, der das Ausgabeelement berechnet, indem der gewichtete Durchschnitt der 2 nächsten benachbarten Eingabeelemente pro Dimension durchgeführt wird. Da nur zwei Dimensionen geändert werden, wird der gewichtete Durchschnitt für jedes Ausgabeelement auf insgesamt vier Eingabeelementen berechnet.

`SpatialScaleX`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Die X-Komponente (oder Breite) des Skalierungsfaktors, um die *ROITensor-Koordinaten* mit zu multiplizieren, um sie proportional zu *InputHeight* und *InputWidth* zu machen. Wenn *ROITensor* beispielsweise normalisierte Koordinaten (Werte im Bereich [0..1]) enthält, hat *SpatialScaleX* normalerweise den gleichen Wert wie *InputWidth.*

`SpatialScaleY`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Die Komponente Y (oder Höhe) des Skalierungsfaktors, um die *ROITensor-Koordinaten* mit zu multiplizieren, um sie proportional zu *InputHeight* und *InputWidth* zu machen. Wenn *ROITensor* beispielsweise normalisierte Koordinaten (Werte im Bereich [0..1]) enthält, hat *SpatialScaleY* normalerweise den gleichen Wert wie *InputHeight*.

`OutOfBoundsInputValue`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Der Wert, der aus *InputTensor* gelesen werden soll, wenn sich die ROIs außerhalb der Grenzen von *InputTensor* befinden. Dies kann passieren, wenn die Werte, die nach dem Skalieren von *ROITensor* von *SpatialScaleX* und *SpatialScaleY* ermittelt wurden, größer als *InputWidth* und *InputHeight sind.*

`MinimumSamplesPerOutput`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

Die Mindestanzahl von Eingabebeispielen, die für jedes Ausgabeelement verwendet werden. Der Operator berechnet die Anzahl der Eingabebeispiele mit , und klammert sie dann an `ScaledCropSize / OutputSize` *MinimumSamplesPerOutput* und *MaximumSamplesPerOutput.*

`MaximumSamplesPerOutput`

Typ: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

Die maximale Anzahl von Eingabebeispielen, die für jedes Ausgabeelement verwendet werden. Der Operator berechnet die Anzahl der Eingabebeispiele mit , und klammert sie dann an `ScaledCropSize / OutputSize` *MinimumSamplesPerOutput* und *MaximumSamplesPerOutput.*

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
*InputTensor,* *OutputTensor* und *ROITensor* müssen denselben *Datentyp haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Unterstützte Dimensionsanzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 | FLOAT32, FLOAT16 |
| ROITensor | Eingabe | 2 bis 4 | FLOAT32, FLOAT16 |
| BatchIndicesTensor | Eingabe | 1 bis 4 | UINT32 |
| OutputTensor | Ausgabe | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |