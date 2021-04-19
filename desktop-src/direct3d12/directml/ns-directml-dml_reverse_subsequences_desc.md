---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Kehrt die Elemente einer *oder mehrerer unter* Sequenzen eines Tensors um. Der Satz von unter Sequenzen, der umgekehrt werden soll, wird basierend auf der angegebenen Achse und den angegebenen Sequenz Längen ausgewählt.
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 5baf16c5acd1ce5c5f44e68420e93aabaa276ea7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106366541"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a><span data-ttu-id="8b03b-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="8b03b-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="8b03b-105">Kehrt die Elemente einer *oder mehrerer unter* Sequenzen eines Tensors um.</span><span class="sxs-lookup"><span data-stu-id="8b03b-105">Reverses the elements of one or more *subsequences* of a tensor.</span></span> <span data-ttu-id="8b03b-106">Der Satz von unter Sequenzen, der umgekehrt werden soll, wird basierend auf der angegebenen Achse und den angegebenen Sequenz Längen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8b03b-106">The set of subsequences to be reversed is chosen based on the provided axis and sequence lengths.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b03b-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="8b03b-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="8b03b-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8b03b-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b03b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b03b-109">Syntax</span></span>
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="8b03b-110">Member</span><span class="sxs-lookup"><span data-stu-id="8b03b-110">Members</span></span>

`InputTensor`

<span data-ttu-id="8b03b-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8b03b-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8b03b-112">Der eingabetensor mit Elementen, die umgekehrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b03b-112">The input tensor containing elements to be reversed.</span></span>


`SequenceLengthsTensor`

<span data-ttu-id="8b03b-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8b03b-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8b03b-114">Ein tensorflow, der einen Wert für jede unter Sequenz enthält, die umgekehrt werden soll, wobei die Länge in Elementen dieser unter Sequenz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8b03b-114">A tensor containing a value for each subsequence to be reversed, denoting the length in elements of that subsequence.</span></span> <span data-ttu-id="8b03b-115">Nur die Elemente innerhalb der Länge der unter Sequenz werden umgekehrt. die übrigen Elemente auf dieser Achse werden unverändert in die Ausgabe kopiert.</span><span class="sxs-lookup"><span data-stu-id="8b03b-115">Only the elements within the length of the subsequence are reversed; the remaining elements along that axis are copied to the output unchanged.</span></span>

<span data-ttu-id="8b03b-116">Dieser Mandanten muss die Anzahl und die Größe der Dimensionen gleich dem *inputtensor* aufweisen, *außer* der durch den Parameter *Axis* angegebenen Dimension.</span><span class="sxs-lookup"><span data-stu-id="8b03b-116">This tensor must have dimension count and sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter.</span></span> <span data-ttu-id="8b03b-117">Die Größe der *Achsen* Dimension muss 1 sein.</span><span class="sxs-lookup"><span data-stu-id="8b03b-117">The size of the *Axis* dimension must be 1.</span></span> <span data-ttu-id="8b03b-118">Wenn z. b. die Größe von *inputtensor* `{2,3,4,5}` und die *Achse* 1 beträgt, muss die Größe von " *sequencelengthstensor* " lauten `{2,1,4,5}` .</span><span class="sxs-lookup"><span data-stu-id="8b03b-118">For example if the *InputTensor* has sizes of `{2,3,4,5}`, and *Axis* is 1, then the sizes of the *SequenceLengthsTensor* must be `{2,1,4,5}`.</span></span>

<span data-ttu-id="8b03b-119">Wenn die Länge einer unter Sequenz die maximale Anzahl von Elementen auf dieser Achse überschreitet, verhält sich dieser Operator so, als ob der Wert an den maximalen Wert gebunden wäre.</span><span class="sxs-lookup"><span data-stu-id="8b03b-119">If the length of a subsequence exceeds the maximum number of elements along that axis, then this operator behaves as if the value were clamped to the maximum.</span></span>


`OutputTensor`

<span data-ttu-id="8b03b-120">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8b03b-120">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8b03b-121">Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b03b-121">The output tensor to write the results to.</span></span> <span data-ttu-id="8b03b-122">Dieser Mandanten muss dieselbe Größe und denselben Datentyp aufweisen wie der *inputtensor*.</span><span class="sxs-lookup"><span data-stu-id="8b03b-122">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="8b03b-123">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8b03b-123">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8b03b-124">Der Index der Dimension, über die Elemente umgekehrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b03b-124">The index of the dimension to reverse elements over.</span></span> <span data-ttu-id="8b03b-125">Dieser Wert muss kleiner als die DimensionCount von " *inputtensor*" sein.</span><span class="sxs-lookup"><span data-stu-id="8b03b-125">This value must be less than the DimensionCount of the *InputTensor*.</span></span>

## <a name="examples"></a><span data-ttu-id="8b03b-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b03b-126">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="8b03b-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b03b-127">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a><span data-ttu-id="8b03b-128">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="8b03b-128">Example 2.</span></span> <span data-ttu-id="8b03b-129">Umkehren an einer anderen Achse</span><span class="sxs-lookup"><span data-stu-id="8b03b-129">Reversing along a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a><span data-ttu-id="8b03b-130">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="8b03b-130">Availability</span></span>
<span data-ttu-id="8b03b-131">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8b03b-131">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8b03b-132">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="8b03b-132">Tensor constraints</span></span>
* <span data-ttu-id="8b03b-133">" *Inputtensor*", " *outputtensor*" und " *sequencelengthstensor* " müssen dieselbe *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8b03b-133">*InputTensor*, *OutputTensor*, and *SequenceLengthsTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="8b03b-134">*Inputtensor* und *outputtensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8b03b-134">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8b03b-135">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="8b03b-135">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="8b03b-136">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="8b03b-136">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="8b03b-137">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="8b03b-137">Tensor</span></span> | <span data-ttu-id="8b03b-138">Typ</span><span class="sxs-lookup"><span data-stu-id="8b03b-138">Kind</span></span> | <span data-ttu-id="8b03b-139">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="8b03b-139">Supported dimension counts</span></span> | <span data-ttu-id="8b03b-140">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="8b03b-140">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8b03b-141">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="8b03b-141">InputTensor</span></span> | <span data-ttu-id="8b03b-142">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b03b-142">Input</span></span> | <span data-ttu-id="8b03b-143">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="8b03b-143">4 to 5</span></span> | <span data-ttu-id="8b03b-144">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="8b03b-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8b03b-145">Sequencelengthstensor</span><span class="sxs-lookup"><span data-stu-id="8b03b-145">SequenceLengthsTensor</span></span> | <span data-ttu-id="8b03b-146">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b03b-146">Input</span></span> | <span data-ttu-id="8b03b-147">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="8b03b-147">4 to 5</span></span> | <span data-ttu-id="8b03b-148">UINT32</span><span class="sxs-lookup"><span data-stu-id="8b03b-148">UINT32</span></span> |
| <span data-ttu-id="8b03b-149">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="8b03b-149">OutputTensor</span></span> | <span data-ttu-id="8b03b-150">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8b03b-150">Output</span></span> | <span data-ttu-id="8b03b-151">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="8b03b-151">4 to 5</span></span> | <span data-ttu-id="8b03b-152">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="8b03b-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="8b03b-153">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="8b03b-153">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="8b03b-154">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="8b03b-154">Tensor</span></span> | <span data-ttu-id="8b03b-155">Typ</span><span class="sxs-lookup"><span data-stu-id="8b03b-155">Kind</span></span> | <span data-ttu-id="8b03b-156">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="8b03b-156">Supported dimension counts</span></span> | <span data-ttu-id="8b03b-157">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="8b03b-157">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8b03b-158">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="8b03b-158">InputTensor</span></span> | <span data-ttu-id="8b03b-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b03b-159">Input</span></span> | <span data-ttu-id="8b03b-160">4</span><span class="sxs-lookup"><span data-stu-id="8b03b-160">4</span></span> | <span data-ttu-id="8b03b-161">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="8b03b-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8b03b-162">Sequencelengthstensor</span><span class="sxs-lookup"><span data-stu-id="8b03b-162">SequenceLengthsTensor</span></span> | <span data-ttu-id="8b03b-163">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b03b-163">Input</span></span> | <span data-ttu-id="8b03b-164">4</span><span class="sxs-lookup"><span data-stu-id="8b03b-164">4</span></span> | <span data-ttu-id="8b03b-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="8b03b-165">UINT32</span></span> |
| <span data-ttu-id="8b03b-166">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="8b03b-166">OutputTensor</span></span> | <span data-ttu-id="8b03b-167">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8b03b-167">Output</span></span> | <span data-ttu-id="8b03b-168">4</span><span class="sxs-lookup"><span data-stu-id="8b03b-168">4</span></span> | <span data-ttu-id="8b03b-169">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="8b03b-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="8b03b-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b03b-170">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8b03b-171">**Header**</span><span class="sxs-lookup"><span data-stu-id="8b03b-171">**Header**</span></span> | <span data-ttu-id="8b03b-172">directml. h</span><span class="sxs-lookup"><span data-stu-id="8b03b-172">directml.h</span></span> |