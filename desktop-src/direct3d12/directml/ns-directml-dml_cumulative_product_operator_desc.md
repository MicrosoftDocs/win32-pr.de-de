---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Multipliziert die Elemente eines Tensors entlang einer Achse und schreibt die laufende Zählung des Produkts in den Ausgabemandor.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 71a078ad0f47c19ad1964d8d21f22e06822b5d01
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550215"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a><span data-ttu-id="2fb24-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="2fb24-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="2fb24-104">Multipliziert die Elemente eines Tensors entlang einer Achse und schreibt die laufende Zählung des Produkts in den Ausgabemandor.</span><span class="sxs-lookup"><span data-stu-id="2fb24-104">Multiplies the elements of a tensor along an axis, writing the running tally of the product into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fb24-105">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher).</span><span class="sxs-lookup"><span data-stu-id="2fb24-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="2fb24-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="2fb24-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb24-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fb24-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a><span data-ttu-id="2fb24-108">Member</span><span class="sxs-lookup"><span data-stu-id="2fb24-108">Members</span></span>

`InputTensor`

<span data-ttu-id="2fb24-109">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2fb24-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2fb24-110">Ein Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="2fb24-110">A tensor containing the input data.</span></span> <span data-ttu-id="2fb24-111">Dies ist in der Regel der gleiche Tensor, der als *InputTensor* bereitgestellt wurde, um DML_BATCH_NORMALIZATION_OPERATOR_DESC [**vorwärts**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="2fb24-111">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="2fb24-112">Der Eingabetensor, der zu multiplizierte Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="2fb24-112">The input tensor containing elements to be multiplied.</span></span>

`OutputTensor`

<span data-ttu-id="2fb24-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2fb24-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2fb24-114">Der Ausgabe tensor, in den die resultierenden kumulativen Produkte geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2fb24-114">The output tensor to write the resulting cumulative products to.</span></span> <span data-ttu-id="2fb24-115">Dieser Tensor muss die gleichen Größen und datentypen wie *InputTensor haben.*</span><span class="sxs-lookup"><span data-stu-id="2fb24-115">This tensor must have the same sizes and data type as *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="2fb24-116">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="2fb24-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="2fb24-117">Der Index der Dimension, über die Elemente multipliziert werden.</span><span class="sxs-lookup"><span data-stu-id="2fb24-117">The index of the dimension to multiply elements over.</span></span> <span data-ttu-id="2fb24-118">Dieser Wert muss kleiner als *dimensionCount des* *InputTensor sein.*</span><span class="sxs-lookup"><span data-stu-id="2fb24-118">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="2fb24-119">Typ: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="2fb24-119">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="2fb24-120">Einer der Werte der [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="2fb24-120">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="2fb24-121">Wenn auf **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, wird das Produkt durch Durchlaufen des Tensors entlang der angegebenen Achse durch den aufsteigenden Elementindex angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2fb24-121">If set to **DML_AXIS_DIRECTION_INCREASING**, then the product occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="2fb24-122">Wenn auf **DML_AXIS_DIRECTION_DECREASING** festgelegt ist, ist die Umkehrung true, und das Produkt tritt auf, indem Elemente durch einen absteigenden Index durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="2fb24-122">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true and the product occurs by traversing elements by descending index.</span></span>

`HasExclusiveProduct`

<span data-ttu-id="2fb24-123">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="2fb24-123">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="2fb24-124">True gibt an, dass der Wert des aktuellen Elements beim Schreiben der ausgeführten Tally in den Ausgabe-Tensor ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="2fb24-124">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="2fb24-125">False gibt an, dass der Wert des aktuellen Elements in der ausgeführten Tally enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2fb24-125">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="2fb24-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fb24-126">Examples</span></span>

<span data-ttu-id="2fb24-127">In den Beispielen in diesem Abschnitt wird der gleiche Eingabe-Tensor verwendet.</span><span class="sxs-lookup"><span data-stu-id="2fb24-127">The examples in this section all use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a><span data-ttu-id="2fb24-128">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="2fb24-128">Example 1.</span></span> <span data-ttu-id="2fb24-129">Kumulatives Produkt über horizontale Splitter hinweg</span><span class="sxs-lookup"><span data-stu-id="2fb24-129">Cumulative product across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a><span data-ttu-id="2fb24-130">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="2fb24-130">Example 2.</span></span> <span data-ttu-id="2fb24-131">Exklusive Produkte</span><span class="sxs-lookup"><span data-stu-id="2fb24-131">Exclusive products</span></span>

<span data-ttu-id="2fb24-132">Wenn *HasExclusiveProduct* auf **TRUE** festgelegt wird, wird der Wert des aktuellen Elements beim Schreiben in den Ausgabe-Tensor von der ausgeführten Tally ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2fb24-132">Setting *HasExclusiveProduct* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="2fb24-133">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="2fb24-133">Example 3.</span></span> <span data-ttu-id="2fb24-134">Achsenrichtung</span><span class="sxs-lookup"><span data-stu-id="2fb24-134">Axis direction</span></span>

<span data-ttu-id="2fb24-135">Wenn *AxisDirection* auf [**DML_AXIS_DIRECTION_DECREASING**](./ne-directml-dml_axis_direction.md) festgelegt wird, wird die Durchlaufreihenfolge von Elementen umgekehrt, wenn die ausgeführte tally-Berechnung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2fb24-135">Setting the *AxisDirection* to [**DML_AXIS_DIRECTION_DECREASING**](./ne-directml-dml_axis_direction.md) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a><span data-ttu-id="2fb24-136">Beispiel 4.</span><span class="sxs-lookup"><span data-stu-id="2fb24-136">Example 4.</span></span> <span data-ttu-id="2fb24-137">Multiplizieren auf einer anderen Achse</span><span class="sxs-lookup"><span data-stu-id="2fb24-137">Multiplying along a different axis</span></span>

<span data-ttu-id="2fb24-138">In diesem Beispiel tritt das Produkt vertikal entlang der Höhenachse (zweite Dimension) auf.</span><span class="sxs-lookup"><span data-stu-id="2fb24-138">In this example, the product occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a><span data-ttu-id="2fb24-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2fb24-139">Remarks</span></span>
<span data-ttu-id="2fb24-140">Dieser Operator unterstützt die direkt ausgeführte Ausführung, was bedeutet, dass der Ausgabe-Tensor während der Bindung den Alias *InputTensor* aliasen darf.</span><span class="sxs-lookup"><span data-stu-id="2fb24-140">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="2fb24-141">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="2fb24-141">Availability</span></span>
<span data-ttu-id="2fb24-142">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2fb24-142">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2fb24-143">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="2fb24-143">Tensor constraints</span></span>
<span data-ttu-id="2fb24-144">*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp* und die gleichen *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2fb24-144">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2fb24-145">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="2fb24-145">Tensor support</span></span>
| <span data-ttu-id="2fb24-146">Tensor</span><span class="sxs-lookup"><span data-stu-id="2fb24-146">Tensor</span></span> | <span data-ttu-id="2fb24-147">Typ</span><span class="sxs-lookup"><span data-stu-id="2fb24-147">Kind</span></span> | <span data-ttu-id="2fb24-148">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="2fb24-148">Supported dimension counts</span></span> | <span data-ttu-id="2fb24-149">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="2fb24-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2fb24-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="2fb24-150">InputTensor</span></span> | <span data-ttu-id="2fb24-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2fb24-151">Input</span></span> | <span data-ttu-id="2fb24-152">4</span><span class="sxs-lookup"><span data-stu-id="2fb24-152">4</span></span> | <span data-ttu-id="2fb24-153">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="2fb24-153">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="2fb24-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="2fb24-154">OutputTensor</span></span> | <span data-ttu-id="2fb24-155">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="2fb24-155">Output</span></span> | <span data-ttu-id="2fb24-156">4</span><span class="sxs-lookup"><span data-stu-id="2fb24-156">4</span></span> | <span data-ttu-id="2fb24-157">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="2fb24-157">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="2fb24-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fb24-158">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2fb24-159">**Header**</span><span class="sxs-lookup"><span data-stu-id="2fb24-159">**Header**</span></span> | <span data-ttu-id="2fb24-160">directml.h</span><span class="sxs-lookup"><span data-stu-id="2fb24-160">directml.h</span></span> |