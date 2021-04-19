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
# <a name="dml_resample1_operator_desc-structure-directmlh"></a><span data-ttu-id="59ef3-104">DML_RESAMPLE1_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="59ef3-104">DML_RESAMPLE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="59ef3-105">Gibt Elemente aus der Quell-zum Ziel Mandanten erneut aus, wobei die Skalierungsfaktoren verwendet werden, um die Ziel-tensorflow-Größe zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="59ef3-105">Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size.</span></span> <span data-ttu-id="59ef3-106">Sie können einen linearen oder nächstgelegenen Interpolations Modus verwenden.</span><span class="sxs-lookup"><span data-stu-id="59ef3-106">You can use a linear or nearest-neighbor interpolation mode.</span></span> <span data-ttu-id="59ef3-107">Der-Operator unterstützt Interpolationen über mehrere Dimensionen, nicht nur über 2D.</span><span class="sxs-lookup"><span data-stu-id="59ef3-107">The operator supports interpolation across multiple dimensions, not just 2D.</span></span> <span data-ttu-id="59ef3-108">Sie können also die gleiche räumliche Größe beibehalten, aber über Kanäle oder Batches hinweg interpolieren.</span><span class="sxs-lookup"><span data-stu-id="59ef3-108">So you can keep the same spatial size, but interpolate across channels or across batches.</span></span> <span data-ttu-id="59ef3-109">Die Beziehung zwischen der Eingabe-und der Ausgabe Koordinate lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="59ef3-109">The relationship between the input and output coordinates is the following.</span></span>

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> <span data-ttu-id="59ef3-110">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="59ef3-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="59ef3-111">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="59ef3-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="59ef3-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="59ef3-112">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="59ef3-113">Member</span><span class="sxs-lookup"><span data-stu-id="59ef3-113">Members</span></span>

`InputTensor`

<span data-ttu-id="59ef3-114">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="59ef3-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="59ef3-115">Der tensorflow, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="59ef3-115">The tensor containing the input data.</span></span>


`OutputTensor`

<span data-ttu-id="59ef3-116">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="59ef3-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="59ef3-117">Der tensorflow, in den die Ausgabedaten geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59ef3-117">The tensor to write the output data to.</span></span>


`InterpolationMode`

<span data-ttu-id="59ef3-118">Typ: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="59ef3-118">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="59ef3-119">Dieses Feld bestimmt die Art der Interpolations, mit der Ausgabe Pixel ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="59ef3-119">This field determines the kind of interpolation used to choose output pixels.</span></span>

- <span data-ttu-id="59ef3-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span><span class="sxs-lookup"><span data-stu-id="59ef3-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span></span> <span data-ttu-id="59ef3-121">Verwendet den *nächstgelegenen Nachbar* Algorithmus, der das Eingabe Element auswählt, das dem entsprechenden Pixel Center für jedes Output-Element am nächsten ist.</span><span class="sxs-lookup"><span data-stu-id="59ef3-121">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>

- <span data-ttu-id="59ef3-122">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="59ef3-122">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="59ef3-123">Verwendet den *vierlinear* -Algorithmus, der das Output-Element berechnet, indem der gewichtete Durchschnitt der zwei nächstgelegenen benachbarten Eingabeelemente pro Dimension ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59ef3-123">Uses the *Quadrilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="59ef3-124">Da alle vier Dimensionen neu erstellt werden können, wird der gewichtete Durchschnitt für jedes Output-Element für insgesamt 16 Eingabeelemente berechnet.</span><span class="sxs-lookup"><span data-stu-id="59ef3-124">Since all 4 dimensions can be resampled, the weighted average is computed on a total of 16 input elements for each output element.</span></span>


`DimensionCount`

<span data-ttu-id="59ef3-125">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="59ef3-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="59ef3-126">Die Anzahl der Werte in den Arrays, die *skaliert*, *inputpixeloffsets* und *outputpixeloffsets* auf zeigen.</span><span class="sxs-lookup"><span data-stu-id="59ef3-126">The number of values in the arrays that *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* point to.</span></span> <span data-ttu-id="59ef3-127">Dieser Wert muss mit der Dimensions Anzahl von *inputtensor* und *outputtensor* identisch sein, die 4 sein muss.</span><span class="sxs-lookup"><span data-stu-id="59ef3-127">This value must match the dimension count of *InputTensor* and *OutputTensor*, which has to be 4.</span></span>


`Scales`

<span data-ttu-id="59ef3-128">Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="59ef3-128">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="59ef3-129">Die Skalierungen, die beim erneuten Sampling der Eingabe angewendet werden, wobei Skalierung > 1 das Image zentral hochskalieren und Skalieren < 1 skalieren Sie das Bild für diese Dimension herunter.</span><span class="sxs-lookup"><span data-stu-id="59ef3-129">The scales to apply when resampling the input, where scales > 1 scale up the image and scales < 1 scale down the image for that dimension.</span></span> <span data-ttu-id="59ef3-130">Beachten Sie, dass die Skalen nicht exakt sein müssen `OutputSize / InputSize` .</span><span class="sxs-lookup"><span data-stu-id="59ef3-130">Note that the scales don't need to be exactly `OutputSize / InputSize`.</span></span> <span data-ttu-id="59ef3-131">Wenn die Eingabe nach der Skalierung größer als die Ausgabe Grenze ist, wird Sie in die Ausgabegröße übertragen.</span><span class="sxs-lookup"><span data-stu-id="59ef3-131">If the input after scaling is larger than the output bound, then we crop it to the output size.</span></span> <span data-ttu-id="59ef3-132">Wenn die Eingabe nach der Skalierung jedoch kleiner als die Ausgabe Grenze ist, werden die Ausgabe Kanten geklammert.</span><span class="sxs-lookup"><span data-stu-id="59ef3-132">On the other hand, if the input after scaling is smaller than the output bound, the output edges are clamped.</span></span>


`InputPixelOffsets`

<span data-ttu-id="59ef3-133">Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="59ef3-133">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="59ef3-134">Die Offsets, die vor dem erneuten Sampling auf die Eingabe Pixel angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59ef3-134">The offsets to apply to the input pixels before resampling.</span></span> <span data-ttu-id="59ef3-135">Wenn dieser Wert ist `0` , wird die linke obere Ecke des Pixels anstelle der Mitte verwendet, die in der Regel nicht das erwartete Ergebnis liefert.</span><span class="sxs-lookup"><span data-stu-id="59ef3-135">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="59ef3-136">Um das Bild mithilfe der Mitte der Pixel neu zu formatieren und das gleiche Verhalten wie [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)zu erzielen, muss dieser Wert lauten `0.5` .</span><span class="sxs-lookup"><span data-stu-id="59ef3-136">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `0.5`.</span></span>


`OutputPixelOffsets`

<span data-ttu-id="59ef3-137">Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="59ef3-137">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="59ef3-138">Die Offsets, die nach dem erneuten Sampling auf die Ausgabe Pixel angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59ef3-138">The offsets to apply to the output pixels after resampling.</span></span> <span data-ttu-id="59ef3-139">Wenn dieser Wert ist `0` , wird die linke obere Ecke des Pixels anstelle der Mitte verwendet, die in der Regel nicht das erwartete Ergebnis liefert.</span><span class="sxs-lookup"><span data-stu-id="59ef3-139">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="59ef3-140">Um das Bild mithilfe der Mitte der Pixel neu zu formatieren und das gleiche Verhalten wie [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)zu erzielen, muss dieser Wert lauten `-0.5` .</span><span class="sxs-lookup"><span data-stu-id="59ef3-140">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `-0.5`.</span></span>


## <a name="remarks"></a><span data-ttu-id="59ef3-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59ef3-141">Remarks</span></span>
<span data-ttu-id="59ef3-142">Wenn *inputpixeloffsets* auf 0,5 und *outputpixeloffsets* auf-0,5 festgelegt sind, entspricht dieser Operator [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="59ef3-142">When the *InputPixelOffsets* are set to 0.5, and the *OutputPixelOffsets* are set to -0.5, this operator is equivalent to [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="59ef3-143">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="59ef3-143">Availability</span></span>
<span data-ttu-id="59ef3-144">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="59ef3-144">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="59ef3-145">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="59ef3-145">Tensor constraints</span></span>
<span data-ttu-id="59ef3-146">*Inputtensor* und *outputtensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="59ef3-146">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="59ef3-147">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="59ef3-147">Tensor support</span></span>
| <span data-ttu-id="59ef3-148">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="59ef3-148">Tensor</span></span> | <span data-ttu-id="59ef3-149">Typ</span><span class="sxs-lookup"><span data-stu-id="59ef3-149">Kind</span></span> | <span data-ttu-id="59ef3-150">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="59ef3-150">Supported dimension counts</span></span> | <span data-ttu-id="59ef3-151">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="59ef3-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="59ef3-152">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="59ef3-152">InputTensor</span></span> | <span data-ttu-id="59ef3-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59ef3-153">Input</span></span> | <span data-ttu-id="59ef3-154">4</span><span class="sxs-lookup"><span data-stu-id="59ef3-154">4</span></span> | <span data-ttu-id="59ef3-155">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="59ef3-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="59ef3-156">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="59ef3-156">OutputTensor</span></span> | <span data-ttu-id="59ef3-157">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="59ef3-157">Output</span></span> | <span data-ttu-id="59ef3-158">4</span><span class="sxs-lookup"><span data-stu-id="59ef3-158">4</span></span> | <span data-ttu-id="59ef3-159">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="59ef3-159">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="59ef3-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59ef3-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="59ef3-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="59ef3-161">**Header**</span></span> | <span data-ttu-id="59ef3-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="59ef3-162">directml.h</span></span> |