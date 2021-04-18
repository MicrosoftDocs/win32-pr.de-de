---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Gibt die Indizes der maximal wertigen Elemente innerhalb einer oder mehrerer Dimensionen des Eingabe Mandanten aus.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 17ccadc1228ea833ea1f1b3235e97430ac000514
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106354895"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a><span data-ttu-id="76c9e-103">DML_ARGMAX_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="76c9e-103">DML_ARGMAX_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="76c9e-104">Gibt die Indizes der maximal wertigen Elemente innerhalb einer oder mehrerer Dimensionen des Eingabe Mandanten aus.</span><span class="sxs-lookup"><span data-stu-id="76c9e-104">Outputs the indices of the maximum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="76c9e-105">Jedes Output-Element ist das Ergebnis der Anwendung einer *argmax* -Reduzierung auf eine Teilmenge des eingabetensors.</span><span class="sxs-lookup"><span data-stu-id="76c9e-105">Each output element is the result of applying an *argmax* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="76c9e-106">Die *argmax* -Funktion gibt den Index des Maximalwert Elements innerhalb eines Satzes von Eingabe Elementen aus.</span><span class="sxs-lookup"><span data-stu-id="76c9e-106">The *argmax* function outputs the index of the maximum-valued element within a set of input elements.</span></span> <span data-ttu-id="76c9e-107">Die Eingabeelemente, die an jeder Reduzierung beteiligt sind, werden durch die bereitgestellten Eingabe Achsen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="76c9e-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="76c9e-108">Ebenso ist jeder Ausgabe Index in Bezug auf die bereitgestellten Eingabe Achsen.</span><span class="sxs-lookup"><span data-stu-id="76c9e-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="76c9e-109">Wenn alle Eingabe Achsen angegeben sind, wendet der Operator eine einzelne *argmax* -Reduzierung an und erzeugt ein einzelnes Output-Element.</span><span class="sxs-lookup"><span data-stu-id="76c9e-109">If all input axes are specified, then the operator applies a single *argmax* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76c9e-110">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="76c9e-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="76c9e-111">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="76c9e-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="76c9e-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="76c9e-112">Syntax</span></span>
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="76c9e-113">Member</span><span class="sxs-lookup"><span data-stu-id="76c9e-113">Members</span></span>

`InputTensor`

<span data-ttu-id="76c9e-114">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76c9e-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76c9e-115">Der zu lesende tensorflow.</span><span class="sxs-lookup"><span data-stu-id="76c9e-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="76c9e-116">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76c9e-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76c9e-117">Der tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76c9e-117">The tensor to write the results to.</span></span> <span data-ttu-id="76c9e-118">Jedes Output-Element ist das Ergebnis einer *argmax* -Reduzierung für eine Teilmenge von Elementen aus dem *inputtensor*.</span><span class="sxs-lookup"><span data-stu-id="76c9e-118">Each output element is the result of an *argmax* reduction on a subset of elements from the *InputTensor*.</span></span> 

- <span data-ttu-id="76c9e-119">*DimensionCount* muss mit *inputtensor. DimensionCount* (der Rang des Eingabe Mandanten beibehalten) identisch sein.</span><span class="sxs-lookup"><span data-stu-id="76c9e-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="76c9e-120">*Größen* müssen mit " *inputtensor. sizes*" verglichen werden, mit Ausnahme der Dimensionen, die in den reduzierten *Achsen* enthalten sind, die die Größe 1 aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="76c9e-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="76c9e-121">Typ: **[uint](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76c9e-121">Type: **[UINT](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="76c9e-122">Die Anzahl der zu reduzierenden Achsen.</span><span class="sxs-lookup"><span data-stu-id="76c9e-122">The number of axes to reduce.</span></span> <span data-ttu-id="76c9e-123">Dieses Feld bestimmt die Größe des *Achsen* Arrays.</span><span class="sxs-lookup"><span data-stu-id="76c9e-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="76c9e-124">Typ: \_ Field_size \_ (axiscount) **Konstanten [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="76c9e-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="76c9e-125">Die Achsen, auf die reduziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="76c9e-125">The axes along which to reduce.</span></span> <span data-ttu-id="76c9e-126">Die Werte müssen im Bereich liegen `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="76c9e-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="76c9e-127">Typ: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="76c9e-127">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="76c9e-128">Bestimmt, welcher Index ausgewählt werden soll, wenn mehrere Eingabeelemente denselben Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="76c9e-128">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="76c9e-129">**DML_AXIS_DIRECTION_INCREASING** gibt den Index des ersten Maximalwert Elements (z. b.) zurück. `argmax({3,2,1,2,3}) = 0`</span><span class="sxs-lookup"><span data-stu-id="76c9e-129">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first maximum-valued element (for example, `argmax({3,2,1,2,3}) = 0`)</span></span>
- <span data-ttu-id="76c9e-130">**DML_AXIS_DIRECTION_DECREASING** gibt den Index des letzten Maximalwert Elements zurück (z. b. `argmax({3,2,1,2,3}) = 4` ).</span><span class="sxs-lookup"><span data-stu-id="76c9e-130">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last maximum-valued element (for example, `argmax({3,2,1,2,3}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="76c9e-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76c9e-131">Examples</span></span>

<span data-ttu-id="76c9e-132">In den Beispielen in diesem Abschnitt wird der gleiche zweidimensionale Eingabe Mandanten verwendet.</span><span class="sxs-lookup"><span data-stu-id="76c9e-132">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a><span data-ttu-id="76c9e-133">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="76c9e-133">Example 1.</span></span> <span data-ttu-id="76c9e-134">Anwenden von *argmax* auf Spalten</span><span class="sxs-lookup"><span data-stu-id="76c9e-134">Applying *argmax* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a><span data-ttu-id="76c9e-135">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="76c9e-135">Example 2.</span></span> <span data-ttu-id="76c9e-136">Anwenden von *argmax* auf Zeilen</span><span class="sxs-lookup"><span data-stu-id="76c9e-136">Applying *argmax* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a><span data-ttu-id="76c9e-137">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="76c9e-137">Example 3.</span></span> <span data-ttu-id="76c9e-138">Anwenden von *argmax* auf alle Achsen (der gesamte Tensor)</span><span class="sxs-lookup"><span data-stu-id="76c9e-138">Applying *argmax* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="76c9e-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76c9e-139">Remarks</span></span>
<span data-ttu-id="76c9e-140">Die Ausgabe Mandanten Größen müssen mit den Eingabe-tensorflow-Größen identisch sein, mit Ausnahme der reduzierten Achsen, die 1 sein müssen.</span><span class="sxs-lookup"><span data-stu-id="76c9e-140">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="76c9e-141">Wenn *axisdirection* [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction)ist, entspricht diese API [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) mit [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="76c9e-141">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="76c9e-142">Eine Teilmenge dieser Funktionalität wird durch den [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) -Operator verfügbar gemacht und auf früheren directml-featureebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76c9e-142">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="76c9e-143">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="76c9e-143">Availability</span></span>
<span data-ttu-id="76c9e-144">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="76c9e-144">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="76c9e-145">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="76c9e-145">Tensor constraints</span></span>
<span data-ttu-id="76c9e-146">*Inputtensor* und *outputtensor* müssen dieselbe *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="76c9e-146">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="76c9e-147">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="76c9e-147">Tensor support</span></span>
| <span data-ttu-id="76c9e-148">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="76c9e-148">Tensor</span></span> | <span data-ttu-id="76c9e-149">Typ</span><span class="sxs-lookup"><span data-stu-id="76c9e-149">Kind</span></span> | <span data-ttu-id="76c9e-150">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="76c9e-150">Supported dimension counts</span></span> | <span data-ttu-id="76c9e-151">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="76c9e-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="76c9e-152">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="76c9e-152">InputTensor</span></span> | <span data-ttu-id="76c9e-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="76c9e-153">Input</span></span> | <span data-ttu-id="76c9e-154">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="76c9e-154">1 to 8</span></span> | <span data-ttu-id="76c9e-155">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="76c9e-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="76c9e-156">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="76c9e-156">OutputTensor</span></span> | <span data-ttu-id="76c9e-157">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="76c9e-157">Output</span></span> | <span data-ttu-id="76c9e-158">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="76c9e-158">1 to 8</span></span> | <span data-ttu-id="76c9e-159">Int64, Int32, UINT64, UInt32</span><span class="sxs-lookup"><span data-stu-id="76c9e-159">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="76c9e-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76c9e-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="76c9e-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="76c9e-161">**Header**</span></span> | <span data-ttu-id="76c9e-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="76c9e-162">directml.h</span></span> |