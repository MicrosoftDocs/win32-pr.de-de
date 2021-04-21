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
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a><span data-ttu-id="6b47e-104">DML_ROI_ALIGN_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="6b47e-104">DML_ROI_ALIGN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="6b47e-105">Führt einen ROI-Ausrichtungsvorgang aus, wie im Dokument [Mask R-CNN (Maskieren von R-CNN) beschrieben.](https://arxiv.org/abs/1703.06870)</span><span class="sxs-lookup"><span data-stu-id="6b47e-105">Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870).</span></span> <span data-ttu-id="6b47e-106">Zusammenfassend lässt sich sehen, dass mit dem Vorgang Diesbeschnitte aus dem Eingabebild-Tensor extrahiert und mithilfe des angegebenen *InterpolationMode* in eine gemeinsame Ausgabegröße geändert werden, die von den letzten 2 Dimensionen von *OutputTensor* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6b47e-106">In summary, the operation extracts crops from the input image tensor and resizes them to a common output size specified by the last 2 dimensions of *OutputTensor* using the specified *InterpolationMode*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b47e-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="6b47e-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="6b47e-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="6b47e-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b47e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b47e-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="6b47e-110">Member</span><span class="sxs-lookup"><span data-stu-id="6b47e-110">Members</span></span>

`InputTensor`

<span data-ttu-id="6b47e-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6b47e-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6b47e-112">Ein Tensor, der die Eingabedaten mit den Dimensionen `{ BatchCount, ChannelCount, InputHeight, InputWidth }` enthält.</span><span class="sxs-lookup"><span data-stu-id="6b47e-112">A tensor containing the input data with dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }`.</span></span>

`ROITensor`

<span data-ttu-id="6b47e-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6b47e-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6b47e-114">Ein Tensor, der die Roi-Daten (Regions of Interest) enthält.</span><span class="sxs-lookup"><span data-stu-id="6b47e-114">A tensor containing the regions of interest (ROI) data.</span></span> <span data-ttu-id="6b47e-115">Die zulässigen Dimensionen `ROITensor` von sind , oder `{ NumROIs, 4 }` `{ 1, NumROIs, 4 }` `{ 1, 1, NumROIs, 4 }` .</span><span class="sxs-lookup"><span data-stu-id="6b47e-115">The allowed dimensions of `ROITensor` are `{ NumROIs, 4 }`, `{ 1, NumROIs, 4 }`, or `{ 1, 1, NumROIs, 4 }`.</span></span> <span data-ttu-id="6b47e-116">Für jeden ROI sind die Werte die Koordinaten der oberen linken und unteren rechten Ecken in der Reihenfolge `[x1, y1, x2, y2]` .</span><span class="sxs-lookup"><span data-stu-id="6b47e-116">For each ROI, the values will be the coordinates of its top-left and bottom-right corners in the order `[x1, y1, x2, y2]`.</span></span>

`BatchIndicesTensor`

<span data-ttu-id="6b47e-117">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6b47e-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6b47e-118">Ein Tensor, der die Batchindizes enthält, aus denen die ROIs extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b47e-118">A tensor containing the batch indices to extract the ROIs from.</span></span> <span data-ttu-id="6b47e-119">Die zulässigen Dimensionen `BatchIndicesTensor` von sind , , oder `{ NumROIs }` `{ 1, NumROIs }` `{ 1, 1, NumROIs }` `{ 1, 1, 1, NumROIs }` .</span><span class="sxs-lookup"><span data-stu-id="6b47e-119">The allowed dimensions of `BatchIndicesTensor` are `{ NumROIs }`, `{ 1, NumROIs }`, `{ 1, 1, NumROIs }`, or `{ 1, 1, 1, NumROIs }`.</span></span> <span data-ttu-id="6b47e-120">Jeder Wert ist der Index eines Batches aus *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="6b47e-120">Each value is the index of a batch from *InputTensor*.</span></span> <span data-ttu-id="6b47e-121">Das Verhalten ist nicht definiert, wenn die Werte nicht im Bereich [0, BatchCount) liegen.</span><span class="sxs-lookup"><span data-stu-id="6b47e-121">The behavior is undefined if the values are not in the range [0, BatchCount).</span></span>

`OutputTensor`

<span data-ttu-id="6b47e-122">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6b47e-122">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6b47e-123">Ein Tensor, der die Ausgabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="6b47e-123">A tensor containing the output data.</span></span> <span data-ttu-id="6b47e-124">Die erwarteten Dimensionen von *OutputTensor* sind `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="6b47e-124">The expected dimensions of *OutputTensor* are `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }`.</span></span>

`ReductionFunction`

<span data-ttu-id="6b47e-125">Typ: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span><span class="sxs-lookup"><span data-stu-id="6b47e-125">Type: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span></span>

<span data-ttu-id="6b47e-126">Die Reduzierungsfunktion, die beim Reduzieren aller Eingabebeispiele verwendet werden soll, die zu einem Ausgabeelement beitragen ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) oder **DML_REDUCE_FUNCTION_MAX**).</span><span class="sxs-lookup"><span data-stu-id="6b47e-126">The reduction function to use when reducing across all input samples that contribute to an output element ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) or **DML_REDUCE_FUNCTION_MAX**).</span></span> <span data-ttu-id="6b47e-127">Die Anzahl der Eingabebeispiele, über die reduziert werden soll, wird durch *MinimumSamplesPerOutput* und *MaximumSamplesPerOutput* begrenzt.</span><span class="sxs-lookup"><span data-stu-id="6b47e-127">The number of input samples to reduce across is bounded by *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`InterpolationMode`

<span data-ttu-id="6b47e-128">Typ: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span><span class="sxs-lookup"><span data-stu-id="6b47e-128">Type: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span></span>

<span data-ttu-id="6b47e-129">Der Interpolationsmodus, der beim Ändern der Größe der Regionen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b47e-129">The interpolation mode to use when resizing the regions.</span></span>

- <span data-ttu-id="6b47e-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span><span class="sxs-lookup"><span data-stu-id="6b47e-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span></span> <span data-ttu-id="6b47e-131">Verwendet den *Nearest* Neighbor-Algorithmus, mit dem das Eingabeelement ausgewählt wird, das dem entsprechenden Pixelmittelpunkt für jedes Ausgabeelement am nächsten ist.</span><span class="sxs-lookup"><span data-stu-id="6b47e-131">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>
- <span data-ttu-id="6b47e-132">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="6b47e-132">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="6b47e-133">Verwendet den *bilinearen* Algorithmus, der das Ausgabeelement berechnet, indem der gewichtete Durchschnitt der 2 nächsten benachbarten Eingabeelemente pro Dimension durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b47e-133">Uses the *Bilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="6b47e-134">Da nur zwei Dimensionen geändert werden, wird der gewichtete Durchschnitt für jedes Ausgabeelement auf insgesamt vier Eingabeelementen berechnet.</span><span class="sxs-lookup"><span data-stu-id="6b47e-134">Since only 2 dimensions are resized, the weighted average is computed on a total of 4 input elements for each output element.</span></span>

`SpatialScaleX`

<span data-ttu-id="6b47e-135">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="6b47e-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="6b47e-136">Die X-Komponente (oder Breite) des Skalierungsfaktors, um die *ROITensor-Koordinaten* mit zu multiplizieren, um sie proportional zu *InputHeight* und *InputWidth* zu machen.</span><span class="sxs-lookup"><span data-stu-id="6b47e-136">The X (or width) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="6b47e-137">Wenn *ROITensor* beispielsweise normalisierte Koordinaten (Werte im Bereich [0..1]) enthält, hat *SpatialScaleX* normalerweise den gleichen Wert wie *InputWidth.*</span><span class="sxs-lookup"><span data-stu-id="6b47e-137">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), then *SpatialScaleX* would usually have the same value as *InputWidth*.</span></span>

`SpatialScaleY`

<span data-ttu-id="6b47e-138">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="6b47e-138">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="6b47e-139">Die Komponente Y (oder Höhe) des Skalierungsfaktors, um die *ROITensor-Koordinaten* mit zu multiplizieren, um sie proportional zu *InputHeight* und *InputWidth* zu machen.</span><span class="sxs-lookup"><span data-stu-id="6b47e-139">The Y (or height) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="6b47e-140">Wenn *ROITensor* beispielsweise normalisierte Koordinaten (Werte im Bereich [0..1]) enthält, hat *SpatialScaleY* normalerweise den gleichen Wert wie *InputHeight*.</span><span class="sxs-lookup"><span data-stu-id="6b47e-140">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), *SpatialScaleY* would usually have the same value as *InputHeight*.</span></span>

`OutOfBoundsInputValue`

<span data-ttu-id="6b47e-141">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="6b47e-141">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="6b47e-142">Der Wert, der aus *InputTensor* gelesen werden soll, wenn sich die ROIs außerhalb der Grenzen von *InputTensor* befinden.</span><span class="sxs-lookup"><span data-stu-id="6b47e-142">The value to read from *InputTensor* when the ROIs are outside the bounds of *InputTensor*.</span></span> <span data-ttu-id="6b47e-143">Dies kann passieren, wenn die Werte, die nach dem Skalieren von *ROITensor* von *SpatialScaleX* und *SpatialScaleY* ermittelt wurden, größer als *InputWidth* und *InputHeight sind.*</span><span class="sxs-lookup"><span data-stu-id="6b47e-143">This can happen when the values obtained after scaling *ROITensor* by *SpatialScaleX* and *SpatialScaleY* are bigger than *InputWidth* and *InputHeight*.</span></span>

`MinimumSamplesPerOutput`

<span data-ttu-id="6b47e-144">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="6b47e-144">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="6b47e-145">Die Mindestanzahl von Eingabebeispielen, die für jedes Ausgabeelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b47e-145">The minimum number of input samples to use for every output element.</span></span> <span data-ttu-id="6b47e-146">Der Operator berechnet die Anzahl der Eingabebeispiele mit , und klammert sie dann an `ScaledCropSize / OutputSize` *MinimumSamplesPerOutput* und *MaximumSamplesPerOutput.*</span><span class="sxs-lookup"><span data-stu-id="6b47e-146">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`MaximumSamplesPerOutput`

<span data-ttu-id="6b47e-147">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="6b47e-147">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="6b47e-148">Die maximale Anzahl von Eingabebeispielen, die für jedes Ausgabeelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b47e-148">The maximum number of input samples to use for every output element.</span></span> <span data-ttu-id="6b47e-149">Der Operator berechnet die Anzahl der Eingabebeispiele mit , und klammert sie dann an `ScaledCropSize / OutputSize` *MinimumSamplesPerOutput* und *MaximumSamplesPerOutput.*</span><span class="sxs-lookup"><span data-stu-id="6b47e-149">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

## <a name="availability"></a><span data-ttu-id="6b47e-150">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="6b47e-150">Availability</span></span>
<span data-ttu-id="6b47e-151">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6b47e-151">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6b47e-152">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="6b47e-152">Tensor constraints</span></span>
<span data-ttu-id="6b47e-153">*InputTensor,* *OutputTensor* und *ROITensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="6b47e-153">*InputTensor*, *OutputTensor*, and *ROITensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6b47e-154">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="6b47e-154">Tensor support</span></span>
| <span data-ttu-id="6b47e-155">Tensor</span><span class="sxs-lookup"><span data-stu-id="6b47e-155">Tensor</span></span> | <span data-ttu-id="6b47e-156">Typ</span><span class="sxs-lookup"><span data-stu-id="6b47e-156">Kind</span></span> | <span data-ttu-id="6b47e-157">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="6b47e-157">Supported dimension counts</span></span> | <span data-ttu-id="6b47e-158">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="6b47e-158">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6b47e-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="6b47e-159">InputTensor</span></span> | <span data-ttu-id="6b47e-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b47e-160">Input</span></span> | <span data-ttu-id="6b47e-161">4</span><span class="sxs-lookup"><span data-stu-id="6b47e-161">4</span></span> | <span data-ttu-id="6b47e-162">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6b47e-162">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6b47e-163">ROITensor</span><span class="sxs-lookup"><span data-stu-id="6b47e-163">ROITensor</span></span> | <span data-ttu-id="6b47e-164">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b47e-164">Input</span></span> | <span data-ttu-id="6b47e-165">2 bis 4</span><span class="sxs-lookup"><span data-stu-id="6b47e-165">2 to 4</span></span> | <span data-ttu-id="6b47e-166">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6b47e-166">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6b47e-167">BatchIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="6b47e-167">BatchIndicesTensor</span></span> | <span data-ttu-id="6b47e-168">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b47e-168">Input</span></span> | <span data-ttu-id="6b47e-169">1 bis 4</span><span class="sxs-lookup"><span data-stu-id="6b47e-169">1 to 4</span></span> | <span data-ttu-id="6b47e-170">UINT32</span><span class="sxs-lookup"><span data-stu-id="6b47e-170">UINT32</span></span> |
| <span data-ttu-id="6b47e-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="6b47e-171">OutputTensor</span></span> | <span data-ttu-id="6b47e-172">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="6b47e-172">Output</span></span> | <span data-ttu-id="6b47e-173">4</span><span class="sxs-lookup"><span data-stu-id="6b47e-173">4</span></span> | <span data-ttu-id="6b47e-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6b47e-174">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="6b47e-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b47e-175">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6b47e-176">**Header**</span><span class="sxs-lookup"><span data-stu-id="6b47e-176">**Header**</span></span> | <span data-ttu-id="6b47e-177">directml.h</span><span class="sxs-lookup"><span data-stu-id="6b47e-177">directml.h</span></span> |