---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Sammelt Elemente aus dem Eingabe Mandanten, wobei der Indexe-tensorflow verwendet wird, um Indizes den gesamten Teil Blöcken der Eingabe zuzuordnen. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 6a48fd19621bed100a13412dbb1992974d125323
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354333"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="77f9c-104">DML_GATHER_ND_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="77f9c-104">DML_GATHER_ND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="77f9c-105">Sammelt Elemente aus dem Eingabe Mandanten, wobei der Indexe-tensorflow verwendet wird, um Indizes den gesamten Teil Blöcken der Eingabe zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="77f9c-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="77f9c-106">Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten dar, wobei das genaue Verhalten von der Eingabe-und Index Dimensions Anzahl abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="77f9c-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the input and indices dimension count.</span></span>

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> <span data-ttu-id="77f9c-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="77f9c-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="77f9c-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="77f9c-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="77f9c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="77f9c-109">Syntax</span></span>
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="77f9c-110">Member</span><span class="sxs-lookup"><span data-stu-id="77f9c-110">Members</span></span>

`InputTensor`

<span data-ttu-id="77f9c-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="77f9c-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="77f9c-112">Der zu lesende tensorflow.</span><span class="sxs-lookup"><span data-stu-id="77f9c-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="77f9c-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="77f9c-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="77f9c-114">Der tensorflow, der die Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="77f9c-114">The tensor containing the indices.</span></span> <span data-ttu-id="77f9c-115">Die *DimensionCount* dieses Mandanten muss mit " *inputtensor. DimensionCount*" verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="77f9c-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="77f9c-116">Die letzte Dimension von " *indicestensor* " ist tatsächlich die Anzahl der Koordinaten pro indextupel, die " *inputtensor. DimensionCount*" nicht überschreiten darf.</span><span class="sxs-lookup"><span data-stu-id="77f9c-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="77f9c-117">Ein indexertensor der *Größen* `{1,4,5,2}` mit *indicesdimensioncount* = 3 bedeutet beispielsweise ein 4x5-Array von 2-Koordinaten-Tupeln, die in *inputtensor* indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="77f9c-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="77f9c-118">Ab `DML_FEATURE_LEVEL_3_0` unterstützt dieser Operator negative Indexwerte, wenn ein ganzzahliger Typ mit Vorzeichen mit diesem Mandanten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="77f9c-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="77f9c-119">Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert.</span><span class="sxs-lookup"><span data-stu-id="77f9c-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="77f9c-120">Ein Index von-1 bezieht sich z. b. auf das letzte Element in dieser Dimension.</span><span class="sxs-lookup"><span data-stu-id="77f9c-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="77f9c-121">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="77f9c-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="77f9c-122">Der tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="77f9c-122">The tensor to write the results to.</span></span> <span data-ttu-id="77f9c-123">Die *DimensionCount* -und *DataType* -Elemente dieses Mandanten müssen mit " *inputtensor. DimensionCount*" verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="77f9c-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="77f9c-124">Der erwartete *outputtensor. sizes* -Parameter ist die Verkettung der " *indicestensor. sizes* "-Segmente und " *inputtensor. sizes* ", die das nachfolgende Segment ergibt:</span><span class="sxs-lookup"><span data-stu-id="77f9c-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield:</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="77f9c-125">Die Ausgabe Dimensionen werden rechtsbündig ausgerichtet, wobei bei Bedarf vorangehende 1-Werte vorangestellt werden, um bis zu *outputtensor. DimensionCount* zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="77f9c-125">The output dimensions are right-aligned, with leading 1 values prepended if needed to satisfy up to *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="77f9c-126">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="77f9c-126">Here's an example.</span></span>

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

<span data-ttu-id="77f9c-127">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="77f9c-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="77f9c-128">Die Anzahl der tatsächlichen Eingabe Dimensionen innerhalb von *inputtensor* , nachdem alle irreführenden, führenden Werte ignoriert wurden `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="77f9c-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="77f9c-129">Wenn beispielsweise " *inputtensor. sizes* " und "= 3" angegeben sind  =  `{1,1,4,6}` `InputDimensionCount` , sind die tatsächlichen aussagekräftigen Indizes `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="77f9c-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="77f9c-130">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="77f9c-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="77f9c-131">Die Anzahl der tatsächlichen Index Dimensionen innerhalb von " *indicestensor* ", nachdem alle nicht relevanten führenden Werte im Bereich von [1, " *indicestensor. DimensionCount*") ignoriert wurden.</span><span class="sxs-lookup"><span data-stu-id="77f9c-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="77f9c-132">Wenn beispielsweise " *indicestensor. sizes*"  =  `{1,1,4,6}` und " *indicesdimensioncount* = 3" angegeben sind, sind die tatsächlichen aussagekräftigen Indizes `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="77f9c-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

## <a name="examples"></a><span data-ttu-id="77f9c-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77f9c-133">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="77f9c-134">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="77f9c-134">Example 1.</span></span> <span data-ttu-id="77f9c-135">Neuzuordnung von 1 d</span><span class="sxs-lookup"><span data-stu-id="77f9c-135">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a><span data-ttu-id="77f9c-136">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="77f9c-136">Example 2.</span></span> <span data-ttu-id="77f9c-137">2D-Neuzuordnung</span><span class="sxs-lookup"><span data-stu-id="77f9c-137">2D remapping</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a><span data-ttu-id="77f9c-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77f9c-138">Remarks</span></span>
<span data-ttu-id="77f9c-139">Eine neuere Version dieses Operators, `DML_OPERATOR_GATHER_ND1` , wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="77f9c-139">A newer version of this operator, `DML_OPERATOR_GATHER_ND1`, was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="availability"></a><span data-ttu-id="77f9c-140">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="77f9c-140">Availability</span></span>
<span data-ttu-id="77f9c-141">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="77f9c-141">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="77f9c-142">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="77f9c-142">Tensor constraints</span></span>
* <span data-ttu-id="77f9c-143">" *Indicestensor*", " *inputtensor*" und " *outputtensor* " müssen dieselbe *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="77f9c-143">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="77f9c-144">*Inputtensor* und *outputtensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="77f9c-144">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="77f9c-145">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="77f9c-145">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="77f9c-146">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="77f9c-146">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="77f9c-147">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="77f9c-147">Tensor</span></span> | <span data-ttu-id="77f9c-148">Typ</span><span class="sxs-lookup"><span data-stu-id="77f9c-148">Kind</span></span> | <span data-ttu-id="77f9c-149">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="77f9c-149">Supported dimension counts</span></span> | <span data-ttu-id="77f9c-150">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="77f9c-150">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="77f9c-151">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="77f9c-151">InputTensor</span></span> | <span data-ttu-id="77f9c-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77f9c-152">Input</span></span> | <span data-ttu-id="77f9c-153">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="77f9c-153">1 to 8</span></span> | <span data-ttu-id="77f9c-154">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="77f9c-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="77f9c-155">Indikator Geber</span><span class="sxs-lookup"><span data-stu-id="77f9c-155">IndicesTensor</span></span> | <span data-ttu-id="77f9c-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77f9c-156">Input</span></span> | <span data-ttu-id="77f9c-157">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="77f9c-157">1 to 8</span></span> | <span data-ttu-id="77f9c-158">Int64, Int32, UINT64, UInt32</span><span class="sxs-lookup"><span data-stu-id="77f9c-158">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="77f9c-159">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="77f9c-159">OutputTensor</span></span> | <span data-ttu-id="77f9c-160">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="77f9c-160">Output</span></span> | <span data-ttu-id="77f9c-161">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="77f9c-161">1 to 8</span></span> | <span data-ttu-id="77f9c-162">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="77f9c-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="77f9c-163">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="77f9c-163">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="77f9c-164">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="77f9c-164">Tensor</span></span> | <span data-ttu-id="77f9c-165">Typ</span><span class="sxs-lookup"><span data-stu-id="77f9c-165">Kind</span></span> | <span data-ttu-id="77f9c-166">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="77f9c-166">Supported dimension counts</span></span> | <span data-ttu-id="77f9c-167">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="77f9c-167">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="77f9c-168">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="77f9c-168">InputTensor</span></span> | <span data-ttu-id="77f9c-169">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77f9c-169">Input</span></span> | <span data-ttu-id="77f9c-170">4</span><span class="sxs-lookup"><span data-stu-id="77f9c-170">4</span></span> | <span data-ttu-id="77f9c-171">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="77f9c-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="77f9c-172">Indikator Geber</span><span class="sxs-lookup"><span data-stu-id="77f9c-172">IndicesTensor</span></span> | <span data-ttu-id="77f9c-173">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77f9c-173">Input</span></span> | <span data-ttu-id="77f9c-174">4</span><span class="sxs-lookup"><span data-stu-id="77f9c-174">4</span></span> | <span data-ttu-id="77f9c-175">UINT32</span><span class="sxs-lookup"><span data-stu-id="77f9c-175">UINT32</span></span> |
| <span data-ttu-id="77f9c-176">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="77f9c-176">OutputTensor</span></span> | <span data-ttu-id="77f9c-177">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="77f9c-177">Output</span></span> | <span data-ttu-id="77f9c-178">4</span><span class="sxs-lookup"><span data-stu-id="77f9c-178">4</span></span> | <span data-ttu-id="77f9c-179">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="77f9c-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="77f9c-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77f9c-180">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="77f9c-181">**Header**</span><span class="sxs-lookup"><span data-stu-id="77f9c-181">**Header**</span></span> | <span data-ttu-id="77f9c-182">directml. h</span><span class="sxs-lookup"><span data-stu-id="77f9c-182">directml.h</span></span> |
