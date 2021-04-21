---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Wählt die größten oder kleinsten *K-Elemente* aus jeder Sequenz entlang einer Achse des *InputTensor* aus und gibt die Werte und Indizes dieser Elemente im *OutputValueTensor* bzw. *OutputIndexTensor* zurück.
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
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
f1_keywords:
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803817"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a><span data-ttu-id="98023-103">DML_TOP_K1_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="98023-103">DML_TOP_K1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="98023-104">Wählt die größten oder kleinsten *K-Elemente* aus jeder Sequenz entlang einer Achse des *InputTensor* aus und gibt die Werte und Indizes dieser Elemente im *OutputValueTensor* bzw. *OutputIndexTensor* zurück.</span><span class="sxs-lookup"><span data-stu-id="98023-104">Selects the largest or smallest *K* elements from each sequence along an axis of the *InputTensor*, and returns the values and indices of those elements in the *OutputValueTensor* and *OutputIndexTensor*, respectively.</span></span> <span data-ttu-id="98023-105">Eine *Sequenz* bezieht sich auf einen der Sätze von Elementen, die entlang der *Axis-Dimension* von *InputTensor vorhanden sind.*</span><span class="sxs-lookup"><span data-stu-id="98023-105">A *sequence* refers to one of the sets of elements that exist along the *Axis* dimension of the *InputTensor*.</span></span>

<span data-ttu-id="98023-106">Die Wahl, ob die größten K-Elemente oder die kleinsten K-Elemente ausgewählt werden sollen, kann mit *AxisDirection gesteuert werden.*</span><span class="sxs-lookup"><span data-stu-id="98023-106">The choice of whether to select the largest K elements or the smallest K elements can be controlled using *AxisDirection*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98023-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="98023-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="98023-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="98023-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="98023-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="98023-109">Syntax</span></span>
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="98023-110">Member</span><span class="sxs-lookup"><span data-stu-id="98023-110">Members</span></span>

`InputTensor`

<span data-ttu-id="98023-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="98023-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="98023-112">Der Eingabetensor, der auszuwählende Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="98023-112">The input tensor containing elements to select.</span></span>

`OutputValueTensor`

<span data-ttu-id="98023-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="98023-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="98023-114">Der Ausgabe tensor, in den die Werte der obersten *K-Elemente geschrieben* werden.</span><span class="sxs-lookup"><span data-stu-id="98023-114">The output tensor to write the values of the top *K* elements to.</span></span> <span data-ttu-id="98023-115">Die obersten *K-Elemente* werden abhängig vom Wert von *AxisDirection* ausgewählt, je nachdem, ob sie das größte oder das kleinste sind.</span><span class="sxs-lookup"><span data-stu-id="98023-115">The top *K* elements are selected based on whether they are the largest or the smallest, depending on the value of *AxisDirection*.</span></span> <span data-ttu-id="98023-116">Dieser Tensor muss größen gleich dem *InputTensor* *aufweisen,* mit Ausnahme der dimension, die durch den *Axis-Parameter* angegeben wird, der eine Größe von K *aufweisen muss.*</span><span class="sxs-lookup"><span data-stu-id="98023-116">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="98023-117">Die in jeder Eingabesequenz ausgewählten *K-Werte* werden garantiert absteigend sortiert (größte bis [kleinste),](./ne-directml-dml_axis_direction.md)wenn *AxisDirection* DML_AXIS_DIRECTION_DECREASING.</span><span class="sxs-lookup"><span data-stu-id="98023-117">The *K* values selected from each input sequence are guaranteed to be sorted descending (largest to smallest) if *AxisDirection* is [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span></span> <span data-ttu-id="98023-118">Andernfalls ist das Gegenteil true, und die ausgewählten Werte sind garantiert aufsteigend sortiert (klein bis größten).</span><span class="sxs-lookup"><span data-stu-id="98023-118">Otherwise, the opposite is true and the values selected are guaranteed to be sorted ascending (smallest to largest).</span></span>

`OutputIndexTensor`

<span data-ttu-id="98023-119">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="98023-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="98023-120">Der Ausgabe tensor, in den die Indizes der obersten *K-Elemente geschrieben* werden.</span><span class="sxs-lookup"><span data-stu-id="98023-120">The output tensor to write the indices of the top *K* elements to.</span></span> <span data-ttu-id="98023-121">Dieser Tensor muss größengleich mit *inputTensor* sein, *mit Ausnahme* der Dimension, die durch den *Axis-Parameter* angegeben wird und eine Größe von *gleich K* aufweisen muss.</span><span class="sxs-lookup"><span data-stu-id="98023-121">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="98023-122">Die in diesem Tensor zurückgegebenen Indizes werden relativ zum Anfang ihrer Sequenz gemessen (im Gegensatz zum Anfang des Tensors).</span><span class="sxs-lookup"><span data-stu-id="98023-122">The indices returned in this tensor are measured relative to the beginning of their sequence (as opposed to the beginning of the tensor).</span></span> <span data-ttu-id="98023-123">Beispielsweise bezieht sich ein Index von 0 immer auf das erste Element für alle Sequenzen in einer Achse.</span><span class="sxs-lookup"><span data-stu-id="98023-123">For example, an index of 0 always refers to the first element for all sequences in an axis.</span></span>

<span data-ttu-id="98023-124">In Fällen, in denen zwei oder mehr Elemente im oberen K den gleichen Wert haben (d. h. wenn ein Gleichstand vorliegt), werden die Indizes beider Elemente eingeschlossen und werden garantiert nach aufsteigender Elementindex sortiert.</span><span class="sxs-lookup"><span data-stu-id="98023-124">In cases where two or more elements in the top-K have the same value (that is, when there is a tie), the indices of both elements are included, and are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="98023-125">Beachten Sie, dass dies unabhängig vom Wert von *AxisDirection* zutrifft.</span><span class="sxs-lookup"><span data-stu-id="98023-125">Note that this is true irrespective of the value of *AxisDirection*.</span></span>

`Axis`

<span data-ttu-id="98023-126">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="98023-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="98023-127">Der Index der Dimension, über die Elemente ausgewählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="98023-127">The index of the dimension to select elements across.</span></span> <span data-ttu-id="98023-128">Dieser Wert muss kleiner als *dimensionCount* des *InputTensor* sein.</span><span class="sxs-lookup"><span data-stu-id="98023-128">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`K`

<span data-ttu-id="98023-129">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="98023-129">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="98023-130">Die Anzahl der auszuwählende Elemente.</span><span class="sxs-lookup"><span data-stu-id="98023-130">The number of elements to select.</span></span> <span data-ttu-id="98023-131">*K* muss größer als 0 sein, aber kleiner als die Anzahl der Elemente im *InputTensor* entlang der Dimension, die von *Achse* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="98023-131">*K* must be greater than 0, but less than the number of elements in the *InputTensor* along the dimension specified by *Axis*.</span></span>

`AxisDirection`

<span data-ttu-id="98023-132">Typ: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="98023-132">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="98023-133">Ein Wert [](./ne-directml-dml_axis_direction.md) aus der DML_AXIS_DIRECTION-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="98023-133">A value from the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="98023-134">Wenn auf **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, gibt dieser Operator die *kleinsten* *K-Elemente* in der Reihenfolge des erhöhenden Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="98023-134">If set to **DML_AXIS_DIRECTION_INCREASING**, then this operator returns the *smallest* *K* elements in order of increasing value.</span></span> <span data-ttu-id="98023-135">Andernfalls werden die *größten* *K-Elemente* in absteigender Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="98023-135">Otherwise, it returns the *largest* *K* elements in decreasing order.</span></span>

## <a name="examples"></a><span data-ttu-id="98023-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98023-136">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="98023-137">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98023-137">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a><span data-ttu-id="98023-138">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="98023-138">Example 2.</span></span> <span data-ttu-id="98023-139">Verwenden einer anderen Achse</span><span class="sxs-lookup"><span data-stu-id="98023-139">Using a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a><span data-ttu-id="98023-140">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="98023-140">Example 3.</span></span> <span data-ttu-id="98023-141">Verknüpfte Werte</span><span class="sxs-lookup"><span data-stu-id="98023-141">Tied values</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a><span data-ttu-id="98023-142">Beispiel 4.</span><span class="sxs-lookup"><span data-stu-id="98023-142">Example 4.</span></span> <span data-ttu-id="98023-143">Erhöhen der Achsenrichtung</span><span class="sxs-lookup"><span data-stu-id="98023-143">Increasing axis direction</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a><span data-ttu-id="98023-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98023-144">Remarks</span></span>
<span data-ttu-id="98023-145">Wenn *AxisDirection* auf [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md)festgelegt ist, entspricht dieser Operator [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="98023-145">When *AxisDirection* is set to [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), this operator is equivalent to [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="98023-146">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="98023-146">Availability</span></span>
<span data-ttu-id="98023-147">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="98023-147">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="98023-148">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="98023-148">Tensor constraints</span></span>

* <span data-ttu-id="98023-149">*InputTensor,* *OutputIndexTensor* und *OutputValueTensor* müssen denselben *DimensionCount aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="98023-149">*InputTensor*, *OutputIndexTensor*, and *OutputValueTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="98023-150">*InputTensor und* *OutputValueTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="98023-150">*InputTensor* and *OutputValueTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="98023-151">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="98023-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="98023-152">DML_FEATURE_LEVEL_3_1 und höher</span><span class="sxs-lookup"><span data-stu-id="98023-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="98023-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="98023-153">Tensor</span></span> | <span data-ttu-id="98023-154">Typ</span><span class="sxs-lookup"><span data-stu-id="98023-154">Kind</span></span> | <span data-ttu-id="98023-155">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="98023-155">Supported dimension counts</span></span> | <span data-ttu-id="98023-156">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="98023-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="98023-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="98023-157">InputTensor</span></span> | <span data-ttu-id="98023-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="98023-158">Input</span></span> | <span data-ttu-id="98023-159">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="98023-159">1 to 8</span></span> | <span data-ttu-id="98023-160">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="98023-160">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="98023-161">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="98023-161">OutputValueTensor</span></span> | <span data-ttu-id="98023-162">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="98023-162">Output</span></span> | <span data-ttu-id="98023-163">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="98023-163">1 to 8</span></span> | <span data-ttu-id="98023-164">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="98023-164">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="98023-165">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="98023-165">OutputIndexTensor</span></span> | <span data-ttu-id="98023-166">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="98023-166">Output</span></span> | <span data-ttu-id="98023-167">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="98023-167">1 to 8</span></span> | <span data-ttu-id="98023-168">UINT32</span><span class="sxs-lookup"><span data-stu-id="98023-168">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="98023-169">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="98023-169">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="98023-170">Tensor</span><span class="sxs-lookup"><span data-stu-id="98023-170">Tensor</span></span> | <span data-ttu-id="98023-171">Typ</span><span class="sxs-lookup"><span data-stu-id="98023-171">Kind</span></span> | <span data-ttu-id="98023-172">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="98023-172">Supported dimension counts</span></span> | <span data-ttu-id="98023-173">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="98023-173">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="98023-174">InputTensor</span><span class="sxs-lookup"><span data-stu-id="98023-174">InputTensor</span></span> | <span data-ttu-id="98023-175">Eingabe</span><span class="sxs-lookup"><span data-stu-id="98023-175">Input</span></span> | <span data-ttu-id="98023-176">4</span><span class="sxs-lookup"><span data-stu-id="98023-176">4</span></span> | <span data-ttu-id="98023-177">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="98023-177">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="98023-178">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="98023-178">OutputValueTensor</span></span> | <span data-ttu-id="98023-179">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="98023-179">Output</span></span> | <span data-ttu-id="98023-180">4</span><span class="sxs-lookup"><span data-stu-id="98023-180">4</span></span> | <span data-ttu-id="98023-181">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="98023-181">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="98023-182">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="98023-182">OutputIndexTensor</span></span> | <span data-ttu-id="98023-183">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="98023-183">Output</span></span> | <span data-ttu-id="98023-184">4</span><span class="sxs-lookup"><span data-stu-id="98023-184">4</span></span> | <span data-ttu-id="98023-185">UINT32</span><span class="sxs-lookup"><span data-stu-id="98023-185">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="98023-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98023-186">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="98023-187">**Header**</span><span class="sxs-lookup"><span data-stu-id="98023-187">**Header**</span></span> | <span data-ttu-id="98023-188">directml.h</span><span class="sxs-lookup"><span data-stu-id="98023-188">directml.h</span></span> |
