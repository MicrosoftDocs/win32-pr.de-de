---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Erfasst Elemente aus dem Eingabetensor und verwendet dabei den Indizestensor, um Indizes vollständigen Teilblöcken der Eingabe neu zuordnen. | DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: b92c8aece88d8466357bb8e48fd3ce5a3b73d2e3
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802859"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a><span data-ttu-id="4aeef-104">DML_GATHER_ND1_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="4aeef-104">DML_GATHER_ND1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="4aeef-105">Erfasst Elemente aus dem Eingabetensor und verwendet den Indizestensor, um Indizes vollständigen Teilblöcken der Eingabe neu zuordnen.</span><span class="sxs-lookup"><span data-stu-id="4aeef-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="4aeef-106">Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten dar, deren genaues Verhalten von der Anzahl der Batch-, Eingabe- und Indizesdimensionen abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="4aeef-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the batch, input, and indices dimension count.</span></span>

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> <span data-ttu-id="4aeef-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="4aeef-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4aeef-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="4aeef-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4aeef-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aeef-109">Syntax</span></span>

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a><span data-ttu-id="4aeef-110">Member</span><span class="sxs-lookup"><span data-stu-id="4aeef-110">Members</span></span>

`InputTensor`

<span data-ttu-id="4aeef-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4aeef-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4aeef-112">Der Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4aeef-112">The tensor to read from.</span></span>

`IndicesTensor`

<span data-ttu-id="4aeef-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4aeef-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4aeef-114">Der Tensor, der die Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="4aeef-114">The tensor containing the indices.</span></span> <span data-ttu-id="4aeef-115">DimensionCount *dieses* Tensors muss mit *InputTensor.DimensionCount übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="4aeef-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="4aeef-116">Die letzte Dimension des *IndicesTensor* ist tatsächlich die Anzahl der Koordinaten pro Index-Tupel und darf *InputTensor.DimensionCount nicht überschreiten.*</span><span class="sxs-lookup"><span data-stu-id="4aeef-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="4aeef-117">Beispielsweise bedeutet ein *Indizestensor* von Größen mit `{1,4,5,2}` *IndicesDimensionCount* = 3 ein 4x5-Array von Zweikoordinaten-Tupeln, die in *InputTensor* indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4aeef-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="4aeef-118">Ab unterstützt dieser Operator negative Indexwerte, wenn ein integraler Typ mit `DML_FEATURE_LEVEL_3_0` Vorsignierung mit diesem Tensor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4aeef-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="4aeef-119">Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert.</span><span class="sxs-lookup"><span data-stu-id="4aeef-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="4aeef-120">Ein Index von -1 bezieht sich beispielsweise auf das letzte Element in dieser Dimension.</span><span class="sxs-lookup"><span data-stu-id="4aeef-120">For example, an index of -1 refers to the last element along that dimension.</span></span>

`OutputTensor`

<span data-ttu-id="4aeef-121">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4aeef-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4aeef-122">Der Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4aeef-122">The tensor to write the results to.</span></span> <span data-ttu-id="4aeef-123">*DimensionCount und* *DataType dieses* Tensors müssen mit *InputTensor.DimensionCount übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="4aeef-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="4aeef-124">Die *erwarteten OutputTensor.Sizes* sind die Verkettung der führenden *IndizesTensor.Sizes* und des nachgestellten Segments *InputTensor.Sizes,* was Folgendes ergibt.</span><span class="sxs-lookup"><span data-stu-id="4aeef-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment, which yields the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="4aeef-125">Die Dimensionen sind rechtsbündig ausgerichtet, wobei bei Bedarf führende 1 Werte voranstellen, um *OutputTensor.DimensionCount* zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4aeef-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="4aeef-126">Hier sehen Sie ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="4aeef-126">Here's an example.</span></span>

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```

`InputDimensionCount`

<span data-ttu-id="4aeef-127">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4aeef-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4aeef-128">Die Anzahl der tatsächlichen Eingabedimensionen innerhalb des *InputTensor,* nachdem irrelevante führende Dimensionen ignoriert wurden, die im Bereich von `[1, *InputTensor.DimensionCount*]` sind.</span><span class="sxs-lookup"><span data-stu-id="4aeef-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="4aeef-129">Wenn beispielsweise *InputTensor.Sizes* und = 3 angegeben  =  `{1,1,4,6}` `InputDimensionCount` sind, sind die tatsächlichen aussagekräftigen Indizes `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="4aeef-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`IndicesDimensionCount`

<span data-ttu-id="4aeef-130">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4aeef-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4aeef-131">Die Anzahl der tatsächlichen Indexdimensionen innerhalb des *Indextensors* nach dem Ignorieren irrelevanter führender Dimensionen im Bereich [1, *IndizesTensor.DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="4aeef-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="4aeef-132">Bei *IndizesTensor.Sizes*  =  `{1,1,4,6}` und *IndizesDimensionCount* = 3 sind die tatsächlichen aussagekräftigen Indizes beispielsweise `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="4aeef-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`BatchDimensionCount`

<span data-ttu-id="4aeef-133">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4aeef-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4aeef-134">Die Anzahl der Dimensionen innerhalb jedes Tensors (*InputTensor*, *IndicesTensor*, *OutputTensor*), die als unabhängige Batches betrachtet werden und sowohl innerhalb von [0, *InputTensor.DimensionCount*) als auch [0, *IndicesTensor.DimensionCount*) liegen.</span><span class="sxs-lookup"><span data-stu-id="4aeef-134">The number of dimensions within each tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) that are considered independent batches, ranging within both [0, *InputTensor.DimensionCount*) and [0, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="4aeef-135">Die Batchanzahl kann 0 sein, was einen einzelnen Batch impliziert.</span><span class="sxs-lookup"><span data-stu-id="4aeef-135">The batch count can be 0, implying a single batch.</span></span> <span data-ttu-id="4aeef-136">Bei *IndizesTensor.Sizes*  =  `{1,3,4,5,6,7}` und *IndizesDimensionCount* = 5 und = 2 gibt es beispielsweise `BatchDimensionCount` Batches und aussagekräftige `{3,4}` `{5,6,7}` Indizes.</span><span class="sxs-lookup"><span data-stu-id="4aeef-136">For example, given *IndicesTensor.Sizes* = `{1,3,4,5,6,7}`, and *IndicesDimensionCount* = 5 and `BatchDimensionCount` = 2, there are batches `{3,4}` and meaningful indices `{5,6,7}`.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aeef-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4aeef-137">Remarks</span></span>
<span data-ttu-id="4aeef-138">**DML_GATHER_ND1_OPERATOR_DESC** fügt *BatchDimensionCount* hinzu und entspricht [DML_GATHER_ND_OPERATOR_DESC,](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) wenn *BatchDimensionCount* = 0 ist.</span><span class="sxs-lookup"><span data-stu-id="4aeef-138">**DML_GATHER_ND1_OPERATOR_DESC** adds *BatchDimensionCount*, and is equivalent to [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) when *BatchDimensionCount* = 0.</span></span>

## <a name="examples"></a><span data-ttu-id="4aeef-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4aeef-139">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="4aeef-140">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="4aeef-140">Example 1.</span></span> <span data-ttu-id="4aeef-141">1D-Neuzuordnung</span><span class="sxs-lookup"><span data-stu-id="4aeef-141">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a><span data-ttu-id="4aeef-142">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="4aeef-142">Example 2.</span></span> <span data-ttu-id="4aeef-143">2D-Neuzuordnung mit Batchanzahl</span><span class="sxs-lookup"><span data-stu-id="4aeef-143">2D remapping with batch count</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a><span data-ttu-id="4aeef-144">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="4aeef-144">Availability</span></span>
<span data-ttu-id="4aeef-145">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4aeef-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4aeef-146">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="4aeef-146">Tensor constraints</span></span>
* <span data-ttu-id="4aeef-147">*IndicesTensor,* *InputTensor* und *OutputTensor* müssen über den gleichen *DimensionCount verfügen.*</span><span class="sxs-lookup"><span data-stu-id="4aeef-147">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="4aeef-148">*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="4aeef-148">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4aeef-149">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="4aeef-149">Tensor support</span></span>
| <span data-ttu-id="4aeef-150">Tensor</span><span class="sxs-lookup"><span data-stu-id="4aeef-150">Tensor</span></span> | <span data-ttu-id="4aeef-151">Typ</span><span class="sxs-lookup"><span data-stu-id="4aeef-151">Kind</span></span> | <span data-ttu-id="4aeef-152">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="4aeef-152">Supported dimension counts</span></span> | <span data-ttu-id="4aeef-153">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="4aeef-153">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4aeef-154">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4aeef-154">InputTensor</span></span> | <span data-ttu-id="4aeef-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4aeef-155">Input</span></span> | <span data-ttu-id="4aeef-156">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="4aeef-156">1 to 8</span></span> | <span data-ttu-id="4aeef-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4aeef-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="4aeef-158">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="4aeef-158">IndicesTensor</span></span> | <span data-ttu-id="4aeef-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4aeef-159">Input</span></span> | <span data-ttu-id="4aeef-160">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="4aeef-160">1 to 8</span></span> | <span data-ttu-id="4aeef-161">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="4aeef-161">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="4aeef-162">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4aeef-162">OutputTensor</span></span> | <span data-ttu-id="4aeef-163">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="4aeef-163">Output</span></span> | <span data-ttu-id="4aeef-164">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="4aeef-164">1 to 8</span></span> | <span data-ttu-id="4aeef-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4aeef-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="4aeef-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4aeef-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4aeef-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="4aeef-167">**Header**</span></span> | <span data-ttu-id="4aeef-168">directml.h</span><span class="sxs-lookup"><span data-stu-id="4aeef-168">directml.h</span></span> |
