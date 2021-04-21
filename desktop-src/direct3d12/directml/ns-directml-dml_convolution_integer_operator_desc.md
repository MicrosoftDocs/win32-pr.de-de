---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Führt eine Konvolution des *FilterTensor mit* dem *InputTensor aus.* Dieser Operator führt die Vorwärtskonvolution für ganzzahlige Daten aus.
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
ms.openlocfilehash: 07406155be9ae5f78fbf5f3b7fcd750aa4631dbc
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803375"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="64ae1-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="64ae1-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="64ae1-105">Führt eine Konvolution des *FilterTensor mit* dem *InputTensor aus.*</span><span class="sxs-lookup"><span data-stu-id="64ae1-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="64ae1-106">Dieser Operator führt die Vorwärtskonvolution für ganzzahlige Daten aus.</span><span class="sxs-lookup"><span data-stu-id="64ae1-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="64ae1-107">Optionale Nullpunkt-Tensoren können auch verwendet werden, um Nullpunktwerte vom Eingabe- und Filtertensor zu subtrahieren.</span><span class="sxs-lookup"><span data-stu-id="64ae1-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64ae1-108">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="64ae1-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="64ae1-109">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="64ae1-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="64ae1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="64ae1-110">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="64ae1-111">Member</span><span class="sxs-lookup"><span data-stu-id="64ae1-111">Members</span></span>

`InputTensor`

<span data-ttu-id="64ae1-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64ae1-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64ae1-113">Ein Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="64ae1-113">A tensor containing the input data.</span></span> <span data-ttu-id="64ae1-114">Die erwarteten Dimensionen des *InputTensor sind* `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="64ae1-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="64ae1-115">Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64ae1-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64ae1-116">Ein optionaler Tensor, der die Nullpunktdaten der Eingabe enthält.</span><span class="sxs-lookup"><span data-stu-id="64ae1-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="64ae1-117">Die erwarteten Dimensionen des *InputZeroPointTensor sind* `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="64ae1-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="64ae1-118">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64ae1-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64ae1-119">Ein Tensor, der die Filterdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="64ae1-119">A tensor containing the filter data.</span></span> <span data-ttu-id="64ae1-120">Die erwarteten Dimensionen des *FilterTensor sind* `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="64ae1-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="64ae1-121">Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64ae1-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64ae1-122">Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="64ae1-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="64ae1-123">Die erwarteten Dimensionen des *FilterZeroPointTensor* sind , wenn eine Tensorquantisierung erforderlich ist oder wenn eine Quantisierung pro Kanal `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="64ae1-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="64ae1-124">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64ae1-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64ae1-125">Der Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64ae1-125">The tensor to write the results to.</span></span> <span data-ttu-id="64ae1-126">Die erwarteten Dimensionen des *OutputTensor* sind `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="64ae1-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="64ae1-127">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="64ae1-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="64ae1-128">Die Anzahl der räumlichen Dimensionen für den Konvolutionsvorgang.</span><span class="sxs-lookup"><span data-stu-id="64ae1-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="64ae1-129">Räumliche Dimensionen sind die unteren Dimensionen der Konvolution *FilterTensor*.</span><span class="sxs-lookup"><span data-stu-id="64ae1-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="64ae1-130">Dieser Wert bestimmt auch die Größe der Arrays *Strides*, *Dilations*, *StartPadding* und *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="64ae1-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="64ae1-131">Es wird nur der Wert 2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64ae1-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="64ae1-132">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="64ae1-132">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="64ae1-133">Ein Array, das die Schritte des Konvolutionsvorgangs enthält.</span><span class="sxs-lookup"><span data-stu-id="64ae1-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="64ae1-134">Diese Schritte werden auf den Konvolutionsfilter angewendet.</span><span class="sxs-lookup"><span data-stu-id="64ae1-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="64ae1-135">Sie sind von den Tensorschritten getrennt, die in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="64ae1-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="64ae1-136">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="64ae1-136">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="64ae1-137">Ein Array, das die Sortierungen des Konvolutionsvorgangs enthält.</span><span class="sxs-lookup"><span data-stu-id="64ae1-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="64ae1-138">Dilations sind Schritte, die auf die Elemente des Filterkernels angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="64ae1-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="64ae1-139">Dies hat den Effekt, dass ein größerer Filterkernel simuliert wird, indem die internen Filterkernelelemente mit Nullen auffüllt werden.</span><span class="sxs-lookup"><span data-stu-id="64ae1-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="64ae1-140">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="64ae1-140">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="64ae1-141">Ein Array, das die Auffüllwerte enthält, die am Anfang jeder räumlichen Dimension des Filters und eingabe tensor des Konvolutionsvorgangs angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64ae1-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="64ae1-142">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="64ae1-142">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="64ae1-143">Ein Array, das die Auffüllwerte enthält, die am Ende jeder räumlichen Dimension des Filters und eingabe tensor des Konvolutionsvorgangs angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64ae1-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="64ae1-144">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="64ae1-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="64ae1-145">Die Anzahl der Gruppen, in die der Konvolutionsvorgang unterteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64ae1-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="64ae1-146">*GroupCount* kann verwendet werden, um eine tiefenweise Konvolution zu erreichen, indem *GroupCount* auf die Anzahl der Eingabekanäle gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="64ae1-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="64ae1-147">Dadurch wird die Konvolution in eine separate Konvolution pro Eingabekanal unterteilt.</span><span class="sxs-lookup"><span data-stu-id="64ae1-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="64ae1-148">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="64ae1-148">Availability</span></span>
<span data-ttu-id="64ae1-149">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="64ae1-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="64ae1-150">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="64ae1-150">Tensor constraints</span></span>
* <span data-ttu-id="64ae1-151">*FilterTensor und* *FilterZeroPointTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="64ae1-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="64ae1-152">*InputTensor* und *InputZeroPointTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="64ae1-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="64ae1-153">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="64ae1-153">Tensor support</span></span>
| <span data-ttu-id="64ae1-154">Tensor</span><span class="sxs-lookup"><span data-stu-id="64ae1-154">Tensor</span></span> | <span data-ttu-id="64ae1-155">Typ</span><span class="sxs-lookup"><span data-stu-id="64ae1-155">Kind</span></span> | <span data-ttu-id="64ae1-156">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="64ae1-156">Dimensions</span></span> | <span data-ttu-id="64ae1-157">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="64ae1-157">Supported dimension counts</span></span> | <span data-ttu-id="64ae1-158">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="64ae1-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="64ae1-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="64ae1-159">InputTensor</span></span> | <span data-ttu-id="64ae1-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64ae1-160">Input</span></span> | <span data-ttu-id="64ae1-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="64ae1-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="64ae1-162">4</span><span class="sxs-lookup"><span data-stu-id="64ae1-162">4</span></span> | <span data-ttu-id="64ae1-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="64ae1-163">INT8, UINT8</span></span> |
| <span data-ttu-id="64ae1-164">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="64ae1-164">InputZeroPointTensor</span></span> | <span data-ttu-id="64ae1-165">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="64ae1-165">Optional input</span></span> | <span data-ttu-id="64ae1-166">{ 1, 1, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="64ae1-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="64ae1-167">4</span><span class="sxs-lookup"><span data-stu-id="64ae1-167">4</span></span> | <span data-ttu-id="64ae1-168">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="64ae1-168">INT8, UINT8</span></span> |
| <span data-ttu-id="64ae1-169">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="64ae1-169">FilterTensor</span></span> | <span data-ttu-id="64ae1-170">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64ae1-170">Input</span></span> | <span data-ttu-id="64ae1-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span><span class="sxs-lookup"><span data-stu-id="64ae1-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="64ae1-172">4</span><span class="sxs-lookup"><span data-stu-id="64ae1-172">4</span></span> | <span data-ttu-id="64ae1-173">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="64ae1-173">INT8, UINT8</span></span> |
| <span data-ttu-id="64ae1-174">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="64ae1-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="64ae1-175">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="64ae1-175">Optional input</span></span> | <span data-ttu-id="64ae1-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="64ae1-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="64ae1-177">4</span><span class="sxs-lookup"><span data-stu-id="64ae1-177">4</span></span> | <span data-ttu-id="64ae1-178">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="64ae1-178">INT8, UINT8</span></span> |
| <span data-ttu-id="64ae1-179">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="64ae1-179">OutputTensor</span></span> | <span data-ttu-id="64ae1-180">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="64ae1-180">Output</span></span> | <span data-ttu-id="64ae1-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="64ae1-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="64ae1-182">4</span><span class="sxs-lookup"><span data-stu-id="64ae1-182">4</span></span> | <span data-ttu-id="64ae1-183">INT32</span><span class="sxs-lookup"><span data-stu-id="64ae1-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="64ae1-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64ae1-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="64ae1-185">**Header**</span><span class="sxs-lookup"><span data-stu-id="64ae1-185">**Header**</span></span> | <span data-ttu-id="64ae1-186">directml.h</span><span class="sxs-lookup"><span data-stu-id="64ae1-186">directml.h</span></span> |