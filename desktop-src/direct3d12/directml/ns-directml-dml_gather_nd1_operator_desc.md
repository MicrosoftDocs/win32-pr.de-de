---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Erfasst Elemente aus dem Eingabe-Tensor und verwendet den Index-Tensor, um Indizes ganzen Unterblöcken der Eingabe neu zuzuordnen. | DML_GATHER_ND1_OPERATOR_DESC
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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417613"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a><span data-ttu-id="00089-104">DML_GATHER_ND1_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="00089-104">DML_GATHER_ND1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="00089-105">Erfasst Elemente aus dem Eingabe-Tensor und verwendet den Index-Tensor, um Indizes ganzen Unterblöcken der Eingabe neu zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="00089-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="00089-106">Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten dar, wobei das genaue Verhalten von der Batch-, Eingabe- und Indexdimensionsanzahl abhängt.</span><span class="sxs-lookup"><span data-stu-id="00089-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the batch, input, and indices dimension count.</span></span>

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> <span data-ttu-id="00089-107">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="00089-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="00089-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="00089-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="00089-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="00089-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="00089-110">Member</span><span class="sxs-lookup"><span data-stu-id="00089-110">Members</span></span>

`InputTensor`

<span data-ttu-id="00089-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="00089-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="00089-112">Der Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="00089-112">The tensor to read from.</span></span>

`IndicesTensor`

<span data-ttu-id="00089-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="00089-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="00089-114">Der Tensor, der die Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="00089-114">The tensor containing the indices.</span></span> <span data-ttu-id="00089-115">*DimensionCount* dieses Tensors muss mit *InputTensor.DimensionCount* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="00089-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="00089-116">Die letzte Dimension von *IndicesTensor* ist tatsächlich die Anzahl der Koordinaten pro Indextupel und darf *inputTensor.DimensionCount* nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="00089-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="00089-117">Ein Index-Tensor von *Sizes* `{1,4,5,2}` mit *IndizesDimensionCount* = 3 bedeutet beispielsweise ein 4x5-Array von 2-Koordinaten-Tupeln, die in *InputTensor* indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="00089-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="00089-118">Ab `DML_FEATURE_LEVEL_3_0` unterstützt dieser Operator negative Indexwerte, wenn ein ganzzahligen Typ mit Vorzeichen mit diesem Tensor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00089-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="00089-119">Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert.</span><span class="sxs-lookup"><span data-stu-id="00089-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="00089-120">Beispielsweise bezieht sich ein Index von -1 auf das letzte Element entlang dieser Dimension.</span><span class="sxs-lookup"><span data-stu-id="00089-120">For example, an index of -1 refers to the last element along that dimension.</span></span>

`OutputTensor`

<span data-ttu-id="00089-121">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="00089-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="00089-122">Der Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00089-122">The tensor to write the results to.</span></span> <span data-ttu-id="00089-123">*DimensionCount* und *DataType* dieses Tensors müssen mit *InputTensor.DimensionCount* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="00089-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="00089-124">Die *erwarteten OutputTensor.Sizes* sind die Verkettung der führenden *Segmente IndicesTensor.Sizes* und des nachgestellten Segments *InputTensor.Sizes,* was Folgendes ergibt.</span><span class="sxs-lookup"><span data-stu-id="00089-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment, which yields the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="00089-125">Die Dimensionen sind rechtsbündig ausgerichtet, wobei bei Bedarf führende 1 Werte voranstellen, um *OutputTensor.DimensionCount* zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="00089-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="00089-126">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="00089-126">Here's an example.</span></span>

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

<span data-ttu-id="00089-127">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="00089-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="00089-128">Die Anzahl der tatsächlichen Eingabedimensionen innerhalb des *InputTensor,* nachdem irrelevante führende Dimensionen ignoriert wurden, die im Bereich von `[1, *InputTensor.DimensionCount*]` sind.</span><span class="sxs-lookup"><span data-stu-id="00089-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="00089-129">Wenn beispielsweise *InputTensor.Sizes* und = 3 angegeben  =  `{1,1,4,6}` `InputDimensionCount` sind, sind die tatsächlichen aussagekräftigen Indizes `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="00089-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`IndicesDimensionCount`

<span data-ttu-id="00089-130">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="00089-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="00089-131">Die Anzahl der tatsächlichen Indexdimensionen innerhalb des *Indextensors,* nachdem irrelevante führende Dimensionen ignoriert wurden, die im Bereich [1, *IndizesTensor.DimensionCount*] liegen.</span><span class="sxs-lookup"><span data-stu-id="00089-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="00089-132">Bei *IndizesTensor.Sizes*  =  `{1,1,4,6}` und *IndizesDimensionCount* = 3 sind die tatsächlichen aussagekräftigen Indizes beispielsweise `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="00089-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`BatchDimensionCount`

<span data-ttu-id="00089-133">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="00089-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="00089-134">Die Anzahl der Dimensionen innerhalb jedes Tensors (*InputTensor*, *IndicesTensor*, *OutputTensor*), die als unabhängige Batches betrachtet werden und sowohl innerhalb von [0, *InputTensor.DimensionCount*) als auch [0, *IndicesTensor.DimensionCount*) liegen.</span><span class="sxs-lookup"><span data-stu-id="00089-134">The number of dimensions within each tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) that are considered independent batches, ranging within both [0, *InputTensor.DimensionCount*) and [0, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="00089-135">Die Batchanzahl kann 0 sein, was einen einzelnen Batch impliziert.</span><span class="sxs-lookup"><span data-stu-id="00089-135">The batch count can be 0, implying a single batch.</span></span> <span data-ttu-id="00089-136">Bei *IndizesTensor.Sizes*  =  `{1,3,4,5,6,7}` und *IndizesDimensionCount* = 5 und = 2 gibt es beispielsweise `BatchDimensionCount` Batches und aussagekräftige `{3,4}` `{5,6,7}` Indizes.</span><span class="sxs-lookup"><span data-stu-id="00089-136">For example, given *IndicesTensor.Sizes* = `{1,3,4,5,6,7}`, and *IndicesDimensionCount* = 5 and `BatchDimensionCount` = 2, there are batches `{3,4}` and meaningful indices `{5,6,7}`.</span></span>

## <a name="remarks"></a><span data-ttu-id="00089-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00089-137">Remarks</span></span>
<span data-ttu-id="00089-138">**DML_GATHER_ND1_OPERATOR_DESC** fügt *BatchDimensionCount* hinzu und entspricht [DML_GATHER_ND_OPERATOR_DESC,](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) wenn *BatchDimensionCount* = 0 ist.</span><span class="sxs-lookup"><span data-stu-id="00089-138">**DML_GATHER_ND1_OPERATOR_DESC** adds *BatchDimensionCount*, and is equivalent to [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) when *BatchDimensionCount* = 0.</span></span>

## <a name="examples"></a><span data-ttu-id="00089-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00089-139">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="00089-140">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="00089-140">Example 1.</span></span> <span data-ttu-id="00089-141">1D-Neuzuordnung</span><span class="sxs-lookup"><span data-stu-id="00089-141">1D remapping</span></span>

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

### <a name="example-2-2d-remapping-with-batch-count"></a><span data-ttu-id="00089-142">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="00089-142">Example 2.</span></span> <span data-ttu-id="00089-143">2D-Neuzuordnung mit Batchanzahl</span><span class="sxs-lookup"><span data-stu-id="00089-143">2D remapping with batch count</span></span>

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

## <a name="availability"></a><span data-ttu-id="00089-144">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="00089-144">Availability</span></span>
<span data-ttu-id="00089-145">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="00089-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="00089-146">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="00089-146">Tensor constraints</span></span>
* <span data-ttu-id="00089-147">*IndicesTensor,* *InputTensor* und *OutputTensor* müssen über den gleichen *DimensionCount verfügen.*</span><span class="sxs-lookup"><span data-stu-id="00089-147">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="00089-148">*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="00089-148">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="00089-149">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="00089-149">Tensor support</span></span>
| <span data-ttu-id="00089-150">Tensor</span><span class="sxs-lookup"><span data-stu-id="00089-150">Tensor</span></span> | <span data-ttu-id="00089-151">Typ</span><span class="sxs-lookup"><span data-stu-id="00089-151">Kind</span></span> | <span data-ttu-id="00089-152">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="00089-152">Supported dimension counts</span></span> | <span data-ttu-id="00089-153">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="00089-153">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="00089-154">InputTensor</span><span class="sxs-lookup"><span data-stu-id="00089-154">InputTensor</span></span> | <span data-ttu-id="00089-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00089-155">Input</span></span> | <span data-ttu-id="00089-156">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="00089-156">1 to 8</span></span> | <span data-ttu-id="00089-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="00089-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="00089-158">IndizesTensor</span><span class="sxs-lookup"><span data-stu-id="00089-158">IndicesTensor</span></span> | <span data-ttu-id="00089-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00089-159">Input</span></span> | <span data-ttu-id="00089-160">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="00089-160">1 to 8</span></span> | <span data-ttu-id="00089-161">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="00089-161">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="00089-162">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="00089-162">OutputTensor</span></span> | <span data-ttu-id="00089-163">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="00089-163">Output</span></span> | <span data-ttu-id="00089-164">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="00089-164">1 to 8</span></span> | <span data-ttu-id="00089-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="00089-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="00089-166">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="00089-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="00089-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="00089-167">**Header**</span></span> | <span data-ttu-id="00089-168">directml.h</span><span class="sxs-lookup"><span data-stu-id="00089-168">directml.h</span></span> |
