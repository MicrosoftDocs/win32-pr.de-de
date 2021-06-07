---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Führt eine Konvolution des *FilterTensor mit* dem *InputTensor aus.* Dieser Operator führt die Vorwärtskonvolution für quantisierte Daten aus. Dieser Operator entspricht mathematisch der Dequantisierung der Eingaben, der Konvierung und der anschließenden Quantisierung der Ausgabe.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 5b98e1f57268cab70c2fb672991bce3d67419db8
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417235"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="76b4f-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="76b4f-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="76b4f-106">Führt eine Konvolution des *FilterTensor mit* dem *InputTensor aus.*</span><span class="sxs-lookup"><span data-stu-id="76b4f-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="76b4f-107">Dieser Operator führt die Vorwärtskonvolution für quantisierte Daten aus.</span><span class="sxs-lookup"><span data-stu-id="76b4f-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="76b4f-108">Dieser Operator entspricht mathematisch der Dequantisierung der Eingaben, der Konvierung und der anschließenden Quantisierung der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="76b4f-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="76b4f-109">Die von diesem Operator verwendeten linearen Quantisierungsfunktionen sind die linearen Quantisierungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="76b4f-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="76b4f-110">Dequantize-Funktion</span><span class="sxs-lookup"><span data-stu-id="76b4f-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="76b4f-111">Quantize-Funktion</span><span class="sxs-lookup"><span data-stu-id="76b4f-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="76b4f-112">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="76b4f-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="76b4f-113">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="76b4f-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="76b4f-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="76b4f-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a><span data-ttu-id="76b4f-115">Member</span><span class="sxs-lookup"><span data-stu-id="76b4f-115">Members</span></span>

`InputTensor`

<span data-ttu-id="76b4f-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76b4f-117">Ein Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="76b4f-117">A tensor containing the input data.</span></span> <span data-ttu-id="76b4f-118">Die erwarteten Dimensionen des *InputTensor sind* `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="76b4f-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="76b4f-119">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76b4f-120">Ein Tensor, der die Eingabeskalierdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="76b4f-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="76b4f-121">Die erwarteten Dimensionen von `InputScaleTensor` sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="76b4f-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="76b4f-122">Dieser Skalierungswert wird zum Dequantisieren der Eingabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="76b4f-123">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76b4f-124">Ein optionaler Tensor, der die Nullpunktdaten der Eingabe enthält.</span><span class="sxs-lookup"><span data-stu-id="76b4f-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="76b4f-125">Die erwarteten Dimensionen des *InputZeroPointTensor sind* `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="76b4f-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="76b4f-126">Dieser Nullpunktwert wird zum Dequantisieren der Eingabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="76b4f-127">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76b4f-128">Ein Tensor, der die Filterdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="76b4f-128">A tensor containing the filter data.</span></span> <span data-ttu-id="76b4f-129">Die erwarteten Dimensionen des *FilterTensor sind* `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="76b4f-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="76b4f-130">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76b4f-131">Ein Tensor, der die Filterskalierdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="76b4f-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="76b4f-132">Die erwarteten Dimensionen von sind `FilterScaleTensor` , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` Quantisierung pro Kanal erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="76b4f-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="76b4f-133">Dieser Skalierungswert wird zum Dequantisieren der Filterwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="76b4f-134">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76b4f-135">Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="76b4f-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="76b4f-136">Die erwarteten Dimensionen des *FilterZeroPointTensor* sind , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine Quantisierung pro Kanal `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="76b4f-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="76b4f-137">Dieser Nullpunktwert wird zum Dequantisieren der Filterwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="76b4f-138">Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76b4f-139">Ein Tensor, der die Biasdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="76b4f-139">A tensor containing the bias data.</span></span> <span data-ttu-id="76b4f-140">Der Bias-Tensor ist ein Tensor, der Daten enthält, die über den Ausgabetensor am Ende der Konvolution übertragen werden, der dem Ergebnis hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="76b4f-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="76b4f-141">Die erwarteten Dimensionen des BiasTensor sind `{ 1, OutputChannelCount, 1, 1 }` für 4D.</span><span class="sxs-lookup"><span data-stu-id="76b4f-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="76b4f-142">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76b4f-143">Ein Tensor, der die Ausgabeskalierdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="76b4f-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="76b4f-144">Die erwarteten Dimensionen von OutputScaleTensor sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="76b4f-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="76b4f-145">Dieser Eingabeskalawert wird zum Quantisieren der Konvolutionsausgabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="76b4f-146">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76b4f-147">Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="76b4f-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="76b4f-148">Die erwarteten Dimensionen von OutputZeroPointTensor sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="76b4f-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="76b4f-149">Dieser Nullpunktwert der Eingabe wird zum Quantisieren der Konvolution der Ausgabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="76b4f-150">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76b4f-151">Ein Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-151">A tensor to write the results to.</span></span> <span data-ttu-id="76b4f-152">Die erwarteten Dimensionen des OutputTensor sind `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="76b4f-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="76b4f-153">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="76b4f-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="76b4f-154">Die Anzahl der räumlichen Dimensionen für den Konvolutionsvorgang.</span><span class="sxs-lookup"><span data-stu-id="76b4f-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="76b4f-155">Räumliche Dimensionen sind die unteren Dimensionen des Konvolutionsfilter-Tensors *FilterTensor.*</span><span class="sxs-lookup"><span data-stu-id="76b4f-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="76b4f-156">Dieser Wert bestimmt auch die Größe der *Arrays Strides,* *Dilations,* *StartPadding* und *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="76b4f-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="76b4f-157">Nur der Wert 2 wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="76b4f-158">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-158">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76b4f-159">Die Schritte der Konvolutionsoperation.</span><span class="sxs-lookup"><span data-stu-id="76b4f-159">The strides of the convolution operation.</span></span> <span data-ttu-id="76b4f-160">Diese Schritte werden auf den Konvolutionsfilter angewendet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="76b4f-161">Sie sind getrennt von den Tensorschritten, [](/windows/win32/api/directml/ns-directml-dml_tensor_desc)die in DML_TENSOR_DESC.</span><span class="sxs-lookup"><span data-stu-id="76b4f-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="76b4f-162">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-162">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76b4f-163">Die Dilationen der Konvolutionsoperation.</span><span class="sxs-lookup"><span data-stu-id="76b4f-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="76b4f-164">Dilationen sind Schritte, die auf die Elemente des Filterkernels angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="76b4f-165">Dies hat den Effekt, dass ein größerer Filterkernel simuliert wird, indem die internen Filterkernelelemente mit Nullen aufschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="76b4f-166">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-166">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76b4f-167">Die Auf padding-Werte, die auf den Anfang jeder räumlichen Dimension des Filters und den Eingabetensor des Konvolutionsvorgang angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76b4f-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="76b4f-168">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="76b4f-168">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76b4f-169">Die Auf padding-Werte, die auf das Ende jeder räumlichen Dimension des Filters und des Eingabetensors des Konvolutionsvorgang angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76b4f-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="76b4f-170">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="76b4f-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="76b4f-171">Die Anzahl der Gruppen, in die der Konvolutionsvorgang unterteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76b4f-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="76b4f-172">*GroupCount* kann verwendet werden, um eine tiefenweise Konvolution zu erreichen, indem *GroupCount* auf die Anzahl der Eingabekanäle gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="76b4f-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="76b4f-173">Dadurch wird die Konvolution in eine separate Konvolution pro Eingabekanal unterteilt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="76b4f-174">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="76b4f-174">Availability</span></span>
<span data-ttu-id="76b4f-175">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="76b4f-176">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="76b4f-176">Tensor constraints</span></span>
* <span data-ttu-id="76b4f-177">*FilterTensor und* *FilterZeroPointTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="76b4f-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="76b4f-178">*InputTensor* und *InputZeroPointTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="76b4f-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="76b4f-179">*OutputTensor* und `OutputZeroPointTensor` müssen den gleichen Datentyp *haben.*</span><span class="sxs-lookup"><span data-stu-id="76b4f-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="76b4f-180">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="76b4f-180">Tensor support</span></span>
| <span data-ttu-id="76b4f-181">Tensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-181">Tensor</span></span> | <span data-ttu-id="76b4f-182">Typ</span><span class="sxs-lookup"><span data-stu-id="76b4f-182">Kind</span></span> | <span data-ttu-id="76b4f-183">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="76b4f-183">Supported dimension counts</span></span> | <span data-ttu-id="76b4f-184">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="76b4f-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="76b4f-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-185">InputTensor</span></span> | <span data-ttu-id="76b4f-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="76b4f-186">Input</span></span> | <span data-ttu-id="76b4f-187">4</span><span class="sxs-lookup"><span data-stu-id="76b4f-187">4</span></span> | <span data-ttu-id="76b4f-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="76b4f-188">INT8, UINT8</span></span> |
| <span data-ttu-id="76b4f-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-189">InputScaleTensor</span></span> | <span data-ttu-id="76b4f-190">Eingabe</span><span class="sxs-lookup"><span data-stu-id="76b4f-190">Input</span></span> | <span data-ttu-id="76b4f-191">4</span><span class="sxs-lookup"><span data-stu-id="76b4f-191">4</span></span> | <span data-ttu-id="76b4f-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="76b4f-192">FLOAT32</span></span> |
| <span data-ttu-id="76b4f-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-193">InputZeroPointTensor</span></span> | <span data-ttu-id="76b4f-194">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="76b4f-194">Optional input</span></span> | <span data-ttu-id="76b4f-195">4</span><span class="sxs-lookup"><span data-stu-id="76b4f-195">4</span></span> | <span data-ttu-id="76b4f-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="76b4f-196">INT8, UINT8</span></span> |
| <span data-ttu-id="76b4f-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-197">FilterTensor</span></span> | <span data-ttu-id="76b4f-198">Eingabe</span><span class="sxs-lookup"><span data-stu-id="76b4f-198">Input</span></span> | <span data-ttu-id="76b4f-199">4</span><span class="sxs-lookup"><span data-stu-id="76b4f-199">4</span></span> | <span data-ttu-id="76b4f-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="76b4f-200">INT8, UINT8</span></span> |
| <span data-ttu-id="76b4f-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-201">FilterScaleTensor</span></span> | <span data-ttu-id="76b4f-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="76b4f-202">Input</span></span> | <span data-ttu-id="76b4f-203">4</span><span class="sxs-lookup"><span data-stu-id="76b4f-203">4</span></span> | <span data-ttu-id="76b4f-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="76b4f-204">FLOAT32</span></span> |
| <span data-ttu-id="76b4f-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="76b4f-206">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="76b4f-206">Optional input</span></span> | <span data-ttu-id="76b4f-207">4</span><span class="sxs-lookup"><span data-stu-id="76b4f-207">4</span></span> | <span data-ttu-id="76b4f-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="76b4f-208">INT8, UINT8</span></span> |
| <span data-ttu-id="76b4f-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-209">BiasTensor</span></span> | <span data-ttu-id="76b4f-210">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="76b4f-210">Optional input</span></span> | <span data-ttu-id="76b4f-211">4</span><span class="sxs-lookup"><span data-stu-id="76b4f-211">4</span></span> | <span data-ttu-id="76b4f-212">INT32</span><span class="sxs-lookup"><span data-stu-id="76b4f-212">INT32</span></span> |
| <span data-ttu-id="76b4f-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-213">OutputScaleTensor</span></span> | <span data-ttu-id="76b4f-214">Eingabe</span><span class="sxs-lookup"><span data-stu-id="76b4f-214">Input</span></span> | <span data-ttu-id="76b4f-215">4</span><span class="sxs-lookup"><span data-stu-id="76b4f-215">4</span></span> | <span data-ttu-id="76b4f-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="76b4f-216">FLOAT32</span></span> |
| <span data-ttu-id="76b4f-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="76b4f-218">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="76b4f-218">Optional input</span></span> | <span data-ttu-id="76b4f-219">4</span><span class="sxs-lookup"><span data-stu-id="76b4f-219">4</span></span> | <span data-ttu-id="76b4f-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="76b4f-220">INT8, UINT8</span></span> |
| <span data-ttu-id="76b4f-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="76b4f-221">OutputTensor</span></span> | <span data-ttu-id="76b4f-222">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="76b4f-222">Output</span></span> | <span data-ttu-id="76b4f-223">4</span><span class="sxs-lookup"><span data-stu-id="76b4f-223">4</span></span> | <span data-ttu-id="76b4f-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="76b4f-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="76b4f-225">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="76b4f-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="76b4f-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="76b4f-226">**Header**</span></span> | <span data-ttu-id="76b4f-227">directml.h</span><span class="sxs-lookup"><span data-stu-id="76b4f-227">directml.h</span></span> |