---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Führt eine Zusammenführung des *filtertensor* mit dem *inputtensor* aus. Dieser Operator führt vorwärts Vorgänge für ganzzahlige Daten aus.
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
ms.openlocfilehash: c16690ea1e3049ffeba398bbbaca2003f965a832
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106367265"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="dfc9b-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="dfc9b-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="dfc9b-105">Führt eine Zusammenführung des *filtertensor* mit dem *inputtensor* aus.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="dfc9b-106">Dieser Operator führt vorwärts Vorgänge für ganzzahlige Daten aus.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="dfc9b-107">Optionale Null-Punkt-Tensoren können auch verwendet werden, um NULL-Punktwerte aus dem Eingabe-und Filter Tensor zu subtrahieren.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfc9b-108">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="dfc9b-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="dfc9b-109">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="dfc9b-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc9b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfc9b-110">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="dfc9b-111">Member</span><span class="sxs-lookup"><span data-stu-id="dfc9b-111">Members</span></span>

`InputTensor`

<span data-ttu-id="dfc9b-112">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dfc9b-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dfc9b-113">Ein tensorflow, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-113">A tensor containing the input data.</span></span> <span data-ttu-id="dfc9b-114">Die erwarteten Dimensionen von " *inputtensor* " sind `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="dfc9b-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="dfc9b-115">Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dfc9b-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dfc9b-116">Ein optionaler tensorflow, der die Eingabedaten für den Nullpunkt enthält.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="dfc9b-117">Die erwarteten Dimensionen von *inputzeropointtensor* sind `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="dfc9b-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="dfc9b-118">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dfc9b-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dfc9b-119">Ein tensorflow, der die Filterdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-119">A tensor containing the filter data.</span></span> <span data-ttu-id="dfc9b-120">Die erwarteten Dimensionen des *filtertensor* sind `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="dfc9b-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="dfc9b-121">Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dfc9b-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dfc9b-122">Ein optionaler tensorflow, der die Filter-NULL-Punktdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="dfc9b-123">Die erwarteten Dimensionen von " *filterzeropointtensor* " sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist oder `{ 1, OutputChannelCount, 1, 1 }` Wenn die pro-Kanal-Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="dfc9b-124">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dfc9b-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dfc9b-125">Der tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-125">The tensor to write the results to.</span></span> <span data-ttu-id="dfc9b-126">Die erwarteten Dimensionen von *outputtensor* sind `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="dfc9b-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="dfc9b-127">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="dfc9b-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="dfc9b-128">Die Anzahl räumlicher Dimensionen für den Vorgangs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="dfc9b-129">Räumliche Dimensionen sind die niedrigeren Dimensionen von "- *filtertensor*".</span><span class="sxs-lookup"><span data-stu-id="dfc9b-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="dfc9b-130">Dieser Wert bestimmt auch die Größe der Felder " *fort* schreiten *", "Erweiterungen", "* *startpadding*" und " *endpadding* ".</span><span class="sxs-lookup"><span data-stu-id="dfc9b-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="dfc9b-131">Nur der Wert 2 wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="dfc9b-132">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="dfc9b-132">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="dfc9b-133">Ein Array, das die Fortschritte der Zusammenführung des Vorgangs enthält.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="dfc9b-134">Diese Schritte werden auf den Konfigurations Filter angewendet.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="dfc9b-135">Sie sind von den in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)enthaltenen tensorflow-Schritten getrennt.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="dfc9b-136">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="dfc9b-136">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="dfc9b-137">Ein Array, das die Erweiterungen der Vorgangs Operation enthält.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="dfc9b-138">Erweiterungen sind Schritte, die auf die Elemente des Filter Kernels angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="dfc9b-139">Dies hat den Effekt, einen größeren Filter Kernel zu simulieren, indem die internen Filter-Kernel Elemente mit Nullen aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="dfc9b-140">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="dfc9b-140">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="dfc9b-141">Ein Array, das die Auffüll Werte enthält, die auf den Anfang jeder räumlichen Dimension des Filters und eingabetensors des Vorgangs angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="dfc9b-142">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="dfc9b-142">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="dfc9b-143">Ein Array, das die Auffüll Werte enthält, die auf das Ende jeder räumlichen Dimension des Filters und des Eingabe-Tensors der Konvolution-Operation angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="dfc9b-144">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="dfc9b-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="dfc9b-145">Die Anzahl der Gruppen, in die der Vorgang in den Vorgang aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="dfc9b-146">*GroupCount* kann verwendet werden, um eine tiefgreifende Zusammenführung zu erzielen, indem *GroupCount* auf die Anzahl der Eingabe Kanäle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="dfc9b-147">Dadurch wird die zusammen Gabe in eine separate zusammen Gabe pro Eingabe Kanal aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="dfc9b-148">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="dfc9b-148">Availability</span></span>
<span data-ttu-id="dfc9b-149">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="dfc9b-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="dfc9b-150">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="dfc9b-150">Tensor constraints</span></span>
* <span data-ttu-id="dfc9b-151">*Filtertensor* und *filterzeropointtensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="dfc9b-152">*Inputtensor* und *inputzeropointtensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dfc9b-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="dfc9b-153">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="dfc9b-153">Tensor support</span></span>
| <span data-ttu-id="dfc9b-154">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="dfc9b-154">Tensor</span></span> | <span data-ttu-id="dfc9b-155">Typ</span><span class="sxs-lookup"><span data-stu-id="dfc9b-155">Kind</span></span> | <span data-ttu-id="dfc9b-156">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="dfc9b-156">Dimensions</span></span> | <span data-ttu-id="dfc9b-157">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="dfc9b-157">Supported dimension counts</span></span> | <span data-ttu-id="dfc9b-158">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="dfc9b-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="dfc9b-159">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="dfc9b-159">InputTensor</span></span> | <span data-ttu-id="dfc9b-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfc9b-160">Input</span></span> | <span data-ttu-id="dfc9b-161">{BatchCount, inputchannelcount, inputheight, inputwidth}</span><span class="sxs-lookup"><span data-stu-id="dfc9b-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="dfc9b-162">4</span><span class="sxs-lookup"><span data-stu-id="dfc9b-162">4</span></span> | <span data-ttu-id="dfc9b-163">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="dfc9b-163">INT8, UINT8</span></span> |
| <span data-ttu-id="dfc9b-164">Inputzeropointtensor</span><span class="sxs-lookup"><span data-stu-id="dfc9b-164">InputZeroPointTensor</span></span> | <span data-ttu-id="dfc9b-165">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfc9b-165">Optional input</span></span> | <span data-ttu-id="dfc9b-166">{1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="dfc9b-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="dfc9b-167">4</span><span class="sxs-lookup"><span data-stu-id="dfc9b-167">4</span></span> | <span data-ttu-id="dfc9b-168">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="dfc9b-168">INT8, UINT8</span></span> |
| <span data-ttu-id="dfc9b-169">Filtertensor</span><span class="sxs-lookup"><span data-stu-id="dfc9b-169">FilterTensor</span></span> | <span data-ttu-id="dfc9b-170">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfc9b-170">Input</span></span> | <span data-ttu-id="dfc9b-171">{Filterbatchcount, filterchannelcount, filterheight, filterwidth}</span><span class="sxs-lookup"><span data-stu-id="dfc9b-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="dfc9b-172">4</span><span class="sxs-lookup"><span data-stu-id="dfc9b-172">4</span></span> | <span data-ttu-id="dfc9b-173">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="dfc9b-173">INT8, UINT8</span></span> |
| <span data-ttu-id="dfc9b-174">Filterzeropointtensor</span><span class="sxs-lookup"><span data-stu-id="dfc9b-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="dfc9b-175">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfc9b-175">Optional input</span></span> | <span data-ttu-id="dfc9b-176">{1, filterzerkopintchannelcount, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="dfc9b-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="dfc9b-177">4</span><span class="sxs-lookup"><span data-stu-id="dfc9b-177">4</span></span> | <span data-ttu-id="dfc9b-178">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="dfc9b-178">INT8, UINT8</span></span> |
| <span data-ttu-id="dfc9b-179">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="dfc9b-179">OutputTensor</span></span> | <span data-ttu-id="dfc9b-180">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="dfc9b-180">Output</span></span> | <span data-ttu-id="dfc9b-181">{BatchCount, outputchannelcount, OutputHeight, OutputWidth}</span><span class="sxs-lookup"><span data-stu-id="dfc9b-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="dfc9b-182">4</span><span class="sxs-lookup"><span data-stu-id="dfc9b-182">4</span></span> | <span data-ttu-id="dfc9b-183">INT32</span><span class="sxs-lookup"><span data-stu-id="dfc9b-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="dfc9b-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfc9b-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="dfc9b-185">**Header**</span><span class="sxs-lookup"><span data-stu-id="dfc9b-185">**Header**</span></span> | <span data-ttu-id="dfc9b-186">directml. h</span><span class="sxs-lookup"><span data-stu-id="dfc9b-186">directml.h</span></span> |