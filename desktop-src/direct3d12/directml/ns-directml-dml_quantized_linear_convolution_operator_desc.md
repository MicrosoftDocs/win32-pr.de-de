---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Führt eine Zusammenführung des *filtertensor* mit dem *inputtensor* aus. Dieser Operator führt vorwärts Vorgänge für quantifizierte Daten aus. Dieser Operator entspricht mathematisch dem dequantifialisieren der Eingaben, dem durchwinken und dem anschließenden quantifialisieren der Ausgabe.
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
ms.openlocfilehash: 01193b19744f413690a3cb5ecccbb8fa60626cb0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361109"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="adaed-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="adaed-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="adaed-106">Führt eine Zusammenführung des *filtertensor* mit dem *inputtensor* aus.</span><span class="sxs-lookup"><span data-stu-id="adaed-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="adaed-107">Dieser Operator führt vorwärts Vorgänge für quantifizierte Daten aus.</span><span class="sxs-lookup"><span data-stu-id="adaed-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="adaed-108">Dieser Operator entspricht mathematisch dem dequantifialisieren der Eingaben, dem durchwinken und dem anschließenden quantifialisieren der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="adaed-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="adaed-109">Die von diesem Operator verwendeten linearen quantize-Funktionen sind die linearen quantifizierungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="adaed-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="adaed-110">Funktion "Debug"</span><span class="sxs-lookup"><span data-stu-id="adaed-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="adaed-111">Quantize-Funktion</span><span class="sxs-lookup"><span data-stu-id="adaed-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="adaed-112">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="adaed-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="adaed-113">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="adaed-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="adaed-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="adaed-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="adaed-115">Member</span><span class="sxs-lookup"><span data-stu-id="adaed-115">Members</span></span>

`InputTensor`

<span data-ttu-id="adaed-116">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="adaed-117">Ein tensorflow, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="adaed-117">A tensor containing the input data.</span></span> <span data-ttu-id="adaed-118">Die erwarteten Dimensionen von " *inputtensor* " sind `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="adaed-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="adaed-119">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="adaed-120">Ein tensorflow mit den Eingabedaten der Skala.</span><span class="sxs-lookup"><span data-stu-id="adaed-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="adaed-121">Die erwarteten Dimensionen von `InputScaleTensor` sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="adaed-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="adaed-122">Dieser Skalierungs Wert wird zum dequantifialisieren der Eingabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="adaed-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="adaed-123">Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="adaed-124">Ein optionaler tensorflow, der die Eingabedaten für den Nullpunkt enthält.</span><span class="sxs-lookup"><span data-stu-id="adaed-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="adaed-125">Die erwarteten Dimensionen von *inputzeropointtensor* sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="adaed-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="adaed-126">Dieser Nullpunktwert wird zum decomieren der Eingabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="adaed-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="adaed-127">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="adaed-128">Ein tensorflow, der die Filterdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="adaed-128">A tensor containing the filter data.</span></span> <span data-ttu-id="adaed-129">Die erwarteten Dimensionen des *filtertensor* sind `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="adaed-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="adaed-130">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="adaed-131">Ein tensorflow, der die Filter Skalierungs Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="adaed-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="adaed-132">Die erwarteten Dimensionen von `FilterScaleTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, OutputChannelCount, 1, 1 }` Wenn die pro-Kanal-Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="adaed-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="adaed-133">Dieser Skalierungs Wert wird zum dequantifialisieren der Filter Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="adaed-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="adaed-134">Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="adaed-135">Ein optionaler tensorflow, der die Filter-NULL-Punktdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="adaed-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="adaed-136">Die erwarteten Dimensionen von " *filterzeropointtensor* " sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist oder `{ 1, OutputChannelCount, 1, 1 }` Wenn eine pro-Kanal-Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="adaed-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="adaed-137">Dieser Nullpunktwert wird zum decomieren der Filter Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="adaed-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="adaed-138">Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="adaed-139">Ein tensorflow, der die Daten der Bias enthält.</span><span class="sxs-lookup"><span data-stu-id="adaed-139">A tensor containing the bias data.</span></span> <span data-ttu-id="adaed-140">Der Bias-tensorflow ist ein tensorflow, der Daten enthält, die über den Ausgabe Mandanten am Ende der Konvolution übertragen werden, die dem Ergebnis hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="adaed-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="adaed-141">Die erwarteten Dimensionen von biastensor sind `{ 1, OutputChannelCount, 1, 1 }` für 4D.</span><span class="sxs-lookup"><span data-stu-id="adaed-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="adaed-142">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="adaed-143">Ein tensorflow, der die Daten der Ausgabe Skala enthält.</span><span class="sxs-lookup"><span data-stu-id="adaed-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="adaed-144">Die erwarteten Dimensionen von outputscaletensor sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="adaed-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="adaed-145">Dieser Wert für die Eingabe Skala wird zum quantifialisieren der Ausgabewerte der-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="adaed-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="adaed-146">Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="adaed-147">Ein optionaler tensorflow, der die Filter-NULL-Punktdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="adaed-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="adaed-148">Die erwarteten Dimensionen von outputzeropointtensor sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="adaed-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="adaed-149">Dieser Wert für die Eingabe von null Punkten wird zum quantifialisieren der Ausgabewerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="adaed-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="adaed-150">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="adaed-151">Ein tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="adaed-151">A tensor to write the results to.</span></span> <span data-ttu-id="adaed-152">Die erwarteten Dimensionen von outputtensor sind `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="adaed-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="adaed-153">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="adaed-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="adaed-154">Die Anzahl räumlicher Dimensionen für den Vorgangs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="adaed-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="adaed-155">Räumliche Dimensionen sind die unteren Dimensionen des tensorflow- *filtertensors* für den Verbindungs Filter.</span><span class="sxs-lookup"><span data-stu-id="adaed-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="adaed-156">Dieser Wert bestimmt auch die Größe der Felder " *fort* schreiten *", "Erweiterungen", "* *startpadding*" und " *endpadding* ".</span><span class="sxs-lookup"><span data-stu-id="adaed-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="adaed-157">Nur der Wert 2 wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="adaed-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="adaed-158">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-158">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="adaed-159">Die Fortschritte des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="adaed-159">The strides of the convolution operation.</span></span> <span data-ttu-id="adaed-160">Diese Schritte werden auf den Konfigurations Filter angewendet.</span><span class="sxs-lookup"><span data-stu-id="adaed-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="adaed-161">Sie sind von den in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)enthaltenen tensorflow-Schritten getrennt.</span><span class="sxs-lookup"><span data-stu-id="adaed-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="adaed-162">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-162">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="adaed-163">Die Erweiterungen des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="adaed-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="adaed-164">Erweiterungen sind Schritte, die auf die Elemente des Filter Kernels angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="adaed-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="adaed-165">Dies hat den Effekt, einen größeren Filter Kernel zu simulieren, indem die internen Filter-Kernel Elemente mit Nullen aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="adaed-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="adaed-166">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-166">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="adaed-167">Die Auffüll Werte, die auf den Anfang jeder räumlichen Dimension des Filters und des Eingabe-Tensors des Vorgangs angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="adaed-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="adaed-168">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="adaed-168">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="adaed-169">Die Auffüll Werte, die auf das Ende jeder räumlichen Dimension des Filters und des Eingabe-Tensors der Konvolution-Operation angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="adaed-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="adaed-170">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="adaed-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="adaed-171">Die Anzahl der Gruppen, in die der Vorgang unterteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="adaed-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="adaed-172">*GroupCount* kann verwendet werden, um eine tiefgreifende Zusammenführung zu erzielen, indem *GroupCount* auf die Anzahl der Eingabe Kanäle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="adaed-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="adaed-173">Dadurch wird die zusammen Gabe in eine separate zusammen Gabe pro Eingabe Kanal aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="adaed-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="adaed-174">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="adaed-174">Availability</span></span>
<span data-ttu-id="adaed-175">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="adaed-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="adaed-176">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="adaed-176">Tensor constraints</span></span>
* <span data-ttu-id="adaed-177">*Filtertensor* und *filterzeropointtensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="adaed-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="adaed-178">*Inputtensor* und *inputzeropointtensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="adaed-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="adaed-179">*Outputtensor* und `OutputZeroPointTensor` muss denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="adaed-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="adaed-180">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="adaed-180">Tensor support</span></span>
| <span data-ttu-id="adaed-181">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="adaed-181">Tensor</span></span> | <span data-ttu-id="adaed-182">Typ</span><span class="sxs-lookup"><span data-stu-id="adaed-182">Kind</span></span> | <span data-ttu-id="adaed-183">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="adaed-183">Supported dimension counts</span></span> | <span data-ttu-id="adaed-184">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="adaed-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="adaed-185">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="adaed-185">InputTensor</span></span> | <span data-ttu-id="adaed-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="adaed-186">Input</span></span> | <span data-ttu-id="adaed-187">4</span><span class="sxs-lookup"><span data-stu-id="adaed-187">4</span></span> | <span data-ttu-id="adaed-188">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="adaed-188">INT8, UINT8</span></span> |
| <span data-ttu-id="adaed-189">Inputscaletensor</span><span class="sxs-lookup"><span data-stu-id="adaed-189">InputScaleTensor</span></span> | <span data-ttu-id="adaed-190">Eingabe</span><span class="sxs-lookup"><span data-stu-id="adaed-190">Input</span></span> | <span data-ttu-id="adaed-191">4</span><span class="sxs-lookup"><span data-stu-id="adaed-191">4</span></span> | <span data-ttu-id="adaed-192">Float32</span><span class="sxs-lookup"><span data-stu-id="adaed-192">FLOAT32</span></span> |
| <span data-ttu-id="adaed-193">Inputzeropointtensor</span><span class="sxs-lookup"><span data-stu-id="adaed-193">InputZeroPointTensor</span></span> | <span data-ttu-id="adaed-194">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="adaed-194">Optional input</span></span> | <span data-ttu-id="adaed-195">4</span><span class="sxs-lookup"><span data-stu-id="adaed-195">4</span></span> | <span data-ttu-id="adaed-196">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="adaed-196">INT8, UINT8</span></span> |
| <span data-ttu-id="adaed-197">Filtertensor</span><span class="sxs-lookup"><span data-stu-id="adaed-197">FilterTensor</span></span> | <span data-ttu-id="adaed-198">Eingabe</span><span class="sxs-lookup"><span data-stu-id="adaed-198">Input</span></span> | <span data-ttu-id="adaed-199">4</span><span class="sxs-lookup"><span data-stu-id="adaed-199">4</span></span> | <span data-ttu-id="adaed-200">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="adaed-200">INT8, UINT8</span></span> |
| <span data-ttu-id="adaed-201">Filterscaletensor</span><span class="sxs-lookup"><span data-stu-id="adaed-201">FilterScaleTensor</span></span> | <span data-ttu-id="adaed-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="adaed-202">Input</span></span> | <span data-ttu-id="adaed-203">4</span><span class="sxs-lookup"><span data-stu-id="adaed-203">4</span></span> | <span data-ttu-id="adaed-204">Float32</span><span class="sxs-lookup"><span data-stu-id="adaed-204">FLOAT32</span></span> |
| <span data-ttu-id="adaed-205">Filterzeropointtensor</span><span class="sxs-lookup"><span data-stu-id="adaed-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="adaed-206">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="adaed-206">Optional input</span></span> | <span data-ttu-id="adaed-207">4</span><span class="sxs-lookup"><span data-stu-id="adaed-207">4</span></span> | <span data-ttu-id="adaed-208">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="adaed-208">INT8, UINT8</span></span> |
| <span data-ttu-id="adaed-209">Biastensor</span><span class="sxs-lookup"><span data-stu-id="adaed-209">BiasTensor</span></span> | <span data-ttu-id="adaed-210">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="adaed-210">Optional input</span></span> | <span data-ttu-id="adaed-211">4</span><span class="sxs-lookup"><span data-stu-id="adaed-211">4</span></span> | <span data-ttu-id="adaed-212">INT32</span><span class="sxs-lookup"><span data-stu-id="adaed-212">INT32</span></span> |
| <span data-ttu-id="adaed-213">Outputscaletensor</span><span class="sxs-lookup"><span data-stu-id="adaed-213">OutputScaleTensor</span></span> | <span data-ttu-id="adaed-214">Eingabe</span><span class="sxs-lookup"><span data-stu-id="adaed-214">Input</span></span> | <span data-ttu-id="adaed-215">4</span><span class="sxs-lookup"><span data-stu-id="adaed-215">4</span></span> | <span data-ttu-id="adaed-216">Float32</span><span class="sxs-lookup"><span data-stu-id="adaed-216">FLOAT32</span></span> |
| <span data-ttu-id="adaed-217">Outputzeropointtensor</span><span class="sxs-lookup"><span data-stu-id="adaed-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="adaed-218">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="adaed-218">Optional input</span></span> | <span data-ttu-id="adaed-219">4</span><span class="sxs-lookup"><span data-stu-id="adaed-219">4</span></span> | <span data-ttu-id="adaed-220">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="adaed-220">INT8, UINT8</span></span> |
| <span data-ttu-id="adaed-221">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="adaed-221">OutputTensor</span></span> | <span data-ttu-id="adaed-222">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="adaed-222">Output</span></span> | <span data-ttu-id="adaed-223">4</span><span class="sxs-lookup"><span data-stu-id="adaed-223">4</span></span> | <span data-ttu-id="adaed-224">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="adaed-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="adaed-225">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adaed-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="adaed-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="adaed-226">**Header**</span></span> | <span data-ttu-id="adaed-227">directml. h</span><span class="sxs-lookup"><span data-stu-id="adaed-227">directml.h</span></span> |