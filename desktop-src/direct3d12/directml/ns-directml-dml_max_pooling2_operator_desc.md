---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Berechnet den Maximalen Wert für die Elemente innerhalb des gleitenden Fensters über den Eingabe-Tensor und gibt optional die Indizes der ausgewählten Höchstwerte zurück.
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
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803667"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a><span data-ttu-id="01242-103">DML_MAX_POOLING2_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="01242-103">DML_MAX_POOLING2_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="01242-104">Berechnet den Maximalen Wert für die Elemente innerhalb des gleitenden Fensters über den Eingabe-Tensor und gibt optional die Indizes der ausgewählten Höchstwerte zurück.</span><span class="sxs-lookup"><span data-stu-id="01242-104">Computes the maximum value across the elements within the sliding window over the input tensor, and optionally returns the indices of the maximum values selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01242-105">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="01242-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="01242-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="01242-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="01242-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="01242-107">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="01242-108">Member</span><span class="sxs-lookup"><span data-stu-id="01242-108">Members</span></span>

`InputTensor`

<span data-ttu-id="01242-109">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="01242-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="01242-110">Ein Eingabe tensor von *Größen,* `{ BatchCount, ChannelCount, Height, Width }` wenn *InputTensor.DimensionCount* 4 und `{ BatchCount, ChannelCount, Depth, Height, Weight } ` *InputTensor.DimensionCount* 5 ist.</span><span class="sxs-lookup"><span data-stu-id="01242-110">An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` if *InputTensor.DimensionCount* is 4, and `{ BatchCount, ChannelCount, Depth, Height, Weight } `if *InputTensor.DimensionCount* is 5.</span></span>


`OutputTensor`

<span data-ttu-id="01242-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="01242-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="01242-112">Ein Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="01242-112">An output tensor to write the results to.</span></span> <span data-ttu-id="01242-113">Die Größen des Ausgabe-Tensors können wie folgt berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="01242-113">The sizes of the output tensor can be computed as follows.</span></span>

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

<span data-ttu-id="01242-114">Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="01242-114">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="01242-115">Ein optionaler Ausgabe-Tensor von Indizes für den Eingabe tensor *InputTensor* der maximalen Werte, die im *OutputTensor* erstellt und gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="01242-115">An optional output tensor of indices to the input tensor *InputTensor* of the maximum values produced and stored in the *OutputTensor*.</span></span> <span data-ttu-id="01242-116">Diese Indexwerte sind nullbasiert und behandeln den Eingabe-Tensor als zusammenhängendes eindimensionales Array.</span><span class="sxs-lookup"><span data-stu-id="01242-116">These index values are zero-based and treat the input tensor as a contiguous one-dimensional array.</span></span> <span data-ttu-id="01242-117">Wenn mehrere Elemente innerhalb des gleitenden Fensters den gleichen Wert aufweisen, werden die späteren gleichen Werte ignoriert, und der Index zeigt auf den ersten gefundenen Wert.</span><span class="sxs-lookup"><span data-stu-id="01242-117">When multiple elements within the sliding window have the same value, the later equal values are ignored and the index points to the first value encountered.</span></span> <span data-ttu-id="01242-118">*OutputTensor* und *OutputIndicesTensor* haben die gleichen Tensorgrößen.</span><span class="sxs-lookup"><span data-stu-id="01242-118">Both the *OutputTensor* and *OutputIndicesTensor* have the same tensor sizes.</span></span>


`DimensionCount`

<span data-ttu-id="01242-119">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="01242-119">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="01242-120">Die Anzahl der räumlichen Dimensionen des Eingabe tensor *InputTensor*, die auch der Anzahl der Dimensionen des gleitenden *Fensters WindowSize* entspricht.</span><span class="sxs-lookup"><span data-stu-id="01242-120">The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*.</span></span> <span data-ttu-id="01242-121">Dieser Wert bestimmt auch die Größe der Arrays *Strides,* *StartPadding* und *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="01242-121">This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="01242-122">Sie sollte auf 2 festgelegt werden, wenn *InputTensor* 4D ist, und 3, wenn es sich um einen 5D-Tensor handelt.</span><span class="sxs-lookup"><span data-stu-id="01242-122">It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.</span></span>


`Strides`

<span data-ttu-id="01242-123">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="01242-123">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="01242-124">Die Schritte für die Größendimensionen des gleitenden Fensters, wenn DimensionCount auf 2 oder auf `{ Height, Width }`  `{ Depth, Height, Width }` 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="01242-124">The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`WindowSize`

<span data-ttu-id="01242-125">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="01242-125">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="01242-126">Die Dimensionen des gleitenden Fensters in `{ Height, Width }` , *wenn DimensionCount* auf 2 oder `{ Depth, Height, Width }` auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="01242-126">The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`StartPadding`

<span data-ttu-id="01242-127">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="01242-127">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="01242-128">Die Anzahl der Auf padding-Elemente, die auf den Anfang jeder räumlichen Dimension des Eingabe tensor *InputTensor angewendet werden sollen.*</span><span class="sxs-lookup"><span data-stu-id="01242-128">The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="01242-129">Die Werte befinden sich in `{ Height, Width }` , *wenn DimensionCount* auf 2 oder `{ Depth, Height, Width }` auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="01242-129">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`EndPadding`

<span data-ttu-id="01242-130">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="01242-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="01242-131">Die Anzahl der Auf padding-Elemente, die auf das Ende jeder räumlichen Dimension des Eingabe tensor *InputTensor angewendet werden sollen.*</span><span class="sxs-lookup"><span data-stu-id="01242-131">The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="01242-132">Die Werte befinden sich in `{ Height, Width }` , *wenn DimensionCount* auf 2 oder `{ Depth, Height, Width }` auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="01242-132">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`Dilations`

<span data-ttu-id="01242-133">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="01242-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="01242-134">Die Werte für jede räumliche Dimension des Eingabe tensor *InputTensor,* mit dem ein Element innerhalb des gleitenden Fensters für jedes Element dieses Werts ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="01242-134">The values for each spatial dimension of the input tensor *InputTensor* by which an element within the sliding window is selected for every elements of that value.</span></span> <span data-ttu-id="01242-135">Die Werte befinden sich in `{ Height, Width }` , *wenn DimensionCount* auf 2 oder `{ Depth, Height, Width }` auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="01242-135">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


## <a name="remarks"></a><span data-ttu-id="01242-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01242-136">Remarks</span></span>
<span data-ttu-id="01242-137">**DML_MAX_POOLING2_OPERATOR_DESC** ersetzt die frühere Version DML_MAX_POOLING_OPERATOR1_DESC [durch](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) eine zusätzliche konstante *Arraydilierung*.</span><span class="sxs-lookup"><span data-stu-id="01242-137">**DML_MAX_POOLING2_OPERATOR_DESC** supersedes the earlier version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) with an additional constant array *Dilations*.</span></span> <span data-ttu-id="01242-138">Die beiden Versionen sind gleichwertig, *wenn Dilations* für 4D-Eingaben oder `{ 1,1 }` für `{ 1,1,1 }` 5D-Eingabefeatures auf festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="01242-138">The two versions are equivalent when *Dilations* is set to `{ 1,1 }` for 4D input, or `{ 1,1,1 }` for 5D input features.</span></span>

## <a name="availability"></a><span data-ttu-id="01242-139">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="01242-139">Availability</span></span>
<span data-ttu-id="01242-140">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01242-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="01242-141">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="01242-141">Tensor constraints</span></span>
* <span data-ttu-id="01242-142">*InputTensor,* *OutputIndicesTensor* und *OutputTensor* müssen denselben *DimensionCount aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="01242-142">*InputTensor*, *OutputIndicesTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="01242-143">*InputTensor und* *OutputTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="01242-143">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="01242-144">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="01242-144">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="01242-145">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="01242-145">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="01242-146">Tensor</span><span class="sxs-lookup"><span data-stu-id="01242-146">Tensor</span></span> | <span data-ttu-id="01242-147">Typ</span><span class="sxs-lookup"><span data-stu-id="01242-147">Kind</span></span> | <span data-ttu-id="01242-148">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="01242-148">Supported dimension counts</span></span> | <span data-ttu-id="01242-149">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="01242-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="01242-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="01242-150">InputTensor</span></span> | <span data-ttu-id="01242-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="01242-151">Input</span></span> | <span data-ttu-id="01242-152">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="01242-152">4 to 5</span></span> | <span data-ttu-id="01242-153">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="01242-153">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="01242-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="01242-154">OutputTensor</span></span> | <span data-ttu-id="01242-155">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="01242-155">Output</span></span> | <span data-ttu-id="01242-156">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="01242-156">4 to 5</span></span> | <span data-ttu-id="01242-157">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="01242-157">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="01242-158">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="01242-158">OutputIndicesTensor</span></span> | <span data-ttu-id="01242-159">Optionale Ausgabe</span><span class="sxs-lookup"><span data-stu-id="01242-159">Optional output</span></span> | <span data-ttu-id="01242-160">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="01242-160">4 to 5</span></span> | <span data-ttu-id="01242-161">UINT32</span><span class="sxs-lookup"><span data-stu-id="01242-161">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="01242-162">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="01242-162">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="01242-163">Tensor</span><span class="sxs-lookup"><span data-stu-id="01242-163">Tensor</span></span> | <span data-ttu-id="01242-164">Typ</span><span class="sxs-lookup"><span data-stu-id="01242-164">Kind</span></span> | <span data-ttu-id="01242-165">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="01242-165">Supported dimension counts</span></span> | <span data-ttu-id="01242-166">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="01242-166">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="01242-167">InputTensor</span><span class="sxs-lookup"><span data-stu-id="01242-167">InputTensor</span></span> | <span data-ttu-id="01242-168">Eingabe</span><span class="sxs-lookup"><span data-stu-id="01242-168">Input</span></span> | <span data-ttu-id="01242-169">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="01242-169">4 to 5</span></span> | <span data-ttu-id="01242-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="01242-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="01242-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="01242-171">OutputTensor</span></span> | <span data-ttu-id="01242-172">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="01242-172">Output</span></span> | <span data-ttu-id="01242-173">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="01242-173">4 to 5</span></span> | <span data-ttu-id="01242-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="01242-174">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="01242-175">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="01242-175">OutputIndicesTensor</span></span> | <span data-ttu-id="01242-176">Optionale Ausgabe</span><span class="sxs-lookup"><span data-stu-id="01242-176">Optional output</span></span> | <span data-ttu-id="01242-177">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="01242-177">4 to 5</span></span> | <span data-ttu-id="01242-178">UINT32</span><span class="sxs-lookup"><span data-stu-id="01242-178">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="01242-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01242-179">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="01242-180">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="01242-180">**Minimum supported client**</span></span> | <span data-ttu-id="01242-181">Windows 10, Version 2004 (10.0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="01242-181">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="01242-182">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="01242-182">**Minimum supported server**</span></span> | <span data-ttu-id="01242-183">Windows Server, Version 2004 (10.0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="01242-183">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="01242-184">**Header**</span><span class="sxs-lookup"><span data-stu-id="01242-184">**Header**</span></span> | <span data-ttu-id="01242-185">directml.h</span><span class="sxs-lookup"><span data-stu-id="01242-185">directml.h</span></span> |