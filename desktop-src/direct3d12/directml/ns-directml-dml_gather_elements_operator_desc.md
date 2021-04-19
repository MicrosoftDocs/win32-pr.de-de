---
UID: NS:directml.DML_GATHER_ELEMENTS_OPERATOR_DESC
title: DML_GATHER_ELEMENTS_OPERATOR_DESC
description: Sammelt Elemente aus dem eingabetensor entlang der angegebenen Achse, wobei der Indexer-tensorflow verwendet wird, um die Eingabe neu zuzuordnen.
helpviewer_keywords:
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- DML_GATHER_ELEMENTS_OPERATOR_DESC structure
- direct3d12.dml_gather_elements_operator_desc
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.openlocfilehash: 19a3f19a19d0287dfcbff8b312b1d245fcfe6c09
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106357140"
---
# <a name="dml_gather_elements_operator_desc-structure-directmlh"></a><span data-ttu-id="fc5a2-103">DML_GATHER_ELEMENTS_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="fc5a2-103">DML_GATHER_ELEMENTS_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="fc5a2-104">Sammelt Elemente aus dem eingabetensor entlang der angegebenen Achse, wobei der Indexer-tensorflow verwendet wird, um die Eingabe neu zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-104">Gathers elements from the input tensor along the given axis using the indices tensor to remap into the input.</span></span> <span data-ttu-id="fc5a2-105">Dieser Operator führt den folgenden Pseudocode mit dem exakten Verhalten aus, das von der Achse, der Anzahl der Eingabe Dimensionen und der Index Dimensions Anzahl abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-105">This operator performs the following pseudocode, with the exact behavior dependent on the axis, input dimension count, and indices dimension count.</span></span>

```
output[i, j, k, ...] = input[index[i, j, k, ...], j, k, ...] // if axis == 0
output[i, j, k, ...] = input[i, index[i, j, k, ...], k, ...] // if axis == 1
output[i, j, k, ...] = input[i, j, index[i, j, k, ...], ...] // if axis == 2
...
```

> [!IMPORTANT]
> <span data-ttu-id="fc5a2-106">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="fc5a2-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="fc5a2-107">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fc5a2-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fc5a2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc5a2-108">Syntax</span></span>
```cpp
struct DML_GATHER_ELEMENTS_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="fc5a2-109">Member</span><span class="sxs-lookup"><span data-stu-id="fc5a2-109">Members</span></span>

`InputTensor`

<span data-ttu-id="fc5a2-110">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fc5a2-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fc5a2-111">Der zu lesende tensorflow.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-111">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="fc5a2-112">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fc5a2-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fc5a2-113">Die Indizes in den eingabetensor entlang der aktiven Achse.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-113">The indices into the input tensor along the active axis.</span></span> <span data-ttu-id="fc5a2-114">Die *Größen* müssen für jede Dimension außer der *Achse* mit " *inputtensor. sizes* " verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-114">The *Sizes* must match *InputTensor.Sizes* for every dimension except *Axis*.</span></span>

<span data-ttu-id="fc5a2-115">Ab `DML_FEATURE_LEVEL_3_0` unterstützt dieser Operator negative Indexwerte, wenn ein ganzzahliger Typ mit Vorzeichen mit diesem Mandanten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-115">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="fc5a2-116">Negative Indizes werden als relativ zum Ende der Achsen Dimension interpretiert.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-116">Negative indices are interpreted as being relative to the end of the axis dimension.</span></span> <span data-ttu-id="fc5a2-117">Ein Index von-1 bezieht sich z. b. auf das letzte Element in dieser Dimension.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-117">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="fc5a2-118">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fc5a2-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fc5a2-119">Der tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-119">The tensor to write the results to.</span></span> <span data-ttu-id="fc5a2-120">Die *Größen* müssen mit " *indicestensor. sizes*" verglichen werden, und der *Datentyp* muss mit " *inputtensor. DataType*" verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-120">The *Sizes* must match *IndicesTensor.Sizes*, and *DataType* must match *InputTensor.DataType*.</span></span>


`Axis`

<span data-ttu-id="fc5a2-121">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fc5a2-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="fc5a2-122">Die Achsen Dimension von *inputtensor* , die zusammengefasst werden soll `[0, *InputTensor.DimensionCount*)` .</span><span class="sxs-lookup"><span data-stu-id="fc5a2-122">The axis dimension of *InputTensor* to gather along, ranging `[0, *InputTensor.DimensionCount*)`.</span></span>

## <a name="examples"></a><span data-ttu-id="fc5a2-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc5a2-123">Examples</span></span>

```
Axis = 0

InputTensor: (Sizes:{3,3}, DataType:FLOAT32)
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]

IndicesTensor: (Sizes:{2,3}, DataType:UINT32)
    [[1, 2, 0],
     [2, 0, 0]]

// output[y, x] = input[indices[y, x], x]
OutputTensor: (Sizes:{2,3}, DataType:UINT32)
    [[4, 8, 3], // select elements vertically from data
     [7, 2, 3]]
```

## <a name="availability"></a><span data-ttu-id="fc5a2-124">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="fc5a2-124">Availability</span></span>
<span data-ttu-id="fc5a2-125">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="fc5a2-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="fc5a2-126">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="fc5a2-126">Tensor constraints</span></span>
* <span data-ttu-id="fc5a2-127">`IndicesTensor`, *Inputtensor* und *outputtensor* müssen dieselbe *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-127">`IndicesTensor`, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="fc5a2-128">*Inputtensor* und *outputtensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fc5a2-128">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fc5a2-129">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="fc5a2-129">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="fc5a2-130">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="fc5a2-130">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="fc5a2-131">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="fc5a2-131">Tensor</span></span> | <span data-ttu-id="fc5a2-132">Typ</span><span class="sxs-lookup"><span data-stu-id="fc5a2-132">Kind</span></span> | <span data-ttu-id="fc5a2-133">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="fc5a2-133">Supported dimension counts</span></span> | <span data-ttu-id="fc5a2-134">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="fc5a2-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fc5a2-135">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="fc5a2-135">InputTensor</span></span> | <span data-ttu-id="fc5a2-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fc5a2-136">Input</span></span> | <span data-ttu-id="fc5a2-137">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="fc5a2-137">1 to 8</span></span> | <span data-ttu-id="fc5a2-138">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="fc5a2-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fc5a2-139">Indikator Geber</span><span class="sxs-lookup"><span data-stu-id="fc5a2-139">IndicesTensor</span></span> | <span data-ttu-id="fc5a2-140">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fc5a2-140">Input</span></span> | <span data-ttu-id="fc5a2-141">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="fc5a2-141">1 to 8</span></span> | <span data-ttu-id="fc5a2-142">Int64, Int32, UINT64, UInt32</span><span class="sxs-lookup"><span data-stu-id="fc5a2-142">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="fc5a2-143">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="fc5a2-143">OutputTensor</span></span> | <span data-ttu-id="fc5a2-144">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fc5a2-144">Output</span></span> | <span data-ttu-id="fc5a2-145">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="fc5a2-145">1 to 8</span></span> | <span data-ttu-id="fc5a2-146">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="fc5a2-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="fc5a2-147">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="fc5a2-147">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="fc5a2-148">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="fc5a2-148">Tensor</span></span> | <span data-ttu-id="fc5a2-149">Typ</span><span class="sxs-lookup"><span data-stu-id="fc5a2-149">Kind</span></span> | <span data-ttu-id="fc5a2-150">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="fc5a2-150">Supported dimension counts</span></span> | <span data-ttu-id="fc5a2-151">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="fc5a2-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fc5a2-152">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="fc5a2-152">InputTensor</span></span> | <span data-ttu-id="fc5a2-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fc5a2-153">Input</span></span> | <span data-ttu-id="fc5a2-154">4</span><span class="sxs-lookup"><span data-stu-id="fc5a2-154">4</span></span> | <span data-ttu-id="fc5a2-155">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="fc5a2-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fc5a2-156">Indikator Geber</span><span class="sxs-lookup"><span data-stu-id="fc5a2-156">IndicesTensor</span></span> | <span data-ttu-id="fc5a2-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fc5a2-157">Input</span></span> | <span data-ttu-id="fc5a2-158">4</span><span class="sxs-lookup"><span data-stu-id="fc5a2-158">4</span></span> | <span data-ttu-id="fc5a2-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="fc5a2-159">UINT32</span></span> |
| <span data-ttu-id="fc5a2-160">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="fc5a2-160">OutputTensor</span></span> | <span data-ttu-id="fc5a2-161">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fc5a2-161">Output</span></span> | <span data-ttu-id="fc5a2-162">4</span><span class="sxs-lookup"><span data-stu-id="fc5a2-162">4</span></span> | <span data-ttu-id="fc5a2-163">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="fc5a2-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="fc5a2-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc5a2-164">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fc5a2-165">**Header**</span><span class="sxs-lookup"><span data-stu-id="fc5a2-165">**Header**</span></span> | <span data-ttu-id="fc5a2-166">directml. h</span><span class="sxs-lookup"><span data-stu-id="fc5a2-166">directml.h</span></span> |