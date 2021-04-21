---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Kehrt die Elemente einer oder mehrerer *Unterabfragen* eines Tensors um. Der Satz von Teilsequenzen, die umgekehrt werden sollen, wird basierend auf der bereitgestellten Achse und sequenzierten Längen ausgewählt.
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
ms.openlocfilehash: 3deddea3d60db1a8689ceabfac92ff17393b7606
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803999"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a><span data-ttu-id="a9a29-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="a9a29-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="a9a29-105">Kehrt die Elemente einer oder mehrerer *Unterabfragen* eines Tensors um.</span><span class="sxs-lookup"><span data-stu-id="a9a29-105">Reverses the elements of one or more *subsequences* of a tensor.</span></span> <span data-ttu-id="a9a29-106">Der Satz von Teilsequenzen, die umgekehrt werden sollen, wird basierend auf der bereitgestellten Achse und sequenzierten Längen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a9a29-106">The set of subsequences to be reversed is chosen based on the provided axis and sequence lengths.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9a29-107">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="a9a29-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a9a29-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="a9a29-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a29-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9a29-109">Syntax</span></span>
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="a9a29-110">Member</span><span class="sxs-lookup"><span data-stu-id="a9a29-110">Members</span></span>

`InputTensor`

<span data-ttu-id="a9a29-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9a29-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9a29-112">Der Eingabe-Tensor, der elemente enthält, die umgekehrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9a29-112">The input tensor containing elements to be reversed.</span></span>


`SequenceLengthsTensor`

<span data-ttu-id="a9a29-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9a29-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9a29-114">Ein Tensor, der einen Wert für jede umgekehrte Untersequence enthält, der die Länge in Elementen dieser Unterabfrage anzeige.</span><span class="sxs-lookup"><span data-stu-id="a9a29-114">A tensor containing a value for each subsequence to be reversed, denoting the length in elements of that subsequence.</span></span> <span data-ttu-id="a9a29-115">Nur die Elemente innerhalb der Länge der Unterabfrage werden umgekehrt. die verbleibenden Elemente entlang dieser Achse werden unverändert in die Ausgabe kopiert.</span><span class="sxs-lookup"><span data-stu-id="a9a29-115">Only the elements within the length of the subsequence are reversed; the remaining elements along that axis are copied to the output unchanged.</span></span>

<span data-ttu-id="a9a29-116">Dieser Tensor muss die Dimensionsanzahl und -größen aufweisen, die dem *InputTensor* entsprechen, *mit Ausnahme* der Dimension, die durch den *Axis-Parameter* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a9a29-116">This tensor must have dimension count and sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter.</span></span> <span data-ttu-id="a9a29-117">Die Größe der *Dimension Achse* muss 1 sein.</span><span class="sxs-lookup"><span data-stu-id="a9a29-117">The size of the *Axis* dimension must be 1.</span></span> <span data-ttu-id="a9a29-118">Wenn der *InputTensor* z. B. die Größen `{2,3,4,5}` hat und *Achse* 1 ist, müssen die Größen von *SequenceLengthsTensor* `{2,1,4,5}` sein.</span><span class="sxs-lookup"><span data-stu-id="a9a29-118">For example if the *InputTensor* has sizes of `{2,3,4,5}`, and *Axis* is 1, then the sizes of the *SequenceLengthsTensor* must be `{2,1,4,5}`.</span></span>

<span data-ttu-id="a9a29-119">Wenn die Länge einer Unterabfrage die maximale Anzahl von Elementen entlang dieser Achse überschreitet, verhält sich dieser Operator so, als ob der Wert an den Höchstwert geklammert wäre.</span><span class="sxs-lookup"><span data-stu-id="a9a29-119">If the length of a subsequence exceeds the maximum number of elements along that axis, then this operator behaves as if the value were clamped to the maximum.</span></span>


`OutputTensor`

<span data-ttu-id="a9a29-120">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9a29-120">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9a29-121">Der Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9a29-121">The output tensor to write the results to.</span></span> <span data-ttu-id="a9a29-122">Dieser Tensor muss die gleichen Größen und denselben Datentyp wie *inputTensor aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="a9a29-122">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="a9a29-123">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a9a29-123">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="a9a29-124">Der Index der Dimension, um die Elemente umgekehrt werden.</span><span class="sxs-lookup"><span data-stu-id="a9a29-124">The index of the dimension to reverse elements over.</span></span> <span data-ttu-id="a9a29-125">Dieser Wert muss kleiner als dimensionCount des *InputTensor-Werts sein.*</span><span class="sxs-lookup"><span data-stu-id="a9a29-125">This value must be less than the DimensionCount of the *InputTensor*.</span></span>

## <a name="examples"></a><span data-ttu-id="a9a29-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9a29-126">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="a9a29-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9a29-127">Example 1</span></span>

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

### <a name="example-2-reversing-along-a-different-axis"></a><span data-ttu-id="a9a29-128">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="a9a29-128">Example 2.</span></span> <span data-ttu-id="a9a29-129">Umkehren entlang einer anderen Achse</span><span class="sxs-lookup"><span data-stu-id="a9a29-129">Reversing along a different axis</span></span>

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

## <a name="availability"></a><span data-ttu-id="a9a29-130">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="a9a29-130">Availability</span></span>
<span data-ttu-id="a9a29-131">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a9a29-131">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a9a29-132">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="a9a29-132">Tensor constraints</span></span>
* <span data-ttu-id="a9a29-133">*InputTensor,* *OutputTensor* und *SequenceLengthsTensor* müssen denselben *DimensionCount aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="a9a29-133">*InputTensor*, *OutputTensor*, and *SequenceLengthsTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="a9a29-134">*InputTensor und* *OutputTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="a9a29-134">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a9a29-135">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a9a29-135">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="a9a29-136">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="a9a29-136">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="a9a29-137">Tensor</span><span class="sxs-lookup"><span data-stu-id="a9a29-137">Tensor</span></span> | <span data-ttu-id="a9a29-138">Typ</span><span class="sxs-lookup"><span data-stu-id="a9a29-138">Kind</span></span> | <span data-ttu-id="a9a29-139">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="a9a29-139">Supported dimension counts</span></span> | <span data-ttu-id="a9a29-140">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="a9a29-140">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a9a29-141">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a9a29-141">InputTensor</span></span> | <span data-ttu-id="a9a29-142">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9a29-142">Input</span></span> | <span data-ttu-id="a9a29-143">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="a9a29-143">4 to 5</span></span> | <span data-ttu-id="a9a29-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a9a29-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a9a29-145">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="a9a29-145">SequenceLengthsTensor</span></span> | <span data-ttu-id="a9a29-146">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9a29-146">Input</span></span> | <span data-ttu-id="a9a29-147">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="a9a29-147">4 to 5</span></span> | <span data-ttu-id="a9a29-148">UINT32</span><span class="sxs-lookup"><span data-stu-id="a9a29-148">UINT32</span></span> |
| <span data-ttu-id="a9a29-149">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a9a29-149">OutputTensor</span></span> | <span data-ttu-id="a9a29-150">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a9a29-150">Output</span></span> | <span data-ttu-id="a9a29-151">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="a9a29-151">4 to 5</span></span> | <span data-ttu-id="a9a29-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a9a29-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="a9a29-153">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="a9a29-153">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="a9a29-154">Tensor</span><span class="sxs-lookup"><span data-stu-id="a9a29-154">Tensor</span></span> | <span data-ttu-id="a9a29-155">Typ</span><span class="sxs-lookup"><span data-stu-id="a9a29-155">Kind</span></span> | <span data-ttu-id="a9a29-156">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="a9a29-156">Supported dimension counts</span></span> | <span data-ttu-id="a9a29-157">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="a9a29-157">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a9a29-158">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a9a29-158">InputTensor</span></span> | <span data-ttu-id="a9a29-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9a29-159">Input</span></span> | <span data-ttu-id="a9a29-160">4</span><span class="sxs-lookup"><span data-stu-id="a9a29-160">4</span></span> | <span data-ttu-id="a9a29-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a9a29-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a9a29-162">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="a9a29-162">SequenceLengthsTensor</span></span> | <span data-ttu-id="a9a29-163">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9a29-163">Input</span></span> | <span data-ttu-id="a9a29-164">4</span><span class="sxs-lookup"><span data-stu-id="a9a29-164">4</span></span> | <span data-ttu-id="a9a29-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="a9a29-165">UINT32</span></span> |
| <span data-ttu-id="a9a29-166">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a9a29-166">OutputTensor</span></span> | <span data-ttu-id="a9a29-167">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a9a29-167">Output</span></span> | <span data-ttu-id="a9a29-168">4</span><span class="sxs-lookup"><span data-stu-id="a9a29-168">4</span></span> | <span data-ttu-id="a9a29-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a9a29-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="a9a29-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9a29-170">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a9a29-171">**Header**</span><span class="sxs-lookup"><span data-stu-id="a9a29-171">**Header**</span></span> | <span data-ttu-id="a9a29-172">directml.h</span><span class="sxs-lookup"><span data-stu-id="a9a29-172">directml.h</span></span> |