---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Summiert die Elemente eines Tensors entlang einer Achse und schreibt die laufende Tally der Summe in den Ausgabe-Tensor.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 2862a2add207b0bb6c41f5c1aabbc390797cba23
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417887"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="353bc-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="353bc-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="353bc-104">Summiert die Elemente eines Tensors entlang einer Achse und schreibt die laufende Tally der Summe in den Ausgabe-Tensor.</span><span class="sxs-lookup"><span data-stu-id="353bc-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="353bc-105">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="353bc-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="353bc-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="353bc-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="353bc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="353bc-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```

## <a name="members"></a><span data-ttu-id="353bc-108">Member</span><span class="sxs-lookup"><span data-stu-id="353bc-108">Members</span></span>

`InputTensor`

<span data-ttu-id="353bc-109">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="353bc-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="353bc-110">Der Eingabe-Tensor, der elemente enthält, die summiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="353bc-110">The input tensor containing elements to be summed.</span></span>

`OutputTensor`

<span data-ttu-id="353bc-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="353bc-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="353bc-112">Der Ausgabe-Tensor, in den die resultierenden kumulativen Summierungen geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="353bc-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="353bc-113">Dieser Tensor muss die gleichen Größen und denselben Datentyp wie *inputTensor aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="353bc-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="353bc-114">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="353bc-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="353bc-115">Der Index der Dimension, über die Elemente summt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="353bc-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="353bc-116">Dieser Wert muss kleiner als *dimensionCount* des *InputTensor* sein.</span><span class="sxs-lookup"><span data-stu-id="353bc-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="353bc-117">Typ: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="353bc-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="353bc-118">Einer der Werte [](./ne-directml-dml_axis_direction.md) der DML_AXIS_DIRECTION-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="353bc-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="353bc-119">Wenn auf **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, erfolgt die Summierung durch Durchlaufen des Tensors entlang der angegebenen Achse durch aufsteigenden Elementindex.</span><span class="sxs-lookup"><span data-stu-id="353bc-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="353bc-120">Wenn auf **DML_AXIS_DIRECTION_DECREASING** festgelegt ist, ist der umgekehrte Wert true, und die Summierung erfolgt durch Durchlaufen von Elementen durch absteigenden Index.</span><span class="sxs-lookup"><span data-stu-id="353bc-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>

`HasExclusiveSum`

<span data-ttu-id="353bc-121">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="353bc-121">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="353bc-122">True gibt an, dass der Wert des aktuellen Elements beim Schreiben der ausgeführten Tally in den Ausgabe-Tensor ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="353bc-122">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="353bc-123">False gibt an, dass der Wert des aktuellen Elements in der ausgeführten Tally enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="353bc-123">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="353bc-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="353bc-124">Examples</span></span>

<span data-ttu-id="353bc-125">In den Beispielen in diesem Abschnitt wird ein Eingabe-Tensor mit den folgenden Eigenschaften verwendet.</span><span class="sxs-lookup"><span data-stu-id="353bc-125">The examples in this section all use an input tensor with the following properties.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-summation-across-horizontal-slivers"></a><span data-ttu-id="353bc-126">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="353bc-126">Example 1.</span></span> <span data-ttu-id="353bc-127">Kumulierte Summierung über horizontale Slivers hinweg</span><span class="sxs-lookup"><span data-stu-id="353bc-127">Cumulative summation across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  3,  6, 11],     // i.e. [2, 2+1, 2+1+3, 2+1+3+5]
   [3, 11, 18, 21],     //      [...                   ]
   [9, 15, 17, 21]]]]   //      [...                   ]
```

### <a name="example-2-exclusive-sums"></a><span data-ttu-id="353bc-128">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="353bc-128">Example 2.</span></span> <span data-ttu-id="353bc-129">Exklusive Summen</span><span class="sxs-lookup"><span data-stu-id="353bc-129">Exclusive sums</span></span>

<span data-ttu-id="353bc-130">Wenn *HasExclusiveSum* auf **TRUE** festgelegt wird, wird der Wert des aktuellen Elements beim Schreiben in den Ausgabe-Tensor von der ausgeführten Tally ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="353bc-130">Setting *HasExclusiveSum* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[0, 2,  3,  6],      // Notice the sum is written before adding the input,
   [0, 3, 11, 18],      // and the final total is not written to any output.
   [0, 9, 15, 17]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="353bc-131">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="353bc-131">Example 3.</span></span> <span data-ttu-id="353bc-132">Achsenrichtung</span><span class="sxs-lookup"><span data-stu-id="353bc-132">Axis direction</span></span>

<span data-ttu-id="353bc-133">Wenn *AxisDirection* auf [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) festgelegt wird, wird die Durchlaufreihenfolge von Elementen umgekehrt, wenn die ausgeführte tally-Berechnung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="353bc-133">Setting the *AxisDirection* to [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[11,  9,  8,  5],    // i.e. [2+1+3+5, 1+3+5, 3+5, 5]
   [21, 18, 10,  3],    //      [...                   ]
   [21, 12,  6,  4]]]]  //      [...                   ]
```

### <a name="example-4-summing-along-a-different-axis"></a><span data-ttu-id="353bc-134">Beispiel 4.</span><span class="sxs-lookup"><span data-stu-id="353bc-134">Example 4.</span></span> <span data-ttu-id="353bc-135">Summieren entlang einer anderen Achse</span><span class="sxs-lookup"><span data-stu-id="353bc-135">Summing along a different axis</span></span>

<span data-ttu-id="353bc-136">In diesem Beispiel erfolgt die Summierung vertikal entlang der Höhenachse (zweite Dimension).</span><span class="sxs-lookup"><span data-stu-id="353bc-136">In this example, the summation occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 5,  9, 10,  8],   //      [2+3,  ...]
   [14, 15, 12, 12]]]] //      [2+3+9 ...]
```

## <a name="remarks"></a><span data-ttu-id="353bc-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="353bc-137">Remarks</span></span>
<span data-ttu-id="353bc-138">Dieser Operator unterstützt die direkt ausgeführte Ausführung, d. h., der *OutputTensor* darf während der Bindung einen Alias für *InputTensor* setzen.</span><span class="sxs-lookup"><span data-stu-id="353bc-138">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="353bc-139">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="353bc-139">Availability</span></span>
<span data-ttu-id="353bc-140">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="353bc-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="353bc-141">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="353bc-141">Tensor constraints</span></span>
<span data-ttu-id="353bc-142">*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp* und die gleichen *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="353bc-142">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="353bc-143">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="353bc-143">Tensor support</span></span>
| <span data-ttu-id="353bc-144">Tensor</span><span class="sxs-lookup"><span data-stu-id="353bc-144">Tensor</span></span> | <span data-ttu-id="353bc-145">Typ</span><span class="sxs-lookup"><span data-stu-id="353bc-145">Kind</span></span> | <span data-ttu-id="353bc-146">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="353bc-146">Supported dimension counts</span></span> | <span data-ttu-id="353bc-147">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="353bc-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="353bc-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="353bc-148">InputTensor</span></span> | <span data-ttu-id="353bc-149">Eingabe</span><span class="sxs-lookup"><span data-stu-id="353bc-149">Input</span></span> | <span data-ttu-id="353bc-150">4</span><span class="sxs-lookup"><span data-stu-id="353bc-150">4</span></span> | <span data-ttu-id="353bc-151">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="353bc-151">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="353bc-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="353bc-152">OutputTensor</span></span> | <span data-ttu-id="353bc-153">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="353bc-153">Output</span></span> | <span data-ttu-id="353bc-154">4</span><span class="sxs-lookup"><span data-stu-id="353bc-154">4</span></span> | <span data-ttu-id="353bc-155">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="353bc-155">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="353bc-156">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="353bc-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="353bc-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="353bc-157">**Header**</span></span> | <span data-ttu-id="353bc-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="353bc-158">directml.h</span></span> |
