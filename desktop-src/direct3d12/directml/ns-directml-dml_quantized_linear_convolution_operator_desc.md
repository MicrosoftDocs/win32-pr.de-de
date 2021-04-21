---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Führt eine Konvolution des *FilterTensor* mit dem *InputTensor aus.* Dieser Operator führt die Vorwärtskonvolution für quantisierte Daten aus. Dieser Operator entspricht mathematischer Entsprechung der Dequantisierung der Eingaben, der Verschachtelung und der anschließenden Quantisierung der Ausgabe.
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
ms.openlocfilehash: 4dd50d80dfe4ae60e3fe7e67124ef00bfbc7bf2b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803879"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="7a4b2-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="7a4b2-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="7a4b2-106">Führt eine Konvolution des *FilterTensor* mit dem *InputTensor aus.*</span><span class="sxs-lookup"><span data-stu-id="7a4b2-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="7a4b2-107">Dieser Operator führt die Vorwärtskonvolution für quantisierte Daten aus.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="7a4b2-108">Dieser Operator entspricht mathematischer Entsprechung der Dequantisierung der Eingaben, der Verschachtelung und der anschließenden Quantisierung der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="7a4b2-109">Die von diesem Operator verwendeten linearen Quantisierungsfunktionen sind die linearen Quantisierungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="7a4b2-110">Dequantize-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a4b2-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="7a4b2-111">Quantize-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a4b2-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="7a4b2-112">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="7a4b2-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="7a4b2-113">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="7a4b2-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a4b2-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a4b2-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="7a4b2-115">Member</span><span class="sxs-lookup"><span data-stu-id="7a4b2-115">Members</span></span>

`InputTensor`

<span data-ttu-id="7a4b2-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7a4b2-117">Ein Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-117">A tensor containing the input data.</span></span> <span data-ttu-id="7a4b2-118">Die erwarteten Dimensionen des *InputTensor* sind `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="7a4b2-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="7a4b2-119">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7a4b2-120">Ein Tensor, der die Eingabeskalierdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="7a4b2-121">Die erwarteten Dimensionen von `InputScaleTensor` sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="7a4b2-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="7a4b2-122">Dieser Skalierungswert wird zum Dequantisieren der Eingabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="7a4b2-123">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7a4b2-124">Ein optionaler Tensor, der die Nullpunktdaten der Eingabe enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="7a4b2-125">Die erwarteten Dimensionen des *InputZeroPointTensor sind* `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="7a4b2-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="7a4b2-126">Dieser Nullpunktwert wird zum Dequantisieren der Eingabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="7a4b2-127">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7a4b2-128">Ein Tensor, der die Filterdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-128">A tensor containing the filter data.</span></span> <span data-ttu-id="7a4b2-129">Die erwarteten Dimensionen des *FilterTensor sind* `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="7a4b2-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="7a4b2-130">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7a4b2-131">Ein Tensor, der die Filterskalierdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="7a4b2-132">Die erwarteten Dimensionen von sind `FilterScaleTensor` , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` Quantisierung pro Kanal erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="7a4b2-133">Dieser Skalierungswert wird zum Dequantisieren der Filterwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="7a4b2-134">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7a4b2-135">Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="7a4b2-136">Die erwarteten Dimensionen des *FilterZeroPointTensor* sind , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine Quantisierung pro Kanal `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="7a4b2-137">Dieser Nullpunktwert wird zum Dequantisieren der Filterwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="7a4b2-138">Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7a4b2-139">Ein Tensor, der die Biasdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-139">A tensor containing the bias data.</span></span> <span data-ttu-id="7a4b2-140">Der Bias-Tensor ist ein Tensor, der Daten enthält, die über den Ausgabetensor am Ende der Konvolution übertragen werden, der dem Ergebnis hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="7a4b2-141">Die erwarteten Dimensionen des BiasTensor sind `{ 1, OutputChannelCount, 1, 1 }` für 4D.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="7a4b2-142">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7a4b2-143">Ein Tensor, der die Ausgabeskalierdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="7a4b2-144">Die erwarteten Dimensionen von OutputScaleTensor sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="7a4b2-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="7a4b2-145">Dieser Eingabeskalierungswert wird zum Quantisieren der Konvolutionsausgabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="7a4b2-146">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7a4b2-147">Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="7a4b2-148">Die erwarteten Dimensionen von OutputZeroPointTensor sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="7a4b2-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="7a4b2-149">Dieser Eingabe-Nullpunktwert wird zum Quantisieren der Konvolution der Ausgabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="7a4b2-150">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7a4b2-151">Ein Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-151">A tensor to write the results to.</span></span> <span data-ttu-id="7a4b2-152">Die erwarteten Dimensionen des OutputTensor sind `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="7a4b2-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="7a4b2-153">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7a4b2-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="7a4b2-154">Die Anzahl der räumlichen Dimensionen für den Konvolutionsvorgang.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="7a4b2-155">Räumliche Dimensionen sind die unteren Dimensionen des Konvolutionsfilters Tensor *FilterTensor*.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="7a4b2-156">Dieser Wert bestimmt auch die Größe der Arrays *Strides*, *Dilations*, *StartPadding* und *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="7a4b2-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="7a4b2-157">Es wird nur der Wert 2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="7a4b2-158">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-158">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="7a4b2-159">Die Fortschritte des Konvolutionsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-159">The strides of the convolution operation.</span></span> <span data-ttu-id="7a4b2-160">Diese Schritte werden auf den Konvolutionsfilter angewendet.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="7a4b2-161">Sie sind von den Tensorschritten getrennt, die in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="7a4b2-162">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-162">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="7a4b2-163">Die Dilationen des Konvolutionsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="7a4b2-164">Dilationen sind Schritte, die auf die Elemente des Filterkernels angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="7a4b2-165">Dies hat den Effekt, dass ein größerer Filterkernel simuliert wird, indem die internen Filterkernelelemente mit Nullen aufschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="7a4b2-166">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-166">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="7a4b2-167">Die Auf padding-Werte, die auf den Anfang jeder räumlichen Dimension des Filters und den Eingabetensor des Konvolutionsvorgang angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="7a4b2-168">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="7a4b2-168">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="7a4b2-169">Die Auf padding-Werte, die auf das Ende jeder räumlichen Dimension des Filters und des Eingabetensors des Konvolutionsvorgang angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="7a4b2-170">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7a4b2-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="7a4b2-171">Die Anzahl der Gruppen, in die der Konvolutionsvorgang unterteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="7a4b2-172">*GroupCount* kann verwendet werden, um eine tiefenorientierte Konvolution zu erreichen, indem *GroupCount* auf die Anzahl der Eingabekanäle gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="7a4b2-173">Dadurch wird die Konvolution in eine separate Konvolution pro Eingabekanal unterteilt.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="7a4b2-174">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="7a4b2-174">Availability</span></span>
<span data-ttu-id="7a4b2-175">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="7a4b2-176">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="7a4b2-176">Tensor constraints</span></span>
* <span data-ttu-id="7a4b2-177">*FilterTensor und* *FilterZeroPointTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="7a4b2-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="7a4b2-178">*InputTensor* und *InputZeroPointTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="7a4b2-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="7a4b2-179">*OutputTensor* und `OutputZeroPointTensor` müssen den gleichen Datentyp *haben.*</span><span class="sxs-lookup"><span data-stu-id="7a4b2-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="7a4b2-180">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="7a4b2-180">Tensor support</span></span>
| <span data-ttu-id="7a4b2-181">Tensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-181">Tensor</span></span> | <span data-ttu-id="7a4b2-182">Typ</span><span class="sxs-lookup"><span data-stu-id="7a4b2-182">Kind</span></span> | <span data-ttu-id="7a4b2-183">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="7a4b2-183">Supported dimension counts</span></span> | <span data-ttu-id="7a4b2-184">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="7a4b2-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="7a4b2-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-185">InputTensor</span></span> | <span data-ttu-id="7a4b2-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a4b2-186">Input</span></span> | <span data-ttu-id="7a4b2-187">4</span><span class="sxs-lookup"><span data-stu-id="7a4b2-187">4</span></span> | <span data-ttu-id="7a4b2-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="7a4b2-188">INT8, UINT8</span></span> |
| <span data-ttu-id="7a4b2-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-189">InputScaleTensor</span></span> | <span data-ttu-id="7a4b2-190">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a4b2-190">Input</span></span> | <span data-ttu-id="7a4b2-191">4</span><span class="sxs-lookup"><span data-stu-id="7a4b2-191">4</span></span> | <span data-ttu-id="7a4b2-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="7a4b2-192">FLOAT32</span></span> |
| <span data-ttu-id="7a4b2-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-193">InputZeroPointTensor</span></span> | <span data-ttu-id="7a4b2-194">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a4b2-194">Optional input</span></span> | <span data-ttu-id="7a4b2-195">4</span><span class="sxs-lookup"><span data-stu-id="7a4b2-195">4</span></span> | <span data-ttu-id="7a4b2-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="7a4b2-196">INT8, UINT8</span></span> |
| <span data-ttu-id="7a4b2-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-197">FilterTensor</span></span> | <span data-ttu-id="7a4b2-198">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a4b2-198">Input</span></span> | <span data-ttu-id="7a4b2-199">4</span><span class="sxs-lookup"><span data-stu-id="7a4b2-199">4</span></span> | <span data-ttu-id="7a4b2-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="7a4b2-200">INT8, UINT8</span></span> |
| <span data-ttu-id="7a4b2-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-201">FilterScaleTensor</span></span> | <span data-ttu-id="7a4b2-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a4b2-202">Input</span></span> | <span data-ttu-id="7a4b2-203">4</span><span class="sxs-lookup"><span data-stu-id="7a4b2-203">4</span></span> | <span data-ttu-id="7a4b2-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="7a4b2-204">FLOAT32</span></span> |
| <span data-ttu-id="7a4b2-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="7a4b2-206">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a4b2-206">Optional input</span></span> | <span data-ttu-id="7a4b2-207">4</span><span class="sxs-lookup"><span data-stu-id="7a4b2-207">4</span></span> | <span data-ttu-id="7a4b2-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="7a4b2-208">INT8, UINT8</span></span> |
| <span data-ttu-id="7a4b2-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-209">BiasTensor</span></span> | <span data-ttu-id="7a4b2-210">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a4b2-210">Optional input</span></span> | <span data-ttu-id="7a4b2-211">4</span><span class="sxs-lookup"><span data-stu-id="7a4b2-211">4</span></span> | <span data-ttu-id="7a4b2-212">INT32</span><span class="sxs-lookup"><span data-stu-id="7a4b2-212">INT32</span></span> |
| <span data-ttu-id="7a4b2-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-213">OutputScaleTensor</span></span> | <span data-ttu-id="7a4b2-214">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a4b2-214">Input</span></span> | <span data-ttu-id="7a4b2-215">4</span><span class="sxs-lookup"><span data-stu-id="7a4b2-215">4</span></span> | <span data-ttu-id="7a4b2-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="7a4b2-216">FLOAT32</span></span> |
| <span data-ttu-id="7a4b2-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="7a4b2-218">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a4b2-218">Optional input</span></span> | <span data-ttu-id="7a4b2-219">4</span><span class="sxs-lookup"><span data-stu-id="7a4b2-219">4</span></span> | <span data-ttu-id="7a4b2-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="7a4b2-220">INT8, UINT8</span></span> |
| <span data-ttu-id="7a4b2-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="7a4b2-221">OutputTensor</span></span> | <span data-ttu-id="7a4b2-222">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="7a4b2-222">Output</span></span> | <span data-ttu-id="7a4b2-223">4</span><span class="sxs-lookup"><span data-stu-id="7a4b2-223">4</span></span> | <span data-ttu-id="7a4b2-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="7a4b2-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="7a4b2-225">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a4b2-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7a4b2-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="7a4b2-226">**Header**</span></span> | <span data-ttu-id="7a4b2-227">directml.h</span><span class="sxs-lookup"><span data-stu-id="7a4b2-227">directml.h</span></span> |