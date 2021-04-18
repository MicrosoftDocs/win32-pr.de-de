---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Berechnet den maximalen Wert für die Elemente innerhalb des gleitenden Fensters über den Eingabe Mandanten und gibt optional die Indizes der ausgewählten Maximalwerte zurück.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 7d2dc9d28e8afcaa5cc6277e26f1f663f3f6688f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106365218"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a><span data-ttu-id="5037a-103">DML_MAX_POOLING2_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="5037a-103">DML_MAX_POOLING2_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="5037a-104">Berechnet den maximalen Wert für die Elemente innerhalb des gleitenden Fensters über den Eingabe Mandanten und gibt optional die Indizes der ausgewählten Maximalwerte zurück.</span><span class="sxs-lookup"><span data-stu-id="5037a-104">Computes the maximum value across the elements within the sliding window over the input tensor, and optionally returns the indices of the maximum values selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5037a-105">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="5037a-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="5037a-106">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5037a-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5037a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5037a-107">Syntax</span></span>
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a><span data-ttu-id="5037a-108">Member</span><span class="sxs-lookup"><span data-stu-id="5037a-108">Members</span></span>

`InputTensor`

<span data-ttu-id="5037a-109">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5037a-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5037a-110">Ein Eingabe-tensorflow der *Größen* `{ BatchCount, ChannelCount, Height, Width }` , wenn *inputtensor. DimensionCount* den Wert 4 hat, und, `{ BatchCount, ChannelCount, Depth, Height, Weight } ` Wenn *inputtensor. DimensionCount* 5 ist.</span><span class="sxs-lookup"><span data-stu-id="5037a-110">An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` if *InputTensor.DimensionCount* is 4, and `{ BatchCount, ChannelCount, Depth, Height, Weight } `if *InputTensor.DimensionCount* is 5.</span></span>


`OutputTensor`

<span data-ttu-id="5037a-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5037a-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5037a-112">Ein Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5037a-112">An output tensor to write the results to.</span></span> <span data-ttu-id="5037a-113">Die Größen des Ausgabe Mandanten können wie folgt berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="5037a-113">The sizes of the output tensor can be computed as follows.</span></span>

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

<span data-ttu-id="5037a-114">Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5037a-114">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5037a-115">Ein optionaler ausgabetensor von Indizes für den Eingabe-tensorflow- *inputtensor* der maximalen Werte, die in *outputtensor* erstellt und gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5037a-115">An optional output tensor of indices to the input tensor *InputTensor* of the maximum values produced and stored in the *OutputTensor*.</span></span> <span data-ttu-id="5037a-116">Diese Indexwerte sind NULL basiert und behandeln den Eingabe Mandanten als zusammenhängendes eindimensionales Array.</span><span class="sxs-lookup"><span data-stu-id="5037a-116">These index values are zero-based and treat the input tensor as a contiguous one-dimensional array.</span></span> <span data-ttu-id="5037a-117">Wenn mehrere Elemente innerhalb des gleitenden Fensters denselben Wert aufweisen, werden die nachfolgenden Gleichheits Werte ignoriert, und der Index zeigt auf den ersten gefundenen Wert.</span><span class="sxs-lookup"><span data-stu-id="5037a-117">When multiple elements within the sliding window have the same value, the later equal values are ignored and the index points to the first value encountered.</span></span> <span data-ttu-id="5037a-118">Sowohl der *outputtensor* als auch der *outputindicestensor* haben die gleichen tensorflow-Größen.</span><span class="sxs-lookup"><span data-stu-id="5037a-118">Both the *OutputTensor* and *OutputIndicesTensor* have the same tensor sizes.</span></span>


`DimensionCount`

<span data-ttu-id="5037a-119">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5037a-119">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5037a-120">Die Anzahl räumlicher Dimensionen des Input tensorflow *inputtensor*, der auch der Anzahl der Dimensionen des gleitenden Fensters *WindowSize* entspricht.</span><span class="sxs-lookup"><span data-stu-id="5037a-120">The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*.</span></span> <span data-ttu-id="5037a-121">Dieser Wert bestimmt auch die Größe der Felder " *fort* schreiten", " *startpadding*" und " *endpadding* ".</span><span class="sxs-lookup"><span data-stu-id="5037a-121">This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="5037a-122">Er sollte auf 2 festgelegt werden, wenn *inputtensor* auf 4D festgelegt ist, und 3, wenn es sich um einen 5D-Tensor handelt.</span><span class="sxs-lookup"><span data-stu-id="5037a-122">It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.</span></span>


`Strides`

<span data-ttu-id="5037a-123">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="5037a-123">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="5037a-124">Die Schritte für die Abmessungen des gleitenden Fensters von Größen `{ Height, Width }` , wenn *DimensionCount* auf 2 festgelegt ist, oder, wenn der Wert `{ Depth, Height, Width }` auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5037a-124">The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`WindowSize`

<span data-ttu-id="5037a-125">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="5037a-125">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="5037a-126">Die Abmessungen des gleitenden Fensters in `{ Height, Width }` , wenn *DimensionCount* auf 2 festgelegt ist, oder, `{ Depth, Height, Width }` Wenn es auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5037a-126">The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`StartPadding`

<span data-ttu-id="5037a-127">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="5037a-127">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="5037a-128">Die Anzahl der Auffüll Elemente, die auf den Anfang jeder räumlichen Dimension des Eingabe-Tensors *inputtensor* angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5037a-128">The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="5037a-129">Die Werte sind in `{ Height, Width }` , wenn *DimensionCount* auf 2 festgelegt ist, oder `{ Depth, Height, Width }` Wenn auf 3 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5037a-129">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`EndPadding`

<span data-ttu-id="5037a-130">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="5037a-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="5037a-131">Die Anzahl der Auffüll Elemente, die auf das Ende jeder räumlichen Dimension des Eingabe-Tensors *inputtensor* angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5037a-131">The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="5037a-132">Die Werte sind in `{ Height, Width }` , wenn *DimensionCount* auf 2 festgelegt ist, oder `{ Depth, Height, Width }` Wenn auf 3 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5037a-132">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`Dilations`

<span data-ttu-id="5037a-133">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="5037a-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="5037a-134">Die Werte für jede räumliche Dimension des Eingabe Mandanten *, von dem* ein Element im gleitenden Fenster für alle Elemente dieses Werts ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5037a-134">The values for each spatial dimension of the input tensor *InputTensor* by which an element within the sliding window is selected for every elements of that value.</span></span> <span data-ttu-id="5037a-135">Die Werte sind in `{ Height, Width }` , wenn *DimensionCount* auf 2 festgelegt ist, oder `{ Depth, Height, Width }` Wenn auf 3 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5037a-135">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


## <a name="remarks"></a><span data-ttu-id="5037a-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5037a-136">Remarks</span></span>
<span data-ttu-id="5037a-137">**DML_MAX_POOLING2_OPERATOR_DESC** ersetzt die frühere Version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) mit einer zusätzlichen Konstanten Array *Erweiterung*.</span><span class="sxs-lookup"><span data-stu-id="5037a-137">**DML_MAX_POOLING2_OPERATOR_DESC** supersedes the earlier version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) with an additional constant array *Dilations*.</span></span> <span data-ttu-id="5037a-138">Die beiden Versionen sind gleichwertig  `{ 1,1 }` , wenn für eine 4D-Eingabe oder `{ 1,1,1 }` für 5D-Eingabe Features festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5037a-138">The two versions are equivalent when *Dilations* is set to `{ 1,1 }` for 4D input, or `{ 1,1,1 }` for 5D input features.</span></span>

## <a name="availability"></a><span data-ttu-id="5037a-139">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="5037a-139">Availability</span></span>
<span data-ttu-id="5037a-140">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="5037a-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5037a-141">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="5037a-141">Tensor constraints</span></span>
* <span data-ttu-id="5037a-142">' *Inputtensor*', ' *outputindicestensor*' und ' *outputtensor* ' müssen dieselbe *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5037a-142">*InputTensor*, *OutputIndicesTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="5037a-143">*Inputtensor* und *outputtensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5037a-143">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5037a-144">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="5037a-144">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="5037a-145">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="5037a-145">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="5037a-146">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="5037a-146">Tensor</span></span> | <span data-ttu-id="5037a-147">Typ</span><span class="sxs-lookup"><span data-stu-id="5037a-147">Kind</span></span> | <span data-ttu-id="5037a-148">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="5037a-148">Supported dimension counts</span></span> | <span data-ttu-id="5037a-149">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="5037a-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5037a-150">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="5037a-150">InputTensor</span></span> | <span data-ttu-id="5037a-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5037a-151">Input</span></span> | <span data-ttu-id="5037a-152">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="5037a-152">4 to 5</span></span> | <span data-ttu-id="5037a-153">Float32, FLOAT16, int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="5037a-153">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="5037a-154">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="5037a-154">OutputTensor</span></span> | <span data-ttu-id="5037a-155">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5037a-155">Output</span></span> | <span data-ttu-id="5037a-156">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="5037a-156">4 to 5</span></span> | <span data-ttu-id="5037a-157">Float32, FLOAT16, int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="5037a-157">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="5037a-158">Outputindicestensor</span><span class="sxs-lookup"><span data-stu-id="5037a-158">OutputIndicesTensor</span></span> | <span data-ttu-id="5037a-159">Optionale Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5037a-159">Optional output</span></span> | <span data-ttu-id="5037a-160">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="5037a-160">4 to 5</span></span> | <span data-ttu-id="5037a-161">UINT32</span><span class="sxs-lookup"><span data-stu-id="5037a-161">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="5037a-162">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="5037a-162">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="5037a-163">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="5037a-163">Tensor</span></span> | <span data-ttu-id="5037a-164">Typ</span><span class="sxs-lookup"><span data-stu-id="5037a-164">Kind</span></span> | <span data-ttu-id="5037a-165">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="5037a-165">Supported dimension counts</span></span> | <span data-ttu-id="5037a-166">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="5037a-166">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5037a-167">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="5037a-167">InputTensor</span></span> | <span data-ttu-id="5037a-168">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5037a-168">Input</span></span> | <span data-ttu-id="5037a-169">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="5037a-169">4 to 5</span></span> | <span data-ttu-id="5037a-170">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5037a-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5037a-171">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="5037a-171">OutputTensor</span></span> | <span data-ttu-id="5037a-172">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5037a-172">Output</span></span> | <span data-ttu-id="5037a-173">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="5037a-173">4 to 5</span></span> | <span data-ttu-id="5037a-174">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5037a-174">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5037a-175">Outputindicestensor</span><span class="sxs-lookup"><span data-stu-id="5037a-175">OutputIndicesTensor</span></span> | <span data-ttu-id="5037a-176">Optionale Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5037a-176">Optional output</span></span> | <span data-ttu-id="5037a-177">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="5037a-177">4 to 5</span></span> | <span data-ttu-id="5037a-178">UINT32</span><span class="sxs-lookup"><span data-stu-id="5037a-178">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="5037a-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5037a-179">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5037a-180">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="5037a-180">**Minimum supported client**</span></span> | <span data-ttu-id="5037a-181">Windows 10, Version 2004 (10,0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="5037a-181">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="5037a-182">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="5037a-182">**Minimum supported server**</span></span> | <span data-ttu-id="5037a-183">Windows Server, Version 2004 (10,0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="5037a-183">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="5037a-184">**Header**</span><span class="sxs-lookup"><span data-stu-id="5037a-184">**Header**</span></span> | <span data-ttu-id="5037a-185">directml. h</span><span class="sxs-lookup"><span data-stu-id="5037a-185">directml.h</span></span> |