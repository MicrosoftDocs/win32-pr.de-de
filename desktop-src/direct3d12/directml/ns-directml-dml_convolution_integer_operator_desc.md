---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Führt eine Konvolution des *FilterTensor* mit dem *InputTensor aus.* Dieser Operator führt die Vorwärtskonvolution für ganzzahlige Daten aus.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f4045598dd1aa050479fec8e5732fe5c0a4e77ee
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550416"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="aaa80-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="aaa80-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="aaa80-105">Führt eine Konvolution des *FilterTensor* mit dem *InputTensor aus.*</span><span class="sxs-lookup"><span data-stu-id="aaa80-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="aaa80-106">Dieser Operator führt die Vorwärtskonvolution für ganzzahlige Daten aus.</span><span class="sxs-lookup"><span data-stu-id="aaa80-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="aaa80-107">Optionale Nullpunkt-Tensoren können auch verwendet werden, um Nullpunktwerte vom Eingabe- und Filter-Tensor zu subtrahieren.</span><span class="sxs-lookup"><span data-stu-id="aaa80-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aaa80-108">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="aaa80-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="aaa80-109">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="aaa80-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa80-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaa80-110">Syntax</span></span>
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```

## <a name="members"></a><span data-ttu-id="aaa80-111">Member</span><span class="sxs-lookup"><span data-stu-id="aaa80-111">Members</span></span>

`InputTensor`

<span data-ttu-id="aaa80-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aaa80-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aaa80-113">Ein Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa80-113">A tensor containing the input data.</span></span> <span data-ttu-id="aaa80-114">Die erwarteten Dimensionen des *InputTensor* sind `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="aaa80-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="aaa80-115">Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aaa80-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aaa80-116">Ein optionaler Tensor, der die Eingabe-Nullpunktdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa80-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="aaa80-117">Die erwarteten Dimensionen von *InputZeroPointTensor* sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="aaa80-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="aaa80-118">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aaa80-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aaa80-119">Ein Tensor, der die Filterdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa80-119">A tensor containing the filter data.</span></span> <span data-ttu-id="aaa80-120">Die erwarteten Dimensionen von *FilterTensor* sind `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="aaa80-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="aaa80-121">Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aaa80-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aaa80-122">Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa80-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="aaa80-123">Die erwarteten Dimensionen von *FilterZeroPointTensor* sind `{ 1, 1, 1, 1 }` , wenn eine Tensorquantisierung erforderlich ist, oder wenn eine `{ 1, OutputChannelCount, 1, 1 }` Pro-Kanal-Quantisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="aaa80-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="aaa80-124">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aaa80-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aaa80-125">Der Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="aaa80-125">The tensor to write the results to.</span></span> <span data-ttu-id="aaa80-126">Die erwarteten Dimensionen des *OutputTensor sind* `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="aaa80-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="aaa80-127">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="aaa80-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="aaa80-128">Die Anzahl der räumlichen Dimensionen für den Konvolutionsvorgang.</span><span class="sxs-lookup"><span data-stu-id="aaa80-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="aaa80-129">Räumliche Dimensionen sind die unteren Dimensionen des *Konvolutionsfiltertensors*.</span><span class="sxs-lookup"><span data-stu-id="aaa80-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="aaa80-130">Dieser Wert bestimmt auch die Größe der *Arrays Strides,* *Dilations,* *StartPadding* und *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="aaa80-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="aaa80-131">Nur der Wert 2 wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aaa80-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="aaa80-132">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="aaa80-132">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aaa80-133">Ein Array, das die Schritte des Konvolutionsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa80-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="aaa80-134">Diese Schritte werden auf den Konvolutionsfilter angewendet.</span><span class="sxs-lookup"><span data-stu-id="aaa80-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="aaa80-135">Sie sind getrennt von den Tensorschritten, [](/windows/win32/api/directml/ns-directml-dml_tensor_desc)die in DML_TENSOR_DESC.</span><span class="sxs-lookup"><span data-stu-id="aaa80-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="aaa80-136">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="aaa80-136">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aaa80-137">Ein Array, das die Dilationen des Konvolutionsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa80-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="aaa80-138">Dilationen sind Schritte, die auf die Elemente des Filterkernels angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="aaa80-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="aaa80-139">Dies hat den Effekt, dass ein größerer Filterkernel simuliert wird, indem die internen Filterkernelelemente mit Nullen aufschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="aaa80-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="aaa80-140">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="aaa80-140">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aaa80-141">Ein Array, das die Auf padding-Werte enthält, die am Anfang jeder räumlichen Dimension des Filters und des Eingabetensors des Konvolutionsvorgang angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aaa80-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="aaa80-142">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="aaa80-142">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aaa80-143">Ein Array mit den Auf padding-Werten, die auf das Ende jeder räumlichen Dimension des Filters und des Eingabetensors des Konvolutionsvorgang angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aaa80-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="aaa80-144">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="aaa80-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="aaa80-145">Die Anzahl der Gruppen, in die der Konvolutionsvorgang unterteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aaa80-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="aaa80-146">*GroupCount* kann verwendet werden, um eine tiefenweise Konvolution zu erreichen, indem *GroupCount* auf die Anzahl der Eingabekanäle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="aaa80-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="aaa80-147">Dadurch wird die Konvolution in eine separate Konvolution pro Eingabekanal unterteilt.</span><span class="sxs-lookup"><span data-stu-id="aaa80-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="aaa80-148">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="aaa80-148">Availability</span></span>
<span data-ttu-id="aaa80-149">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="aaa80-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="aaa80-150">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="aaa80-150">Tensor constraints</span></span>
* <span data-ttu-id="aaa80-151">*FilterTensor* und *FilterZeroPointTensor* müssen den gleichen *Datentyp aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="aaa80-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="aaa80-152">*InputTensor* und *InputZeroPointTensor* müssen den gleichen *Datentyp aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="aaa80-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="aaa80-153">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="aaa80-153">Tensor support</span></span>
| <span data-ttu-id="aaa80-154">Tensor</span><span class="sxs-lookup"><span data-stu-id="aaa80-154">Tensor</span></span> | <span data-ttu-id="aaa80-155">Typ</span><span class="sxs-lookup"><span data-stu-id="aaa80-155">Kind</span></span> | <span data-ttu-id="aaa80-156">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="aaa80-156">Dimensions</span></span> | <span data-ttu-id="aaa80-157">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="aaa80-157">Supported dimension counts</span></span> | <span data-ttu-id="aaa80-158">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="aaa80-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="aaa80-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="aaa80-159">InputTensor</span></span> | <span data-ttu-id="aaa80-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaa80-160">Input</span></span> | <span data-ttu-id="aaa80-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="aaa80-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="aaa80-162">4</span><span class="sxs-lookup"><span data-stu-id="aaa80-162">4</span></span> | <span data-ttu-id="aaa80-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="aaa80-163">INT8, UINT8</span></span> |
| <span data-ttu-id="aaa80-164">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="aaa80-164">InputZeroPointTensor</span></span> | <span data-ttu-id="aaa80-165">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaa80-165">Optional input</span></span> | <span data-ttu-id="aaa80-166">{ 1, 1, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="aaa80-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="aaa80-167">4</span><span class="sxs-lookup"><span data-stu-id="aaa80-167">4</span></span> | <span data-ttu-id="aaa80-168">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="aaa80-168">INT8, UINT8</span></span> |
| <span data-ttu-id="aaa80-169">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="aaa80-169">FilterTensor</span></span> | <span data-ttu-id="aaa80-170">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaa80-170">Input</span></span> | <span data-ttu-id="aaa80-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span><span class="sxs-lookup"><span data-stu-id="aaa80-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="aaa80-172">4</span><span class="sxs-lookup"><span data-stu-id="aaa80-172">4</span></span> | <span data-ttu-id="aaa80-173">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="aaa80-173">INT8, UINT8</span></span> |
| <span data-ttu-id="aaa80-174">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="aaa80-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="aaa80-175">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaa80-175">Optional input</span></span> | <span data-ttu-id="aaa80-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="aaa80-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="aaa80-177">4</span><span class="sxs-lookup"><span data-stu-id="aaa80-177">4</span></span> | <span data-ttu-id="aaa80-178">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="aaa80-178">INT8, UINT8</span></span> |
| <span data-ttu-id="aaa80-179">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="aaa80-179">OutputTensor</span></span> | <span data-ttu-id="aaa80-180">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="aaa80-180">Output</span></span> | <span data-ttu-id="aaa80-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="aaa80-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="aaa80-182">4</span><span class="sxs-lookup"><span data-stu-id="aaa80-182">4</span></span> | <span data-ttu-id="aaa80-183">INT32</span><span class="sxs-lookup"><span data-stu-id="aaa80-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="aaa80-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aaa80-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="aaa80-185">**Header**</span><span class="sxs-lookup"><span data-stu-id="aaa80-185">**Header**</span></span> | <span data-ttu-id="aaa80-186">directml.h</span><span class="sxs-lookup"><span data-stu-id="aaa80-186">directml.h</span></span> |