---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Kopiert den gesamten Eingabe tensor in die Ausgabe und überschreibt dann ausgewählte Indizes mit entsprechenden Werten aus dem Aktualisierungs tensor.
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: 6c987e01862d849c6215a2d25fe957ef0a22e7af
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417714"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="bd60b-103">DML_SCATTER_ND_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="bd60b-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="bd60b-104">Kopiert den gesamten Eingabe tensor in die Ausgabe und überschreibt dann ausgewählte Indizes mit entsprechenden Werten aus dem Aktualisierungs tensor.</span><span class="sxs-lookup"><span data-stu-id="bd60b-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="bd60b-105">Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten dar, mit dem genauen Verhalten, das durch die Achsen- und Indexgröße bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="bd60b-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="bd60b-106">Wenn sich zwei Ausgabeelementindizes überlappen (ungültig), gibt es keine Garantie dafür, welcher letzte Schreibzugriff gewinnt.</span><span class="sxs-lookup"><span data-stu-id="bd60b-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd60b-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="bd60b-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="bd60b-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="bd60b-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd60b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd60b-109">Syntax</span></span>
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="bd60b-110">Member</span><span class="sxs-lookup"><span data-stu-id="bd60b-110">Members</span></span>

`InputTensor`

<span data-ttu-id="bd60b-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bd60b-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bd60b-112">Der Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd60b-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="bd60b-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bd60b-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bd60b-114">Ein Tensor, der die Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="bd60b-114">A tensor containing the indices.</span></span> <span data-ttu-id="bd60b-115">DimensionCount *dieses* Tensors muss mit *InputTensor.DimensionCount übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="bd60b-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="bd60b-116">Die letzte Dimension des *IndicesTensor* ist tatsächlich die Anzahl der Koordinaten pro Index-Tupel und darf *InputTensor.DimensionCount nicht überschreiten.*</span><span class="sxs-lookup"><span data-stu-id="bd60b-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="bd60b-117">Beispielsweise bedeutet ein Indizestensor der Größe mit `{1,4,5,2}` *IndicesDimensionCount* = 3 ein 4x5-Array von Zwei-Wert-Koordinatentpeln, die in *InputTensor* indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="bd60b-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="bd60b-118">Ab unterstützt dieser Operator negative Indexwerte, wenn ein integraler Typ mit `DML_FEATURE_LEVEL_3_0` Vorsignierung mit diesem Tensor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bd60b-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="bd60b-119">Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert.</span><span class="sxs-lookup"><span data-stu-id="bd60b-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="bd60b-120">Ein Index von -1 bezieht sich beispielsweise auf das letzte Element in dieser Dimension.</span><span class="sxs-lookup"><span data-stu-id="bd60b-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="bd60b-121">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bd60b-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bd60b-122">Ein Tensor, der die neuen Werte enthält, um die vorhandenen Eingabewerte an den entsprechenden Indizes zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="bd60b-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="bd60b-123">DimensionCount *dieses* Tensors muss mit *InputTensor.DimensionCount übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="bd60b-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="bd60b-124">Die erwarteten *UpdatesTensor.Sizes* sind die Verkettung der führenden Segmente *IndicesTensor.Sizes* und *InputTensor.Sizes,* um Folgendes zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="bd60b-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="bd60b-125">Die Dimensionen sind rechtsbündig ausgerichtet, und führenden 1 Werten wird bei Bedarf vorgefertigt, um *UpdatesTensor.DimensionCount zu erfüllen.*</span><span class="sxs-lookup"><span data-stu-id="bd60b-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="bd60b-126">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="bd60b-126">Here's an example.</span></span>

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

<span data-ttu-id="bd60b-127">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bd60b-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bd60b-128">Der Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bd60b-128">The tensor to write the results to.</span></span> <span data-ttu-id="bd60b-129">Die *Größen und* der Datentyp *dieses* Tensors müssen mit *InputTensor.Sizes übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="bd60b-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="bd60b-130">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bd60b-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="bd60b-131">Die Anzahl der tatsächlichen Eingabedimensionen innerhalb des *InputTensor,* nachdem alle irrelevanten führenden Dimensionen im Bereich [1, *InputTensor.DimensionCount ) ignoriert wurden.*</span><span class="sxs-lookup"><span data-stu-id="bd60b-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="bd60b-132">Wenn beispielsweise *InputTensor.Sizes* = {1,1,4,6} und *InputDimensionCount* = 3 angegeben sind, sind die tatsächlichen sinnvollen Indizes {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="bd60b-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="bd60b-133">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bd60b-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="bd60b-134">Die Anzahl der tatsächlichen Indexdimensionen innerhalb des *IndizesTensors,* nachdem alle irrelevanten führenden Dimensionen im Bereich [1, *IndicesTensor.DimensionCount ) ignoriert wurden.*</span><span class="sxs-lookup"><span data-stu-id="bd60b-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="bd60b-135">Wenn beispielsweise *IndicesTensor.Sizes* = {1,1,4,6} und *IndicesDimensionCount* = 3 angegeben sind, sind die tatsächlichen sinnvollen Indizes {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="bd60b-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="bd60b-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd60b-136">Examples</span></span>

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a><span data-ttu-id="bd60b-137">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="bd60b-137">Availability</span></span>
<span data-ttu-id="bd60b-138">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bd60b-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="bd60b-139">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="bd60b-139">Tensor constraints</span></span>
* <span data-ttu-id="bd60b-140">*IndicesTensor,* *InputTensor,* *OutputTensor* und müssen `UpdatesTensor` denselben *DimensionCount aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="bd60b-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="bd60b-141">*InputTensor*, *OutputTensor* und `UpdatesTensor` müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="bd60b-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="bd60b-142">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="bd60b-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="bd60b-143">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="bd60b-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="bd60b-144">Tensor</span><span class="sxs-lookup"><span data-stu-id="bd60b-144">Tensor</span></span> | <span data-ttu-id="bd60b-145">Typ</span><span class="sxs-lookup"><span data-stu-id="bd60b-145">Kind</span></span> | <span data-ttu-id="bd60b-146">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="bd60b-146">Supported dimension counts</span></span> | <span data-ttu-id="bd60b-147">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="bd60b-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bd60b-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="bd60b-148">InputTensor</span></span> | <span data-ttu-id="bd60b-149">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bd60b-149">Input</span></span> | <span data-ttu-id="bd60b-150">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="bd60b-150">1 to 8</span></span> | <span data-ttu-id="bd60b-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bd60b-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bd60b-152">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="bd60b-152">IndicesTensor</span></span> | <span data-ttu-id="bd60b-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bd60b-153">Input</span></span> | <span data-ttu-id="bd60b-154">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="bd60b-154">1 to 8</span></span> | <span data-ttu-id="bd60b-155">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="bd60b-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="bd60b-156">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="bd60b-156">UpdatesTensor</span></span> | <span data-ttu-id="bd60b-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bd60b-157">Input</span></span> | <span data-ttu-id="bd60b-158">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="bd60b-158">1 to 8</span></span> | <span data-ttu-id="bd60b-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bd60b-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bd60b-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="bd60b-160">OutputTensor</span></span> | <span data-ttu-id="bd60b-161">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="bd60b-161">Output</span></span> | <span data-ttu-id="bd60b-162">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="bd60b-162">1 to 8</span></span> | <span data-ttu-id="bd60b-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bd60b-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="bd60b-164">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="bd60b-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="bd60b-165">Tensor</span><span class="sxs-lookup"><span data-stu-id="bd60b-165">Tensor</span></span> | <span data-ttu-id="bd60b-166">Typ</span><span class="sxs-lookup"><span data-stu-id="bd60b-166">Kind</span></span> | <span data-ttu-id="bd60b-167">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="bd60b-167">Supported dimension counts</span></span> | <span data-ttu-id="bd60b-168">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="bd60b-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bd60b-169">InputTensor</span><span class="sxs-lookup"><span data-stu-id="bd60b-169">InputTensor</span></span> | <span data-ttu-id="bd60b-170">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bd60b-170">Input</span></span> | <span data-ttu-id="bd60b-171">4</span><span class="sxs-lookup"><span data-stu-id="bd60b-171">4</span></span> | <span data-ttu-id="bd60b-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bd60b-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bd60b-173">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="bd60b-173">IndicesTensor</span></span> | <span data-ttu-id="bd60b-174">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bd60b-174">Input</span></span> | <span data-ttu-id="bd60b-175">4</span><span class="sxs-lookup"><span data-stu-id="bd60b-175">4</span></span> | <span data-ttu-id="bd60b-176">UINT32</span><span class="sxs-lookup"><span data-stu-id="bd60b-176">UINT32</span></span> |
| <span data-ttu-id="bd60b-177">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="bd60b-177">UpdatesTensor</span></span> | <span data-ttu-id="bd60b-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bd60b-178">Input</span></span> | <span data-ttu-id="bd60b-179">4</span><span class="sxs-lookup"><span data-stu-id="bd60b-179">4</span></span> | <span data-ttu-id="bd60b-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bd60b-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bd60b-181">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="bd60b-181">OutputTensor</span></span> | <span data-ttu-id="bd60b-182">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="bd60b-182">Output</span></span> | <span data-ttu-id="bd60b-183">4</span><span class="sxs-lookup"><span data-stu-id="bd60b-183">4</span></span> | <span data-ttu-id="bd60b-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bd60b-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="bd60b-185">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bd60b-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bd60b-186">**Header**</span><span class="sxs-lookup"><span data-stu-id="bd60b-186">**Header**</span></span> | <span data-ttu-id="bd60b-187">directml.h</span><span class="sxs-lookup"><span data-stu-id="bd60b-187">directml.h</span></span> |