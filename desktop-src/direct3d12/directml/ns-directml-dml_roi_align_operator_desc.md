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
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a><span data-ttu-id="0e32a-104">DML_ROI_ALIGN_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="0e32a-104">DML_ROI_ALIGN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="0e32a-105">Führt einen ROI-align-Vorgang aus, wie im [Dokument Maske R-CNN](https://arxiv.org/abs/1703.06870)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0e32a-105">Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870).</span></span> <span data-ttu-id="0e32a-106">Zusammengefasst extrahiert der Vorgang die Ernten aus dem eingabebildintensor und ändert Sie in eine gängige Ausgabegröße, die durch die letzten 2 Dimensionen von *outputtensor* unter Verwendung des angegebenen *InterpolationMode* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e32a-106">In summary, the operation extracts crops from the input image tensor and resizes them to a common output size specified by the last 2 dimensions of *OutputTensor* using the specified *InterpolationMode*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e32a-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="0e32a-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="0e32a-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="0e32a-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e32a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e32a-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="0e32a-110">Member</span><span class="sxs-lookup"><span data-stu-id="0e32a-110">Members</span></span>

`InputTensor`

<span data-ttu-id="0e32a-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0e32a-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0e32a-112">Ein tensorflow, der die Eingabedaten mit Dimensionen enthält `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="0e32a-112">A tensor containing the input data with dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }`.</span></span>

`ROITensor`

<span data-ttu-id="0e32a-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0e32a-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0e32a-114">Ein Mandanten, der die Datenbereiche (Region of Interest, ROI) enthält.</span><span class="sxs-lookup"><span data-stu-id="0e32a-114">A tensor containing the regions of interest (ROI) data.</span></span> <span data-ttu-id="0e32a-115">Die zulässigen Dimensionen von `ROITensor` sind `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` oder `{ 1, 1, NumROIs, 4 }` .</span><span class="sxs-lookup"><span data-stu-id="0e32a-115">The allowed dimensions of `ROITensor` are `{ NumROIs, 4 }`, `{ 1, NumROIs, 4 }`, or `{ 1, 1, NumROIs, 4 }`.</span></span> <span data-ttu-id="0e32a-116">Bei jedem ROI sind die Werte die Koordinaten der oberen linken und der unteren rechten Ecke in der Reihenfolge `[x1, y1, x2, y2]` .</span><span class="sxs-lookup"><span data-stu-id="0e32a-116">For each ROI, the values will be the coordinates of its top-left and bottom-right corners in the order `[x1, y1, x2, y2]`.</span></span>

`BatchIndicesTensor`

<span data-ttu-id="0e32a-117">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0e32a-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0e32a-118">Ein tensorflow, der die Batch Indizes enthält, aus denen die Rois extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="0e32a-118">A tensor containing the batch indices to extract the ROIs from.</span></span> <span data-ttu-id="0e32a-119">Die zulässigen Dimensionen von `BatchIndicesTensor` sind `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` oder `{ 1, 1, 1, NumROIs }` .</span><span class="sxs-lookup"><span data-stu-id="0e32a-119">The allowed dimensions of `BatchIndicesTensor` are `{ NumROIs }`, `{ 1, NumROIs }`, `{ 1, 1, NumROIs }`, or `{ 1, 1, 1, NumROIs }`.</span></span> <span data-ttu-id="0e32a-120">Jeder Wert ist der Index eines Batches von *inputtensor*.</span><span class="sxs-lookup"><span data-stu-id="0e32a-120">Each value is the index of a batch from *InputTensor*.</span></span> <span data-ttu-id="0e32a-121">Das Verhalten ist nicht definiert, wenn die Werte nicht im Bereich [0, BatchCount) liegen.</span><span class="sxs-lookup"><span data-stu-id="0e32a-121">The behavior is undefined if the values are not in the range [0, BatchCount).</span></span>

`OutputTensor`

<span data-ttu-id="0e32a-122">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0e32a-122">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0e32a-123">Ein tensorflow, der die Ausgabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="0e32a-123">A tensor containing the output data.</span></span> <span data-ttu-id="0e32a-124">Die erwarteten Dimensionen von *outputtensor* sind `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="0e32a-124">The expected dimensions of *OutputTensor* are `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }`.</span></span>

`ReductionFunction`

<span data-ttu-id="0e32a-125">Typ: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span><span class="sxs-lookup"><span data-stu-id="0e32a-125">Type: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span></span>

<span data-ttu-id="0e32a-126">Die zu verwendende Reduzierungs Funktion, wenn alle Eingabe Beispiele reduziert werden, die zu einem Output-Element ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) oder **DML_REDUCE_FUNCTION_MAX**) beitragen.</span><span class="sxs-lookup"><span data-stu-id="0e32a-126">The reduction function to use when reducing across all input samples that contribute to an output element ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) or **DML_REDUCE_FUNCTION_MAX**).</span></span> <span data-ttu-id="0e32a-127">Die Anzahl der zu reduzierenden Eingabe Beispiele ist von *minimumsamplesperoutput* und *maximumsamplesperoutput* begrenzt.</span><span class="sxs-lookup"><span data-stu-id="0e32a-127">The number of input samples to reduce across is bounded by *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`InterpolationMode`

<span data-ttu-id="0e32a-128">Typ: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span><span class="sxs-lookup"><span data-stu-id="0e32a-128">Type: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span></span>

<span data-ttu-id="0e32a-129">Der Interpolations Modus, der verwendet werden soll, wenn die Größe der Bereiche geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0e32a-129">The interpolation mode to use when resizing the regions.</span></span>

- <span data-ttu-id="0e32a-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span><span class="sxs-lookup"><span data-stu-id="0e32a-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span></span> <span data-ttu-id="0e32a-131">Verwendet den *nächstgelegenen Nachbar* Algorithmus, der das Eingabe Element auswählt, das dem entsprechenden Pixel Center für jedes Output-Element am nächsten ist.</span><span class="sxs-lookup"><span data-stu-id="0e32a-131">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>
- <span data-ttu-id="0e32a-132">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="0e32a-132">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="0e32a-133">Verwendet den *Bilinear* -Algorithmus, der das Output-Element berechnet, indem der gewichtete Durchschnitt der zwei nächstgelegenen benachbarten Eingabeelemente pro Dimension ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e32a-133">Uses the *Bilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="0e32a-134">Da die Größe von nur 2 Dimensionen geändert wird, wird der gewichtete Durchschnitt für jedes Ausgabe Element auf insgesamt vier Eingabeelemente berechnet.</span><span class="sxs-lookup"><span data-stu-id="0e32a-134">Since only 2 dimensions are resized, the weighted average is computed on a total of 4 input elements for each output element.</span></span>

`SpatialScaleX`

<span data-ttu-id="0e32a-135">Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="0e32a-135">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="0e32a-136">Die X-Komponente (oder Breite) des Skalierungsfaktors, um die *roitensor* -Koordinaten zu multiplizieren, damit Sie proportional zu *inputheight* und *inputwidth* werden.</span><span class="sxs-lookup"><span data-stu-id="0e32a-136">The X (or width) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="0e32a-137">Wenn z. b. der *roitensor* normalisierte Koordinaten (Werte im Bereich [0.. 1]) enthält, hat *spatialscalex* normalerweise denselben Wert wie *Input Width*.</span><span class="sxs-lookup"><span data-stu-id="0e32a-137">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), then *SpatialScaleX* would usually have the same value as *InputWidth*.</span></span>

`SpatialScaleY`

<span data-ttu-id="0e32a-138">Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="0e32a-138">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="0e32a-139">Die Y-Komponente (oder Höhe) des Skalierungsfaktors, um die *roitensor* -Koordinaten zu multiplizieren, damit Sie proportional zu *inputheight* und *inputwidth* werden.</span><span class="sxs-lookup"><span data-stu-id="0e32a-139">The Y (or height) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="0e32a-140">Wenn z. b. der *roitensor* normalisierte Koordinaten (Werte im Bereich [0.. 1]) enthält, hat *spatialscaley* normalerweise denselben Wert wie *inputheight*.</span><span class="sxs-lookup"><span data-stu-id="0e32a-140">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), *SpatialScaleY* would usually have the same value as *InputHeight*.</span></span>

`OutOfBoundsInputValue`

<span data-ttu-id="0e32a-141">Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="0e32a-141">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="0e32a-142">Der von *inputtensor* zu lesende Wert, wenn sich die Rois außerhalb der Grenzen von *inputtensor* befinden.</span><span class="sxs-lookup"><span data-stu-id="0e32a-142">The value to read from *InputTensor* when the ROIs are outside the bounds of *InputTensor*.</span></span> <span data-ttu-id="0e32a-143">Dies kann vorkommen, wenn die Werte, die nach dem Skalieren von *roitensor* von *spatialscalex* und *spatialscaley* abgerufen werden, größer als *Input Width* und *inputheight* sind.</span><span class="sxs-lookup"><span data-stu-id="0e32a-143">This can happen when the values obtained after scaling *ROITensor* by *SpatialScaleX* and *SpatialScaleY* are bigger than *InputWidth* and *InputHeight*.</span></span>

`MinimumSamplesPerOutput`

<span data-ttu-id="0e32a-144">Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="0e32a-144">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="0e32a-145">Die Mindestanzahl von Eingabe Beispielen, die für jedes Output-Element verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0e32a-145">The minimum number of input samples to use for every output element.</span></span> <span data-ttu-id="0e32a-146">Der-Operator berechnet die Anzahl der Eingabe Proben, indem `ScaledCropSize / OutputSize` er Sie durchführt, und gibt ihn dann an *minimumsamplesperoutput* und *maximumsamplesperoutput* an.</span><span class="sxs-lookup"><span data-stu-id="0e32a-146">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`MaximumSamplesPerOutput`

<span data-ttu-id="0e32a-147">Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="0e32a-147">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="0e32a-148">Die maximale Anzahl von Eingabe Beispielen, die für jedes Output-Element verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0e32a-148">The maximum number of input samples to use for every output element.</span></span> <span data-ttu-id="0e32a-149">Der-Operator berechnet die Anzahl der Eingabe Proben, indem `ScaledCropSize / OutputSize` er Sie durchführt, und gibt ihn dann an *minimumsamplesperoutput* und *maximumsamplesperoutput* an.</span><span class="sxs-lookup"><span data-stu-id="0e32a-149">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

## <a name="availability"></a><span data-ttu-id="0e32a-150">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="0e32a-150">Availability</span></span>
<span data-ttu-id="0e32a-151">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="0e32a-151">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="0e32a-152">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="0e32a-152">Tensor constraints</span></span>
<span data-ttu-id="0e32a-153">" *Inputtensor*", " *outputtensor*" und " *roitensor* " müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0e32a-153">*InputTensor*, *OutputTensor*, and *ROITensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="0e32a-154">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0e32a-154">Tensor support</span></span>
| <span data-ttu-id="0e32a-155">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="0e32a-155">Tensor</span></span> | <span data-ttu-id="0e32a-156">Typ</span><span class="sxs-lookup"><span data-stu-id="0e32a-156">Kind</span></span> | <span data-ttu-id="0e32a-157">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="0e32a-157">Supported dimension counts</span></span> | <span data-ttu-id="0e32a-158">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="0e32a-158">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0e32a-159">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="0e32a-159">InputTensor</span></span> | <span data-ttu-id="0e32a-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0e32a-160">Input</span></span> | <span data-ttu-id="0e32a-161">4</span><span class="sxs-lookup"><span data-stu-id="0e32a-161">4</span></span> | <span data-ttu-id="0e32a-162">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0e32a-162">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0e32a-163">Roitensor</span><span class="sxs-lookup"><span data-stu-id="0e32a-163">ROITensor</span></span> | <span data-ttu-id="0e32a-164">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0e32a-164">Input</span></span> | <span data-ttu-id="0e32a-165">2 bis 4</span><span class="sxs-lookup"><span data-stu-id="0e32a-165">2 to 4</span></span> | <span data-ttu-id="0e32a-166">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0e32a-166">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0e32a-167">Batchindicestensor</span><span class="sxs-lookup"><span data-stu-id="0e32a-167">BatchIndicesTensor</span></span> | <span data-ttu-id="0e32a-168">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0e32a-168">Input</span></span> | <span data-ttu-id="0e32a-169">1 bis 4</span><span class="sxs-lookup"><span data-stu-id="0e32a-169">1 to 4</span></span> | <span data-ttu-id="0e32a-170">UINT32</span><span class="sxs-lookup"><span data-stu-id="0e32a-170">UINT32</span></span> |
| <span data-ttu-id="0e32a-171">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="0e32a-171">OutputTensor</span></span> | <span data-ttu-id="0e32a-172">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="0e32a-172">Output</span></span> | <span data-ttu-id="0e32a-173">4</span><span class="sxs-lookup"><span data-stu-id="0e32a-173">4</span></span> | <span data-ttu-id="0e32a-174">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0e32a-174">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="0e32a-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e32a-175">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0e32a-176">**Header**</span><span class="sxs-lookup"><span data-stu-id="0e32a-176">**Header**</span></span> | <span data-ttu-id="0e32a-177">directml. h</span><span class="sxs-lookup"><span data-stu-id="0e32a-177">directml.h</span></span> |