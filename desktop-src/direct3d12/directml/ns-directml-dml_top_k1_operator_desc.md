---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Wählt die größten oder kleinsten *K* -Elemente aus jeder Sequenz entlang einer Achse von *inputtensor* aus und gibt die Werte und Indizes dieser Elemente in *outputvaluetensor* bzw. *outputindextensor* zurück.
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
ms.openlocfilehash: 8c5b9bf58a8582588d19878c7e06c602584777fa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351191"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a><span data-ttu-id="159e8-103">DML_TOP_K1_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="159e8-103">DML_TOP_K1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="159e8-104">Wählt die größten oder kleinsten *K* -Elemente aus jeder Sequenz entlang einer Achse von *inputtensor* aus und gibt die Werte und Indizes dieser Elemente in *outputvaluetensor* bzw. *outputindextensor* zurück.</span><span class="sxs-lookup"><span data-stu-id="159e8-104">Selects the largest or smallest *K* elements from each sequence along an axis of the *InputTensor*, and returns the values and indices of those elements in the *OutputValueTensor* and *OutputIndexTensor*, respectively.</span></span> <span data-ttu-id="159e8-105">Eine *Sequenz* verweist auf eine Reihe von Elementen, die entlang der *Achsen* Dimension von *inputtensor* vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="159e8-105">A *sequence* refers to one of the sets of elements that exist along the *Axis* dimension of the *InputTensor*.</span></span>

<span data-ttu-id="159e8-106">Die Auswahl, ob die größten k-Elemente oder die kleinsten k-Elemente ausgewählt werden sollen, kann mithilfe von *axisdirection* gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="159e8-106">The choice of whether to select the largest K elements or the smallest K elements can be controlled using *AxisDirection*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="159e8-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="159e8-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="159e8-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="159e8-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="159e8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="159e8-109">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="159e8-110">Member</span><span class="sxs-lookup"><span data-stu-id="159e8-110">Members</span></span>

`InputTensor`

<span data-ttu-id="159e8-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="159e8-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="159e8-112">Der eingabensor mit den Elementen, die ausgewählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="159e8-112">The input tensor containing elements to select.</span></span>


`OutputValueTensor`

<span data-ttu-id="159e8-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="159e8-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="159e8-114">Der Ausgabe Mandanten, in den die Werte der obersten *K* Elemente geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="159e8-114">The output tensor to write the values of the top *K* elements to.</span></span> <span data-ttu-id="159e8-115">Abhängig vom Wert von *axisdirection* werden die obersten *K* Elemente basierend darauf ausgewählt, ob Sie der größte oder kleinste Wert sind.</span><span class="sxs-lookup"><span data-stu-id="159e8-115">The top *K* elements are selected based on whether they are the largest or the smallest, depending on the value of *AxisDirection*.</span></span> <span data-ttu-id="159e8-116">Dieser tensorflow muss Übergrößen verfügen, die mit dem *inputtensor* identisch sind, *mit Ausnahme* der durch den *Axis* -Parameter angegebenen Dimension, deren Größe gleich *K* sein muss.</span><span class="sxs-lookup"><span data-stu-id="159e8-116">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="159e8-117">Die aus jeder Eingabe Sequenz ausgewählten *K* -Werte werden garantiert absteigend sortiert (der größte zu kleinste Wert), wenn *axisdirection* [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md)ist.</span><span class="sxs-lookup"><span data-stu-id="159e8-117">The *K* values selected from each input sequence are guaranteed to be sorted descending (largest to smallest) if *AxisDirection* is [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span></span> <span data-ttu-id="159e8-118">Andernfalls ist das Gegenteil der Fall, und die ausgewählten Werte werden garantiert aufsteigend sortiert (der kleinste zum größten Wert).</span><span class="sxs-lookup"><span data-stu-id="159e8-118">Otherwise, the opposite is true and the values selected are guaranteed to be sorted ascending (smallest to largest).</span></span>


`OutputIndexTensor`

<span data-ttu-id="159e8-119">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="159e8-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="159e8-120">Der Ausgabe Mandanten, in den die Indizes der obersten *K* Elemente geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="159e8-120">The output tensor to write the indices of the top *K* elements to.</span></span> <span data-ttu-id="159e8-121">Dieser tensorflow muss Übergrößen verfügen, die mit dem *inputtensor* identisch sind, *mit Ausnahme* der durch den *Axis* -Parameter angegebenen Dimension, deren Größe gleich *K* sein muss.</span><span class="sxs-lookup"><span data-stu-id="159e8-121">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="159e8-122">Die Indizes, die in diesem Mandanten zurückgegeben werden, werden relativ zum Anfang der Sequenz (im Gegensatz zum Anfang des Mandanten) gemessen.</span><span class="sxs-lookup"><span data-stu-id="159e8-122">The indices returned in this tensor are measured relative to the beginning of their sequence (as opposed to the beginning of the tensor).</span></span> <span data-ttu-id="159e8-123">Beispielsweise verweist der Index 0 immer auf das erste Element für alle Sequenzen in einer Achse.</span><span class="sxs-lookup"><span data-stu-id="159e8-123">For example, an index of 0 always refers to the first element for all sequences in an axis.</span></span>

<span data-ttu-id="159e8-124">In Fällen, in denen zwei oder mehr Elemente im oberen-K denselben Wert aufweisen (d. h., wenn ein gleich geordnetes Element vorhanden ist), werden die Indizes beider Elemente eingeschlossen, und die Sortierung erfolgt nach dem aufsteigenden Element Index.</span><span class="sxs-lookup"><span data-stu-id="159e8-124">In cases where two or more elements in the top-K have the same value (that is, when there is a tie), the indices of both elements are included, and are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="159e8-125">Beachten Sie, dass dies unabhängig vom Wert von *axisdirection* true ist.</span><span class="sxs-lookup"><span data-stu-id="159e8-125">Note that this is true irrespective of the value of *AxisDirection*.</span></span>


`Axis`

<span data-ttu-id="159e8-126">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="159e8-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="159e8-127">Der Index der Dimension, in der Elemente ausgewählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="159e8-127">The index of the dimension to select elements across.</span></span> <span data-ttu-id="159e8-128">Dieser Wert muss kleiner als die *DimensionCount* von " *inputtensor*" sein.</span><span class="sxs-lookup"><span data-stu-id="159e8-128">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`K`

<span data-ttu-id="159e8-129">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="159e8-129">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="159e8-130">Die Anzahl der Elemente, die ausgewählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="159e8-130">The number of elements to select.</span></span> <span data-ttu-id="159e8-131">*K* muss größer als 0 (null) sein, aber kleiner als die Anzahl der Elemente im *inputtensor* entlang der durch die *Achse* angegebenen Dimension.</span><span class="sxs-lookup"><span data-stu-id="159e8-131">*K* must be greater than 0, but less than the number of elements in the *InputTensor* along the dimension specified by *Axis*.</span></span>


`AxisDirection`

<span data-ttu-id="159e8-132">Typ: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="159e8-132">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="159e8-133">Ein Wert aus der [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="159e8-133">A value from the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="159e8-134">Wenn **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, gibt dieser Operator die *kleinsten* *K* Elemente in der Reihenfolge zurück, in der der Wert zunimmt.</span><span class="sxs-lookup"><span data-stu-id="159e8-134">If set to **DML_AXIS_DIRECTION_INCREASING**, then this operator returns the *smallest* *K* elements in order of increasing value.</span></span> <span data-ttu-id="159e8-135">Andernfalls werden die *größten* *K* Elemente in absteigender Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="159e8-135">Otherwise, it returns the *largest* *K* elements in decreasing order.</span></span>

## <a name="examples"></a><span data-ttu-id="159e8-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="159e8-136">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="159e8-137">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="159e8-137">Example 1</span></span>

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

### <a name="example-2-using-a-different-axis"></a><span data-ttu-id="159e8-138">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="159e8-138">Example 2.</span></span> <span data-ttu-id="159e8-139">Verwenden einer anderen Achse</span><span class="sxs-lookup"><span data-stu-id="159e8-139">Using a different axis</span></span>

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

### <a name="example-3-tied-values"></a><span data-ttu-id="159e8-140">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="159e8-140">Example 3.</span></span> <span data-ttu-id="159e8-141">Gebundene Werte</span><span class="sxs-lookup"><span data-stu-id="159e8-141">Tied values</span></span>

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

### <a name="example-4-increasing-axis-direction"></a><span data-ttu-id="159e8-142">Beispiel 4:</span><span class="sxs-lookup"><span data-stu-id="159e8-142">Example 4.</span></span> <span data-ttu-id="159e8-143">Erhöhen der Achsen Richtung</span><span class="sxs-lookup"><span data-stu-id="159e8-143">Increasing axis direction</span></span>

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


## <a name="remarks"></a><span data-ttu-id="159e8-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="159e8-144">Remarks</span></span>
<span data-ttu-id="159e8-145">Wenn *axisdirection* auf [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md)festgelegt ist, entspricht dieser Operator [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="159e8-145">When *AxisDirection* is set to [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), this operator is equivalent to [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="159e8-146">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="159e8-146">Availability</span></span>
<span data-ttu-id="159e8-147">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="159e8-147">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="159e8-148">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="159e8-148">Tensor constraints</span></span>
* <span data-ttu-id="159e8-149">*Inputtensor* und *outputvaluetensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="159e8-149">*InputTensor* and *OutputValueTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="159e8-150">*Outputindextensor* und *outputvaluetensor* müssen die gleichen *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="159e8-150">*OutputIndexTensor* and *OutputValueTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="159e8-151">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="159e8-151">Tensor support</span></span>
| <span data-ttu-id="159e8-152">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="159e8-152">Tensor</span></span> | <span data-ttu-id="159e8-153">Typ</span><span class="sxs-lookup"><span data-stu-id="159e8-153">Kind</span></span> | <span data-ttu-id="159e8-154">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="159e8-154">Dimensions</span></span> | <span data-ttu-id="159e8-155">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="159e8-155">Supported dimension counts</span></span> | <span data-ttu-id="159e8-156">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="159e8-156">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="159e8-157">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="159e8-157">InputTensor</span></span> | <span data-ttu-id="159e8-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="159e8-158">Input</span></span> | <span data-ttu-id="159e8-159">{ In0, In1, In2, In3 }</span><span class="sxs-lookup"><span data-stu-id="159e8-159">{ In0, In1, In2, In3 }</span></span> | <span data-ttu-id="159e8-160">4</span><span class="sxs-lookup"><span data-stu-id="159e8-160">4</span></span> | <span data-ttu-id="159e8-161">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="159e8-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="159e8-162">Outputvaluetensor</span><span class="sxs-lookup"><span data-stu-id="159e8-162">OutputValueTensor</span></span> | <span data-ttu-id="159e8-163">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="159e8-163">Output</span></span> | <span data-ttu-id="159e8-164">{ Out0, Out1, Out2, Out3 }</span><span class="sxs-lookup"><span data-stu-id="159e8-164">{ Out0, Out1, Out2, Out3 }</span></span> | <span data-ttu-id="159e8-165">4</span><span class="sxs-lookup"><span data-stu-id="159e8-165">4</span></span> | <span data-ttu-id="159e8-166">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="159e8-166">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="159e8-167">Outputindextensor</span><span class="sxs-lookup"><span data-stu-id="159e8-167">OutputIndexTensor</span></span> | <span data-ttu-id="159e8-168">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="159e8-168">Output</span></span> | <span data-ttu-id="159e8-169">{ Out0, Out1, Out2, Out3 }</span><span class="sxs-lookup"><span data-stu-id="159e8-169">{ Out0, Out1, Out2, Out3 }</span></span> | <span data-ttu-id="159e8-170">4</span><span class="sxs-lookup"><span data-stu-id="159e8-170">4</span></span> | <span data-ttu-id="159e8-171">UINT32</span><span class="sxs-lookup"><span data-stu-id="159e8-171">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="159e8-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="159e8-172">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="159e8-173">**Header**</span><span class="sxs-lookup"><span data-stu-id="159e8-173">**Header**</span></span> | <span data-ttu-id="159e8-174">directml. h</span><span class="sxs-lookup"><span data-stu-id="159e8-174">directml.h</span></span> |