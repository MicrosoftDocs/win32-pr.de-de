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
ms.openlocfilehash: cb4006a20dd25751c027ba97e63dcfc60c25faf6
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282559"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a><span data-ttu-id="cd7f2-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="cd7f2-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="cd7f2-104">Multipliziert die Elemente eines Tensors entlang einer Achse und schreibt die laufende Zählung des Produkts in den Ausgabemandor.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-104">Multiplies the elements of a tensor along an axis, writing the running tally of the product into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd7f2-105">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher).</span><span class="sxs-lookup"><span data-stu-id="cd7f2-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="cd7f2-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="cd7f2-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd7f2-107">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="cd7f2-108">Member</span><span class="sxs-lookup"><span data-stu-id="cd7f2-108">Members</span></span>

`InputTensor`

<span data-ttu-id="cd7f2-109">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd7f2-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd7f2-110">Ein Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-110">A tensor containing the input data.</span></span> <span data-ttu-id="cd7f2-111">Dies ist in der Regel der gleiche Tensor, der als *InputTensor* bereitgestellt wurde, um DML_BATCH_NORMALIZATION_OPERATOR_DESC [**vorwärts**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-111">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="cd7f2-112">Der Eingabetensor, der zu multiplizierte Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-112">The input tensor containing elements to be multiplied.</span></span>

`OutputTensor`

<span data-ttu-id="cd7f2-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd7f2-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd7f2-114">Der Ausgabe tensor, in den die resultierenden kumulativen Produkte geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-114">The output tensor to write the resulting cumulative products to.</span></span> <span data-ttu-id="cd7f2-115">Dieser Tensor muss die gleichen Größen und Datentypen wie *InputTensor haben.*</span><span class="sxs-lookup"><span data-stu-id="cd7f2-115">This tensor must have the same sizes and data type as *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="cd7f2-116">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cd7f2-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="cd7f2-117">Der Index der Dimension, über die Elemente multipliziert werden.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-117">The index of the dimension to multiply elements over.</span></span> <span data-ttu-id="cd7f2-118">Dieser Wert muss kleiner als *dimensionCount des* *InputTensor-Werts sein.*</span><span class="sxs-lookup"><span data-stu-id="cd7f2-118">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="cd7f2-119">Typ: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="cd7f2-119">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="cd7f2-120">Einer der Werte der [DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-120">One of the values of the [DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction) enumeration.</span></span> <span data-ttu-id="cd7f2-121">Wenn auf **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, wird das Produkt durch Durchlaufen des Tensors entlang der angegebenen Achse durch den aufsteigenden Elementindex angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-121">If set to **DML_AXIS_DIRECTION_INCREASING**, then the product occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="cd7f2-122">Wenn auf **DML_AXIS_DIRECTION_DECREASING** festgelegt ist, ist die Umkehrung true, und das Produkt tritt auf, indem Elemente durch einen absteigenden Index durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-122">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true and the product occurs by traversing elements by descending index.</span></span>

`HasExclusiveProduct`

<span data-ttu-id="cd7f2-123">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="cd7f2-123">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="cd7f2-124">True **gibt** an, dass der Wert des aktuellen Elements ausgeschlossen wird, wenn die laufende Klammer in den Ausgabemandator geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-124">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="cd7f2-125">False **gibt** an, dass der Wert des aktuellen Elements in der ausgeführten Zählung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-125">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="cd7f2-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd7f2-126">Examples</span></span>

<span data-ttu-id="cd7f2-127">In den Beispielen in diesem Abschnitt wird der gleiche Eingabetensor verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-127">The examples in this section all use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a><span data-ttu-id="cd7f2-128">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="cd7f2-128">Example 1.</span></span> <span data-ttu-id="cd7f2-129">Kumulatives Produkt über horizontale Schrägstriche</span><span class="sxs-lookup"><span data-stu-id="cd7f2-129">Cumulative product across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a><span data-ttu-id="cd7f2-130">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="cd7f2-130">Example 2.</span></span> <span data-ttu-id="cd7f2-131">Exklusive Produkte</span><span class="sxs-lookup"><span data-stu-id="cd7f2-131">Exclusive products</span></span>

<span data-ttu-id="cd7f2-132">Das *Festlegen von HasExclusiveProduct* auf **TRUE** hat den Effekt, dass der Wert des aktuellen Elements beim Schreiben in den Ausgabemandor von der ausgeführten Zählung ausgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-132">Setting *HasExclusiveProduct* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="cd7f2-133">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="cd7f2-133">Example 3.</span></span> <span data-ttu-id="cd7f2-134">Achsenrichtung</span><span class="sxs-lookup"><span data-stu-id="cd7f2-134">Axis direction</span></span>

<span data-ttu-id="cd7f2-135">Das Festlegen *von AxisDirection* auf [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) hat den Effekt, dass die Durchlaufrichtung der Elemente beim Berechnen der laufenden Zählung umkehrt.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-135">Setting the *AxisDirection* to [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a><span data-ttu-id="cd7f2-136">Beispiel 4.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-136">Example 4.</span></span> <span data-ttu-id="cd7f2-137">Multiplizieren entlang einer anderen Achse</span><span class="sxs-lookup"><span data-stu-id="cd7f2-137">Multiplying along a different axis</span></span>

<span data-ttu-id="cd7f2-138">In diesem Beispiel tritt das Produkt vertikal entlang der Höhenachse (zweite Dimension) auf.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-138">In this example, the product occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a><span data-ttu-id="cd7f2-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd7f2-139">Remarks</span></span>
<span data-ttu-id="cd7f2-140">Dieser Operator unterstützt die in-place-Ausführung, was bedeutet, dass der Ausgabetensor während der Bindung den *Alias InputTensor* verwenden darf.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-140">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="cd7f2-141">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="cd7f2-141">Availability</span></span>
<span data-ttu-id="cd7f2-142">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cd7f2-142">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cd7f2-143">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="cd7f2-143">Tensor constraints</span></span>
<span data-ttu-id="cd7f2-144">*InputTensor* und *OutputTensor* müssen denselben *DataType,* *DimensionCount* und *die gleichen Größen aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="cd7f2-144">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cd7f2-145">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="cd7f2-145">Tensor support</span></span>
### <a name="dml_feature_level_4_0-and-above"></a><span data-ttu-id="cd7f2-146">DML_FEATURE_LEVEL_4_0 und höher</span><span class="sxs-lookup"><span data-stu-id="cd7f2-146">DML_FEATURE_LEVEL_4_0 and above</span></span>
| <span data-ttu-id="cd7f2-147">Tensor</span><span class="sxs-lookup"><span data-stu-id="cd7f2-147">Tensor</span></span> | <span data-ttu-id="cd7f2-148">Typ</span><span class="sxs-lookup"><span data-stu-id="cd7f2-148">Kind</span></span> | <span data-ttu-id="cd7f2-149">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="cd7f2-149">Supported dimension counts</span></span> | <span data-ttu-id="cd7f2-150">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="cd7f2-150">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cd7f2-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cd7f2-151">InputTensor</span></span> | <span data-ttu-id="cd7f2-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd7f2-152">Input</span></span> | <span data-ttu-id="cd7f2-153">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="cd7f2-153">1 to 8</span></span> | <span data-ttu-id="cd7f2-154">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="cd7f2-154">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="cd7f2-155">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cd7f2-155">OutputTensor</span></span> | <span data-ttu-id="cd7f2-156">Output</span><span class="sxs-lookup"><span data-stu-id="cd7f2-156">Output</span></span> | <span data-ttu-id="cd7f2-157">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="cd7f2-157">1 to 8</span></span> | <span data-ttu-id="cd7f2-158">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="cd7f2-158">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="cd7f2-159">DML_FEATURE_LEVEL_3_1 und höher</span><span class="sxs-lookup"><span data-stu-id="cd7f2-159">DML_FEATURE_LEVEL_3_1 and above</span></span>
| <span data-ttu-id="cd7f2-160">Tensor</span><span class="sxs-lookup"><span data-stu-id="cd7f2-160">Tensor</span></span> | <span data-ttu-id="cd7f2-161">Typ</span><span class="sxs-lookup"><span data-stu-id="cd7f2-161">Kind</span></span> | <span data-ttu-id="cd7f2-162">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="cd7f2-162">Supported dimension counts</span></span> | <span data-ttu-id="cd7f2-163">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="cd7f2-163">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cd7f2-164">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cd7f2-164">InputTensor</span></span> | <span data-ttu-id="cd7f2-165">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd7f2-165">Input</span></span> | <span data-ttu-id="cd7f2-166">4</span><span class="sxs-lookup"><span data-stu-id="cd7f2-166">4</span></span> | <span data-ttu-id="cd7f2-167">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="cd7f2-167">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="cd7f2-168">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cd7f2-168">OutputTensor</span></span> | <span data-ttu-id="cd7f2-169">Output</span><span class="sxs-lookup"><span data-stu-id="cd7f2-169">Output</span></span> | <span data-ttu-id="cd7f2-170">4</span><span class="sxs-lookup"><span data-stu-id="cd7f2-170">4</span></span> | <span data-ttu-id="cd7f2-171">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="cd7f2-171">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="cd7f2-172">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cd7f2-172">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cd7f2-173">**Header**</span><span class="sxs-lookup"><span data-stu-id="cd7f2-173">**Header**</span></span> | <span data-ttu-id="cd7f2-174">directml.h</span><span class="sxs-lookup"><span data-stu-id="cd7f2-174">directml.h</span></span> |