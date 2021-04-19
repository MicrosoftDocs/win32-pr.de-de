---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Kopiert den gesamten Eingabe Mandanten in die Ausgabe und überschreibt dann ausgewählte Indizes mit entsprechenden Werten aus dem Aktualisierungs Mandanten.
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
ms.openlocfilehash: ae9a3022a7070bbf0253e71550f2ca1ceced6768
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351831"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="b9386-103">DML_SCATTER_ND_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b9386-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="b9386-104">Kopiert den gesamten Eingabe Mandanten in die Ausgabe und überschreibt dann ausgewählte Indizes mit entsprechenden Werten aus dem Aktualisierungs Mandanten.</span><span class="sxs-lookup"><span data-stu-id="b9386-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="b9386-105">Dieser Operator führt den folgenden Pseudocode aus, wobei "..." stellt eine Reihe von Koordinaten mit dem exakten Verhalten dar, das durch die Größe der Achse und der Indizes bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="b9386-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="b9386-106">Wenn sich zwei Ausgabe Element Indizes überlappen (was ungültig ist), gibt es keine Garantie dafür, welcher letzte Schreibvorgang gewinnt.</span><span class="sxs-lookup"><span data-stu-id="b9386-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9386-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="b9386-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="b9386-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b9386-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9386-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9386-109">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="b9386-110">Member</span><span class="sxs-lookup"><span data-stu-id="b9386-110">Members</span></span>

`InputTensor`

<span data-ttu-id="b9386-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b9386-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b9386-112">Der zu lesende tensorflow.</span><span class="sxs-lookup"><span data-stu-id="b9386-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="b9386-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b9386-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b9386-114">Ein tensorflow, der die Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="b9386-114">A tensor containing the indices.</span></span> <span data-ttu-id="b9386-115">Die *DimensionCount* dieses Mandanten muss mit " *inputtensor. DimensionCount*" verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="b9386-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="b9386-116">Die letzte Dimension von " *indicestensor* " ist tatsächlich die Anzahl der Koordinaten pro indextupel, die " *inputtensor. DimensionCount*" nicht überschreiten darf.</span><span class="sxs-lookup"><span data-stu-id="b9386-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="b9386-117">Beispielsweise `{1,4,5,2}` bedeutet ein indextensor der Größe mit *indicesdimensioncount* = 3 ein 4x5-Array von 2-Wert-Koordinaten Tupeln, die in *inputtensor* indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b9386-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="b9386-118">Ab `DML_FEATURE_LEVEL_3_0` unterstützt dieser Operator negative Indexwerte, wenn ein ganzzahliger Typ mit Vorzeichen mit diesem Mandanten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9386-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="b9386-119">Negative Indizes werden als relativ zum Ende der jeweiligen Dimension interpretiert.</span><span class="sxs-lookup"><span data-stu-id="b9386-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="b9386-120">Ein Index von-1 bezieht sich z. b. auf das letzte Element in dieser Dimension.</span><span class="sxs-lookup"><span data-stu-id="b9386-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="b9386-121">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b9386-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b9386-122">Ein tensorflow mit den neuen Werten, mit denen die vorhandenen Eingabewerte in den entsprechenden Indizes ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="b9386-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="b9386-123">Die *DimensionCount* dieses Mandanten muss mit " *inputtensor. DimensionCount*" verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="b9386-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="b9386-124">Die erwarteten *updatestensor. sizes* sind die Verkettung der führenden Segmente " *indicestensor. sizes* " und " *inputtensor. sizes* ", um Folgendes zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="b9386-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="b9386-125">Die Dimensionen sind rechtsbündig ausgerichtet, wobei bei Bedarf vorangehende 1-Werte vorangestellt werden, um *updatestensor. DimensionCount* zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="b9386-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="b9386-126">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="b9386-126">Here's an example.</span></span>

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

<span data-ttu-id="b9386-127">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b9386-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b9386-128">Der tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9386-128">The tensor to write the results to.</span></span> <span data-ttu-id="b9386-129">Die *Größen* und der *Datentyp* dieses Mandanten müssen mit " *inputtensor. sizes*" verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="b9386-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="b9386-130">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b9386-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b9386-131">Die Anzahl der tatsächlichen Eingabe Dimensionen innerhalb von *inputtensor* , nachdem alle irreführenden, führenden Werte mit [1, *inputtensor. DimensionCount*) ignoriert wurden.</span><span class="sxs-lookup"><span data-stu-id="b9386-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="b9386-132">Wenn z. b *. "inputtensor. sizes* =" {1,1,4,6} und " *inputdimensioncount* = 3" angegeben sind, sind die tatsächlichen aussagekräftigen Indizes {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="b9386-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="b9386-133">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b9386-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b9386-134">Die Anzahl der tatsächlichen Index Dimensionen innerhalb des *bezeichungsgebers* , nachdem alle irreführenden, führenden Werte mit [1, *indicestensor. DimensionCount*) ignoriert wurden.</span><span class="sxs-lookup"><span data-stu-id="b9386-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="b9386-135">Wenn beispielsweise " *indicestensor. sizes* =" {1,1,4,6} und " *indicesdimensioncount* = 3" angegeben sind, sind die tatsächlichen aussagekräftigen Indizes {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="b9386-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="b9386-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9386-136">Examples</span></span>

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

## <a name="availability"></a><span data-ttu-id="b9386-137">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="b9386-137">Availability</span></span>
<span data-ttu-id="b9386-138">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="b9386-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b9386-139">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="b9386-139">Tensor constraints</span></span>
* <span data-ttu-id="b9386-140">" *Indicestensor*", " *inputtensor*", " *outputtensor*" und "" `UpdatesTensor` müssen dieselbe *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b9386-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="b9386-141">" *Inputtensor*", " *outputtensor*" und "" `UpdatesTensor` müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b9386-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b9386-142">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="b9386-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="b9386-143">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="b9386-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="b9386-144">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="b9386-144">Tensor</span></span> | <span data-ttu-id="b9386-145">Typ</span><span class="sxs-lookup"><span data-stu-id="b9386-145">Kind</span></span> | <span data-ttu-id="b9386-146">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="b9386-146">Supported dimension counts</span></span> | <span data-ttu-id="b9386-147">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="b9386-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b9386-148">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="b9386-148">InputTensor</span></span> | <span data-ttu-id="b9386-149">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b9386-149">Input</span></span> | <span data-ttu-id="b9386-150">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="b9386-150">1 to 8</span></span> | <span data-ttu-id="b9386-151">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="b9386-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b9386-152">Indikator Geber</span><span class="sxs-lookup"><span data-stu-id="b9386-152">IndicesTensor</span></span> | <span data-ttu-id="b9386-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b9386-153">Input</span></span> | <span data-ttu-id="b9386-154">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="b9386-154">1 to 8</span></span> | <span data-ttu-id="b9386-155">Int64, Int32, UINT64, UInt32</span><span class="sxs-lookup"><span data-stu-id="b9386-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="b9386-156">Updatestensor</span><span class="sxs-lookup"><span data-stu-id="b9386-156">UpdatesTensor</span></span> | <span data-ttu-id="b9386-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b9386-157">Input</span></span> | <span data-ttu-id="b9386-158">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="b9386-158">1 to 8</span></span> | <span data-ttu-id="b9386-159">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="b9386-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b9386-160">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="b9386-160">OutputTensor</span></span> | <span data-ttu-id="b9386-161">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="b9386-161">Output</span></span> | <span data-ttu-id="b9386-162">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="b9386-162">1 to 8</span></span> | <span data-ttu-id="b9386-163">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="b9386-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="b9386-164">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="b9386-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="b9386-165">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="b9386-165">Tensor</span></span> | <span data-ttu-id="b9386-166">Typ</span><span class="sxs-lookup"><span data-stu-id="b9386-166">Kind</span></span> | <span data-ttu-id="b9386-167">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="b9386-167">Supported dimension counts</span></span> | <span data-ttu-id="b9386-168">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="b9386-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b9386-169">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="b9386-169">InputTensor</span></span> | <span data-ttu-id="b9386-170">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b9386-170">Input</span></span> | <span data-ttu-id="b9386-171">4</span><span class="sxs-lookup"><span data-stu-id="b9386-171">4</span></span> | <span data-ttu-id="b9386-172">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="b9386-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b9386-173">Indikator Geber</span><span class="sxs-lookup"><span data-stu-id="b9386-173">IndicesTensor</span></span> | <span data-ttu-id="b9386-174">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b9386-174">Input</span></span> | <span data-ttu-id="b9386-175">4</span><span class="sxs-lookup"><span data-stu-id="b9386-175">4</span></span> | <span data-ttu-id="b9386-176">UINT32</span><span class="sxs-lookup"><span data-stu-id="b9386-176">UINT32</span></span> |
| <span data-ttu-id="b9386-177">Updatestensor</span><span class="sxs-lookup"><span data-stu-id="b9386-177">UpdatesTensor</span></span> | <span data-ttu-id="b9386-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b9386-178">Input</span></span> | <span data-ttu-id="b9386-179">4</span><span class="sxs-lookup"><span data-stu-id="b9386-179">4</span></span> | <span data-ttu-id="b9386-180">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="b9386-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b9386-181">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="b9386-181">OutputTensor</span></span> | <span data-ttu-id="b9386-182">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="b9386-182">Output</span></span> | <span data-ttu-id="b9386-183">4</span><span class="sxs-lookup"><span data-stu-id="b9386-183">4</span></span> | <span data-ttu-id="b9386-184">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="b9386-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="b9386-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9386-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b9386-186">**Header**</span><span class="sxs-lookup"><span data-stu-id="b9386-186">**Header**</span></span> | <span data-ttu-id="b9386-187">directml. h</span><span class="sxs-lookup"><span data-stu-id="b9386-187">directml.h</span></span> |