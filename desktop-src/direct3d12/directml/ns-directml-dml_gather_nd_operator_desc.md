---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Erfasst Elemente aus dem Eingabetensor und verwendet dabei den Indizestensor, um Indizes vollständigen Teilblöcken der Eingabe neu zuordnen. | DML_GATHER_ND_OPERATOR_DESC
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
ms.openlocfilehash: 8e74078eaf55f209fba92ba97737d22047a5e67c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802894"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="5fc64-104">DML_GATHER_ND_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="5fc64-104">DML_GATHER_ND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5fc64-105">Erfasst Elemente aus dem Eingabetensor und verwendet den Indizestensor, um Indizes vollständigen Teilblöcken der Eingabe neu zuordnen.</span><span class="sxs-lookup"><span data-stu-id="5fc64-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="5fc64-106">Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten dar, deren genaues Verhalten von der Anzahl der Eingabe- und Indizesdimensionen abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="5fc64-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the input and indices dimension count.</span></span>

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> <span data-ttu-id="5fc64-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="5fc64-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5fc64-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="5fc64-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc64-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fc64-109">Syntax</span></span>
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="5fc64-110">Member</span><span class="sxs-lookup"><span data-stu-id="5fc64-110">Members</span></span>

`InputTensor`

<span data-ttu-id="5fc64-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5fc64-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5fc64-112">Der Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fc64-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="5fc64-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5fc64-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5fc64-114">Der Tensor, der die Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="5fc64-114">The tensor containing the indices.</span></span> <span data-ttu-id="5fc64-115">DimensionCount *dieses* Tensors muss mit *InputTensor.DimensionCount übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="5fc64-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="5fc64-116">Die letzte Dimension des *IndicesTensor* ist tatsächlich die Anzahl der Koordinaten pro Index-Tupel und darf *InputTensor.DimensionCount nicht überschreiten.*</span><span class="sxs-lookup"><span data-stu-id="5fc64-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="5fc64-117">Beispielsweise bedeutet ein Indizes-Tensor von *Größen* mit `{1,4,5,2}` *IndicesDimensionCount* = 3 ein 4x5-Array von 2-Koordinaten-Tupeln, die in *InputTensor* indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="5fc64-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="5fc64-118">Ab unterstützt dieser Operator negative Indexwerte, wenn ein integraler Typ mit `DML_FEATURE_LEVEL_3_0` Vorsignierung mit diesem Tensor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5fc64-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="5fc64-119">Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert.</span><span class="sxs-lookup"><span data-stu-id="5fc64-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="5fc64-120">Beispielsweise bezieht sich ein Index von -1 auf das letzte Element in dieser Dimension.</span><span class="sxs-lookup"><span data-stu-id="5fc64-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="5fc64-121">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5fc64-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5fc64-122">Der Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5fc64-122">The tensor to write the results to.</span></span> <span data-ttu-id="5fc64-123">*DimensionCount und* *DataType dieses* Tensors müssen mit *InputTensor.DimensionCount übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="5fc64-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="5fc64-124">Die *erwarteten OutputTensor.Sizes* sind die Verkettung der führenden *Segmente "IndicesTensor.Sizes"* und des nachgestellten Segments *"InputTensor.Sizes":*</span><span class="sxs-lookup"><span data-stu-id="5fc64-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield:</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="5fc64-125">Die Ausgabedimensionen sind rechtsbündig ausgerichtet, wobei bei Bedarf führende 1 Werte voranstehen, um bis zu *OutputTensor.DimensionCount* zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="5fc64-125">The output dimensions are right-aligned, with leading 1 values prepended if needed to satisfy up to *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="5fc64-126">Hier sehen Sie ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="5fc64-126">Here's an example.</span></span>

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

<span data-ttu-id="5fc64-127">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5fc64-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5fc64-128">Die Anzahl der tatsächlichen Eingabedimensionen innerhalb des *InputTensor,* nachdem irrelevante führende Dimensionen ignoriert wurden, die im Bereich von `[1, *InputTensor.DimensionCount*]` sind.</span><span class="sxs-lookup"><span data-stu-id="5fc64-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="5fc64-129">Wenn beispielsweise *InputTensor.Sizes* und = 3 angegeben  =  `{1,1,4,6}` `InputDimensionCount` sind, sind die tatsächlichen aussagekräftigen Indizes `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="5fc64-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="5fc64-130">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5fc64-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5fc64-131">Die Anzahl der tatsächlichen Indexdimensionen innerhalb des *Indextensors* nach dem Ignorieren irrelevanter führender Dimensionen im Bereich [1, *IndizesTensor.DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="5fc64-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="5fc64-132">Bei *IndizesTensor.Sizes*  =  `{1,1,4,6}` und *IndizesDimensionCount* = 3 sind die tatsächlichen aussagekräftigen Indizes beispielsweise `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="5fc64-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

## <a name="examples"></a><span data-ttu-id="5fc64-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5fc64-133">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="5fc64-134">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="5fc64-134">Example 1.</span></span> <span data-ttu-id="5fc64-135">1D-Neuzuordnung</span><span class="sxs-lookup"><span data-stu-id="5fc64-135">1D remapping</span></span>

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

### <a name="example-2-2d-remapping"></a><span data-ttu-id="5fc64-136">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="5fc64-136">Example 2.</span></span> <span data-ttu-id="5fc64-137">2D-Neuzuordnung</span><span class="sxs-lookup"><span data-stu-id="5fc64-137">2D remapping</span></span>

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


## <a name="remarks"></a><span data-ttu-id="5fc64-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5fc64-138">Remarks</span></span>
<span data-ttu-id="5fc64-139">Eine neuere Version dieses Operators, `DML_OPERATOR_GATHER_ND1` , wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5fc64-139">A newer version of this operator, `DML_OPERATOR_GATHER_ND1`, was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="availability"></a><span data-ttu-id="5fc64-140">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="5fc64-140">Availability</span></span>
<span data-ttu-id="5fc64-141">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5fc64-141">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5fc64-142">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="5fc64-142">Tensor constraints</span></span>
* <span data-ttu-id="5fc64-143">*IndicesTensor,* *InputTensor* und *OutputTensor* müssen über den gleichen *DimensionCount verfügen.*</span><span class="sxs-lookup"><span data-stu-id="5fc64-143">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="5fc64-144">*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="5fc64-144">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5fc64-145">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="5fc64-145">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="5fc64-146">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="5fc64-146">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="5fc64-147">Tensor</span><span class="sxs-lookup"><span data-stu-id="5fc64-147">Tensor</span></span> | <span data-ttu-id="5fc64-148">Typ</span><span class="sxs-lookup"><span data-stu-id="5fc64-148">Kind</span></span> | <span data-ttu-id="5fc64-149">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="5fc64-149">Supported dimension counts</span></span> | <span data-ttu-id="5fc64-150">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="5fc64-150">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5fc64-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5fc64-151">InputTensor</span></span> | <span data-ttu-id="5fc64-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fc64-152">Input</span></span> | <span data-ttu-id="5fc64-153">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="5fc64-153">1 to 8</span></span> | <span data-ttu-id="5fc64-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5fc64-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5fc64-155">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="5fc64-155">IndicesTensor</span></span> | <span data-ttu-id="5fc64-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fc64-156">Input</span></span> | <span data-ttu-id="5fc64-157">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="5fc64-157">1 to 8</span></span> | <span data-ttu-id="5fc64-158">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="5fc64-158">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="5fc64-159">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5fc64-159">OutputTensor</span></span> | <span data-ttu-id="5fc64-160">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5fc64-160">Output</span></span> | <span data-ttu-id="5fc64-161">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="5fc64-161">1 to 8</span></span> | <span data-ttu-id="5fc64-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5fc64-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="5fc64-163">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="5fc64-163">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="5fc64-164">Tensor</span><span class="sxs-lookup"><span data-stu-id="5fc64-164">Tensor</span></span> | <span data-ttu-id="5fc64-165">Typ</span><span class="sxs-lookup"><span data-stu-id="5fc64-165">Kind</span></span> | <span data-ttu-id="5fc64-166">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="5fc64-166">Supported dimension counts</span></span> | <span data-ttu-id="5fc64-167">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="5fc64-167">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5fc64-168">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5fc64-168">InputTensor</span></span> | <span data-ttu-id="5fc64-169">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fc64-169">Input</span></span> | <span data-ttu-id="5fc64-170">4</span><span class="sxs-lookup"><span data-stu-id="5fc64-170">4</span></span> | <span data-ttu-id="5fc64-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5fc64-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5fc64-172">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="5fc64-172">IndicesTensor</span></span> | <span data-ttu-id="5fc64-173">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fc64-173">Input</span></span> | <span data-ttu-id="5fc64-174">4</span><span class="sxs-lookup"><span data-stu-id="5fc64-174">4</span></span> | <span data-ttu-id="5fc64-175">UINT32</span><span class="sxs-lookup"><span data-stu-id="5fc64-175">UINT32</span></span> |
| <span data-ttu-id="5fc64-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5fc64-176">OutputTensor</span></span> | <span data-ttu-id="5fc64-177">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5fc64-177">Output</span></span> | <span data-ttu-id="5fc64-178">4</span><span class="sxs-lookup"><span data-stu-id="5fc64-178">4</span></span> | <span data-ttu-id="5fc64-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5fc64-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="5fc64-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fc64-180">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5fc64-181">**Header**</span><span class="sxs-lookup"><span data-stu-id="5fc64-181">**Header**</span></span> | <span data-ttu-id="5fc64-182">directml.h</span><span class="sxs-lookup"><span data-stu-id="5fc64-182">directml.h</span></span> |
