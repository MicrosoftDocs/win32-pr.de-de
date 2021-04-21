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
ms.openlocfilehash: ac98813e15ab3dac71a9f8395333160ce37778b0
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804057"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a><span data-ttu-id="68f20-104">DML_RESAMPLE1_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="68f20-104">DML_RESAMPLE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="68f20-105">Resamples von Elementen von der Quelle zum Ziel-Tensor unter Verwendung der Skalierungsfaktoren zum Berechnen der Ziel-Tensorgröße.</span><span class="sxs-lookup"><span data-stu-id="68f20-105">Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size.</span></span> <span data-ttu-id="68f20-106">Sie können einen linearen oder nächsten Nachbarinterpolationsmodus verwenden.</span><span class="sxs-lookup"><span data-stu-id="68f20-106">You can use a linear or nearest-neighbor interpolation mode.</span></span> <span data-ttu-id="68f20-107">Der -Operator unterstützt die Interpolation über mehrere Dimensionen hinweg, nicht nur 2D.</span><span class="sxs-lookup"><span data-stu-id="68f20-107">The operator supports interpolation across multiple dimensions, not just 2D.</span></span> <span data-ttu-id="68f20-108">Sie können also die gleiche räumliche Größe beibehalten, aber über Kanäle oder Batches hinweg interpolieren.</span><span class="sxs-lookup"><span data-stu-id="68f20-108">So you can keep the same spatial size, but interpolate across channels or across batches.</span></span> <span data-ttu-id="68f20-109">Die Beziehung zwischen den Eingabe- und Ausgabekoordinaten lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="68f20-109">The relationship between the input and output coordinates is the following.</span></span>

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> <span data-ttu-id="68f20-110">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="68f20-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="68f20-111">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="68f20-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="68f20-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="68f20-112">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="68f20-113">Member</span><span class="sxs-lookup"><span data-stu-id="68f20-113">Members</span></span>

`InputTensor`

<span data-ttu-id="68f20-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="68f20-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="68f20-115">Der Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="68f20-115">The tensor containing the input data.</span></span>


`OutputTensor`

<span data-ttu-id="68f20-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="68f20-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="68f20-117">Der Tensor, in den die Ausgabedaten geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="68f20-117">The tensor to write the output data to.</span></span>


`InterpolationMode`

<span data-ttu-id="68f20-118">Typ: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="68f20-118">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="68f20-119">Dieses Feld bestimmt die Art der Interpolation, die zum Auswählen von Ausgabepixeln verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68f20-119">This field determines the kind of interpolation used to choose output pixels.</span></span>

- <span data-ttu-id="68f20-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span><span class="sxs-lookup"><span data-stu-id="68f20-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span></span> <span data-ttu-id="68f20-121">Verwendet den *Nearest* Neighbor-Algorithmus, mit dem das Eingabeelement ausgewählt wird, das dem entsprechenden Pixelmittelpunkt für jedes Ausgabeelement am nächsten ist.</span><span class="sxs-lookup"><span data-stu-id="68f20-121">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>

- <span data-ttu-id="68f20-122">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="68f20-122">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="68f20-123">Verwendet den *Quadrilinear-Algorithmus,* der das Ausgabeelement berechnet, indem der gewichtete Durchschnitt der 2 nächsten benachbarten Eingabeelemente pro Dimension durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68f20-123">Uses the *Quadrilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="68f20-124">Da alle vier Dimensionen neu berechnet werden können, wird der gewichtete Durchschnitt auf insgesamt 16 Eingabeelementen für jedes Ausgabeelement berechnet.</span><span class="sxs-lookup"><span data-stu-id="68f20-124">Since all 4 dimensions can be resampled, the weighted average is computed on a total of 16 input elements for each output element.</span></span>


`DimensionCount`

<span data-ttu-id="68f20-125">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="68f20-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="68f20-126">Die Anzahl der Werte in den Arrays, auf die *Skaliert,* *InputPixelOffsets* und *OutputPixelOffsets* zeigen.</span><span class="sxs-lookup"><span data-stu-id="68f20-126">The number of values in the arrays that *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* point to.</span></span> <span data-ttu-id="68f20-127">Dieser Wert muss mit der Dimensionsanzahl von *InputTensor* und *OutputTensor* übereinstimmen, die 4 sein muss.</span><span class="sxs-lookup"><span data-stu-id="68f20-127">This value must match the dimension count of *InputTensor* and *OutputTensor*, which has to be 4.</span></span>


`Scales`

<span data-ttu-id="68f20-128">Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="68f20-128">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="68f20-129">Die Skalierungen, die beim Erneutampling der Eingabe angewendet werden, wobei > 1 das Bild hochskaliert und < 1 das Bild für diese Dimension herunterskaliert.</span><span class="sxs-lookup"><span data-stu-id="68f20-129">The scales to apply when resampling the input, where scales > 1 scale up the image and scales < 1 scale down the image for that dimension.</span></span> <span data-ttu-id="68f20-130">Beachten Sie, dass die Skalierungen nicht genau sein `OutputSize / InputSize` müssen.</span><span class="sxs-lookup"><span data-stu-id="68f20-130">Note that the scales don't need to be exactly `OutputSize / InputSize`.</span></span> <span data-ttu-id="68f20-131">Wenn die Eingabe nach der Skalierung größer als die Ausgabegrenze ist, wird sie auf die Ausgabegröße zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="68f20-131">If the input after scaling is larger than the output bound, then we crop it to the output size.</span></span> <span data-ttu-id="68f20-132">Wenn die Eingabe nach der Skalierung hingegen kleiner als die Ausgabegrenze ist, werden die Ausgaberänder gebunden.</span><span class="sxs-lookup"><span data-stu-id="68f20-132">On the other hand, if the input after scaling is smaller than the output bound, the output edges are clamped.</span></span>


`InputPixelOffsets`

<span data-ttu-id="68f20-133">Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="68f20-133">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="68f20-134">Die Offsets, die vor dem Erneutampling auf die Eingabepixel angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="68f20-134">The offsets to apply to the input pixels before resampling.</span></span> <span data-ttu-id="68f20-135">Wenn dieser Wert ist, wird die linke obere Ecke des Pixels anstelle seines Mittelpunkts verwendet, was in der Regel nicht das `0` erwartete Ergebnis ergeben wird.</span><span class="sxs-lookup"><span data-stu-id="68f20-135">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="68f20-136">Um das Bild mithilfe des Mittelpunkts der Pixel neu zu sampeln und das gleiche Verhalten wie [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)zu erhalten, muss dieser Wert `0.5` sein.</span><span class="sxs-lookup"><span data-stu-id="68f20-136">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `0.5`.</span></span>


`OutputPixelOffsets`

<span data-ttu-id="68f20-137">Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="68f20-137">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="68f20-138">Die Offsets, die nach dem Resampling auf die Ausgabepixel angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="68f20-138">The offsets to apply to the output pixels after resampling.</span></span> <span data-ttu-id="68f20-139">Wenn dieser Wert ist, wird die linke obere Ecke des Pixels anstelle seines Mittelpunkts verwendet, was in der Regel nicht das `0` erwartete Ergebnis ergeben wird.</span><span class="sxs-lookup"><span data-stu-id="68f20-139">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="68f20-140">Um das Bild mithilfe des Mittelpunkts der Pixel neu zu sampeln und das gleiche Verhalten wie [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)zu erhalten, muss dieser Wert `-0.5` sein.</span><span class="sxs-lookup"><span data-stu-id="68f20-140">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `-0.5`.</span></span>


## <a name="remarks"></a><span data-ttu-id="68f20-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68f20-141">Remarks</span></span>
<span data-ttu-id="68f20-142">Wenn *inputPixelOffsets* auf 0,5 und *OutputPixelOffsets* auf -0,5 festgelegt sind, entspricht dieser Operator DML_RESAMPLE_OPERATOR_DESC [.](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="68f20-142">When the *InputPixelOffsets* are set to 0.5, and the *OutputPixelOffsets* are set to -0.5, this operator is equivalent to [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="68f20-143">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="68f20-143">Availability</span></span>
<span data-ttu-id="68f20-144">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="68f20-144">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="68f20-145">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="68f20-145">Tensor constraints</span></span>
<span data-ttu-id="68f20-146">*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="68f20-146">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="68f20-147">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="68f20-147">Tensor support</span></span>
| <span data-ttu-id="68f20-148">Tensor</span><span class="sxs-lookup"><span data-stu-id="68f20-148">Tensor</span></span> | <span data-ttu-id="68f20-149">Typ</span><span class="sxs-lookup"><span data-stu-id="68f20-149">Kind</span></span> | <span data-ttu-id="68f20-150">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="68f20-150">Supported dimension counts</span></span> | <span data-ttu-id="68f20-151">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="68f20-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="68f20-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="68f20-152">InputTensor</span></span> | <span data-ttu-id="68f20-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="68f20-153">Input</span></span> | <span data-ttu-id="68f20-154">4</span><span class="sxs-lookup"><span data-stu-id="68f20-154">4</span></span> | <span data-ttu-id="68f20-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="68f20-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="68f20-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="68f20-156">OutputTensor</span></span> | <span data-ttu-id="68f20-157">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="68f20-157">Output</span></span> | <span data-ttu-id="68f20-158">4</span><span class="sxs-lookup"><span data-stu-id="68f20-158">4</span></span> | <span data-ttu-id="68f20-159">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="68f20-159">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="68f20-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68f20-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="68f20-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="68f20-161">**Header**</span></span> | <span data-ttu-id="68f20-162">directml.h</span><span class="sxs-lookup"><span data-stu-id="68f20-162">directml.h</span></span> |