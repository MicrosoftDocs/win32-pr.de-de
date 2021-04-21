---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Kopiert den gesamten Eingabe-Tensor in die Ausgabe und überschreibt dann ausgewählte Indizes mit entsprechenden Werten aus dem Aktualisierungs-Tensor.
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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803977"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="75566-103">DML_SCATTER_ND_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="75566-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="75566-104">Kopiert den gesamten Eingabe-Tensor in die Ausgabe und überschreibt dann ausgewählte Indizes mit entsprechenden Werten aus dem Aktualisierungs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="75566-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="75566-105">Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten dar, wobei das genaue Verhalten durch die Achsen- und Indexgröße bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="75566-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="75566-106">Wenn sich zwei Ausgabeelementindizes überlappen (was ungültig ist), gibt es keine Garantie dafür, welcher letzte Schreibvorgang gewinnt.</span><span class="sxs-lookup"><span data-stu-id="75566-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75566-107">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="75566-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="75566-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="75566-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="75566-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="75566-109">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="75566-110">Member</span><span class="sxs-lookup"><span data-stu-id="75566-110">Members</span></span>

`InputTensor`

<span data-ttu-id="75566-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="75566-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="75566-112">Der Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="75566-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="75566-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="75566-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="75566-114">Ein Tensor, der die Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="75566-114">A tensor containing the indices.</span></span> <span data-ttu-id="75566-115">*DimensionCount* dieses Tensors muss mit *InputTensor.DimensionCount* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="75566-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="75566-116">Die letzte Dimension des *Indextensors* ist tatsächlich die Anzahl der Koordinaten pro Indextupel und darf *inputTensor.DimensionCount* nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="75566-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="75566-117">Ein Index-Tensor der Größe `{1,4,5,2}` mit *IndizesDimensionCount* = 3 bedeutet beispielsweise ein 4x5-Array von 2-Wert-Koordinatentupeln, die in *InputTensor* indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="75566-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="75566-118">Ab `DML_FEATURE_LEVEL_3_0` unterstützt dieser Operator negative Indexwerte, wenn ein ganzzahligen Typ mit Vorzeichen mit diesem Tensor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="75566-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="75566-119">Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert.</span><span class="sxs-lookup"><span data-stu-id="75566-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="75566-120">Beispielsweise bezieht sich ein Index von -1 auf das letzte Element entlang dieser Dimension.</span><span class="sxs-lookup"><span data-stu-id="75566-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="75566-121">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="75566-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="75566-122">Ein Tensor, der die neuen Werte enthält, um die vorhandenen Eingabewerte an den entsprechenden Indizes zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="75566-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="75566-123">DimensionCount *dieses* Tensors muss mit *InputTensor.DimensionCount übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="75566-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="75566-124">Die erwarteten *UpdatesTensor.Sizes* sind die Verkettung der führenden Segmente *IndicesTensor.Sizes* und *InputTensor.Sizes,* um Folgendes zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="75566-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="75566-125">Die Dimensionen sind rechtsbündig ausgerichtet, und führenden 1 Werten wird bei Bedarf vorgefertigt, um *UpdatesTensor.DimensionCount zu erfüllen.*</span><span class="sxs-lookup"><span data-stu-id="75566-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="75566-126">Hier sehen Sie ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="75566-126">Here's an example.</span></span>

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

<span data-ttu-id="75566-127">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="75566-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="75566-128">Der Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="75566-128">The tensor to write the results to.</span></span> <span data-ttu-id="75566-129">Die *Größen und* der Datentyp *dieses* Tensors müssen mit *InputTensor.Sizes übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="75566-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="75566-130">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="75566-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="75566-131">Die Anzahl der tatsächlichen Eingabedimensionen innerhalb des *InputTensor,* nachdem alle irrelevanten führenden Dimensionen ignoriert wurden, die [1, *InputTensor.DimensionCount*) reichen.</span><span class="sxs-lookup"><span data-stu-id="75566-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="75566-132">Wenn beispielsweise *InputTensor.Sizes* = {1,1,4,6} und *InputDimensionCount* = 3 angegeben sind, sind die tatsächlichen sinnvollen Indizes {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="75566-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="75566-133">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="75566-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="75566-134">Die Anzahl der tatsächlichen Indexdimensionen innerhalb des *IndizesTensors,* nachdem alle irrelevanten führenden Dimensionen im Bereich [1, *IndicesTensor.DimensionCount ) ignoriert wurden.*</span><span class="sxs-lookup"><span data-stu-id="75566-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="75566-135">Wenn beispielsweise *IndicesTensor.Sizes* = {1,1,4,6} und *IndicesDimensionCount* = 3 angegeben sind, sind die tatsächlichen sinnvollen Indizes {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="75566-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="75566-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75566-136">Examples</span></span>

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

## <a name="availability"></a><span data-ttu-id="75566-137">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="75566-137">Availability</span></span>
<span data-ttu-id="75566-138">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="75566-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="75566-139">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="75566-139">Tensor constraints</span></span>
* <span data-ttu-id="75566-140">*IndicesTensor,* *InputTensor,* *OutputTensor* und müssen `UpdatesTensor` denselben *DimensionCount aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="75566-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="75566-141">*InputTensor*, *OutputTensor* und `UpdatesTensor` müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="75566-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="75566-142">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="75566-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="75566-143">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="75566-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="75566-144">Tensor</span><span class="sxs-lookup"><span data-stu-id="75566-144">Tensor</span></span> | <span data-ttu-id="75566-145">Typ</span><span class="sxs-lookup"><span data-stu-id="75566-145">Kind</span></span> | <span data-ttu-id="75566-146">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="75566-146">Supported dimension counts</span></span> | <span data-ttu-id="75566-147">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="75566-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="75566-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="75566-148">InputTensor</span></span> | <span data-ttu-id="75566-149">Eingabe</span><span class="sxs-lookup"><span data-stu-id="75566-149">Input</span></span> | <span data-ttu-id="75566-150">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="75566-150">1 to 8</span></span> | <span data-ttu-id="75566-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="75566-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="75566-152">IndizesTensor</span><span class="sxs-lookup"><span data-stu-id="75566-152">IndicesTensor</span></span> | <span data-ttu-id="75566-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="75566-153">Input</span></span> | <span data-ttu-id="75566-154">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="75566-154">1 to 8</span></span> | <span data-ttu-id="75566-155">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="75566-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="75566-156">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="75566-156">UpdatesTensor</span></span> | <span data-ttu-id="75566-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="75566-157">Input</span></span> | <span data-ttu-id="75566-158">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="75566-158">1 to 8</span></span> | <span data-ttu-id="75566-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="75566-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="75566-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="75566-160">OutputTensor</span></span> | <span data-ttu-id="75566-161">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="75566-161">Output</span></span> | <span data-ttu-id="75566-162">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="75566-162">1 to 8</span></span> | <span data-ttu-id="75566-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="75566-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="75566-164">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="75566-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="75566-165">Tensor</span><span class="sxs-lookup"><span data-stu-id="75566-165">Tensor</span></span> | <span data-ttu-id="75566-166">Typ</span><span class="sxs-lookup"><span data-stu-id="75566-166">Kind</span></span> | <span data-ttu-id="75566-167">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="75566-167">Supported dimension counts</span></span> | <span data-ttu-id="75566-168">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="75566-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="75566-169">InputTensor</span><span class="sxs-lookup"><span data-stu-id="75566-169">InputTensor</span></span> | <span data-ttu-id="75566-170">Eingabe</span><span class="sxs-lookup"><span data-stu-id="75566-170">Input</span></span> | <span data-ttu-id="75566-171">4</span><span class="sxs-lookup"><span data-stu-id="75566-171">4</span></span> | <span data-ttu-id="75566-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="75566-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="75566-173">IndizesTensor</span><span class="sxs-lookup"><span data-stu-id="75566-173">IndicesTensor</span></span> | <span data-ttu-id="75566-174">Eingabe</span><span class="sxs-lookup"><span data-stu-id="75566-174">Input</span></span> | <span data-ttu-id="75566-175">4</span><span class="sxs-lookup"><span data-stu-id="75566-175">4</span></span> | <span data-ttu-id="75566-176">UINT32</span><span class="sxs-lookup"><span data-stu-id="75566-176">UINT32</span></span> |
| <span data-ttu-id="75566-177">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="75566-177">UpdatesTensor</span></span> | <span data-ttu-id="75566-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="75566-178">Input</span></span> | <span data-ttu-id="75566-179">4</span><span class="sxs-lookup"><span data-stu-id="75566-179">4</span></span> | <span data-ttu-id="75566-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="75566-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="75566-181">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="75566-181">OutputTensor</span></span> | <span data-ttu-id="75566-182">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="75566-182">Output</span></span> | <span data-ttu-id="75566-183">4</span><span class="sxs-lookup"><span data-stu-id="75566-183">4</span></span> | <span data-ttu-id="75566-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="75566-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="75566-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75566-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="75566-186">**Header**</span><span class="sxs-lookup"><span data-stu-id="75566-186">**Header**</span></span> | <span data-ttu-id="75566-187">directml.h</span><span class="sxs-lookup"><span data-stu-id="75566-187">directml.h</span></span> |