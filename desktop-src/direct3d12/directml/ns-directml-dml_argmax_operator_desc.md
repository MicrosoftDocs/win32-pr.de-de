---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Gibt die Indizes der Höchstwertelemente innerhalb einer oder mehrerer Dimensionen des Eingabe-Tensors aus.
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
ms.openlocfilehash: 4c2852c3d301a12d318c5e3006b26830c6eaa6e1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417775"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a><span data-ttu-id="bae74-103">DML_ARGMAX_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="bae74-103">DML_ARGMAX_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="bae74-104">Gibt die Indizes der Höchstwertelemente innerhalb einer oder mehrerer Dimensionen des Eingabe-Tensors aus.</span><span class="sxs-lookup"><span data-stu-id="bae74-104">Outputs the indices of the maximum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="bae74-105">Jedes Ausgabeelement ist das Ergebnis der Anwendung einer *argmax-Reduzierung* auf eine Teilmenge des Eingabe-Tensors.</span><span class="sxs-lookup"><span data-stu-id="bae74-105">Each output element is the result of applying an *argmax* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="bae74-106">Die *argmax-Funktion* gibt den Index des Höchstwertelements innerhalb eines Satzes von Eingabeelementen aus.</span><span class="sxs-lookup"><span data-stu-id="bae74-106">The *argmax* function outputs the index of the maximum-valued element within a set of input elements.</span></span> <span data-ttu-id="bae74-107">Die Eingabeelemente, die an jeder Reduzierung beteiligt sind, werden durch die bereitgestellten Eingabeachsen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="bae74-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="bae74-108">Auf ähnliche Weise ist jeder Ausgabeindex in Bezug auf die bereitgestellten Eingabeachsen.</span><span class="sxs-lookup"><span data-stu-id="bae74-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="bae74-109">Wenn alle Eingabeachsen angegeben sind, wendet der Operator eine einzelne *Argmax-Reduzierung* an und erzeugt ein einzelnes Ausgabeelement.</span><span class="sxs-lookup"><span data-stu-id="bae74-109">If all input axes are specified, then the operator applies a single *argmax* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bae74-110">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="bae74-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="bae74-111">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="bae74-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bae74-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="bae74-112">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="bae74-113">Member</span><span class="sxs-lookup"><span data-stu-id="bae74-113">Members</span></span>

`InputTensor`

<span data-ttu-id="bae74-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bae74-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bae74-115">Der Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bae74-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="bae74-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bae74-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bae74-117">Der Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bae74-117">The tensor to write the results to.</span></span> <span data-ttu-id="bae74-118">Jedes Ausgabeelement ist das Ergebnis einer *Argmax-Reduzierung* für eine Teilmenge von Elementen aus dem *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="bae74-118">Each output element is the result of an *argmax* reduction on a subset of elements from the *InputTensor*.</span></span> 

- <span data-ttu-id="bae74-119">*DimensionCount* muss *mit InputTensor.DimensionCount* übereinstimmen (der Rang des Eingabe-Tensors wird beibehalten).</span><span class="sxs-lookup"><span data-stu-id="bae74-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="bae74-120">*Größen* müssen mit *InputTensor.Sizes* übereinstimmen, mit Ausnahme von Dimensionen, die in den *reduzierten Achsen* enthalten sind, die Größe 1 aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="bae74-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="bae74-121">Typ: **[UINT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae74-121">Type: **[UINT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bae74-122">Die Anzahl der zu reduzierende Achsen.</span><span class="sxs-lookup"><span data-stu-id="bae74-122">The number of axes to reduce.</span></span> <span data-ttu-id="bae74-123">Dieses Feld bestimmt die Größe des *Axes-Arrays.*</span><span class="sxs-lookup"><span data-stu-id="bae74-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="bae74-124">Typ: \_ Field_size \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="bae74-124">Type: \_Field_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bae74-125">Die Achsen, entlang derer reduziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bae74-125">The axes along which to reduce.</span></span> <span data-ttu-id="bae74-126">Werte müssen im Bereich `[0, InputTensor.DimensionCount - 1]` liegen.</span><span class="sxs-lookup"><span data-stu-id="bae74-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="bae74-127">Typ: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="bae74-127">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="bae74-128">Bestimmt, welcher Index ausgewählt werden soll, wenn mehrere Eingabeelemente denselben Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bae74-128">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="bae74-129">**DML_AXIS_DIRECTION_INCREASING** gibt den Index des ersten Höchstwertelements zurück (z. B. `argmax({3,2,1,2,3}) = 0` ).</span><span class="sxs-lookup"><span data-stu-id="bae74-129">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first maximum-valued element (for example, `argmax({3,2,1,2,3}) = 0`)</span></span>
- <span data-ttu-id="bae74-130">**DML_AXIS_DIRECTION_DECREASING** gibt den Index des letzten Höchstwertelements zurück (z. B. `argmax({3,2,1,2,3}) = 4` ).</span><span class="sxs-lookup"><span data-stu-id="bae74-130">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last maximum-valued element (for example, `argmax({3,2,1,2,3}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="bae74-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bae74-131">Examples</span></span>

<span data-ttu-id="bae74-132">In den Beispielen in diesem Abschnitt wird der gleiche zweidimensionale Eingabe-Tensor verwendet.</span><span class="sxs-lookup"><span data-stu-id="bae74-132">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a><span data-ttu-id="bae74-133">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="bae74-133">Example 1.</span></span> <span data-ttu-id="bae74-134">Anwenden von *argmax* auf Spalten</span><span class="sxs-lookup"><span data-stu-id="bae74-134">Applying *argmax* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a><span data-ttu-id="bae74-135">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="bae74-135">Example 2.</span></span> <span data-ttu-id="bae74-136">Anwenden von *argmax* auf Zeilen</span><span class="sxs-lookup"><span data-stu-id="bae74-136">Applying *argmax* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a><span data-ttu-id="bae74-137">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="bae74-137">Example 3.</span></span> <span data-ttu-id="bae74-138">Anwenden von *argmax* auf alle Achsen (den gesamten Tensor)</span><span class="sxs-lookup"><span data-stu-id="bae74-138">Applying *argmax* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="bae74-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bae74-139">Remarks</span></span>
<span data-ttu-id="bae74-140">Die Ausgabe-Tensorgrößen müssen mit den Eingabe-Tensorgrößen identisch sein, mit Ausnahme der reduzierten Achsen, die 1 sein müssen.</span><span class="sxs-lookup"><span data-stu-id="bae74-140">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="bae74-141">Wenn *AxisDirection* [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction)ist, entspricht diese API [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) mit [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="bae74-141">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="bae74-142">Eine Teilmenge dieser Funktionalität wird über den [operator DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) verfügbar gemacht und auf früheren DirectML-Featureebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bae74-142">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="bae74-143">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="bae74-143">Availability</span></span>
<span data-ttu-id="bae74-144">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bae74-144">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="bae74-145">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="bae74-145">Tensor constraints</span></span>
<span data-ttu-id="bae74-146">*InputTensor* und *OutputTensor* müssen über den gleichen *DimensionCount verfügen.*</span><span class="sxs-lookup"><span data-stu-id="bae74-146">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="bae74-147">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="bae74-147">Tensor support</span></span>
| <span data-ttu-id="bae74-148">Tensor</span><span class="sxs-lookup"><span data-stu-id="bae74-148">Tensor</span></span> | <span data-ttu-id="bae74-149">Typ</span><span class="sxs-lookup"><span data-stu-id="bae74-149">Kind</span></span> | <span data-ttu-id="bae74-150">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="bae74-150">Supported dimension counts</span></span> | <span data-ttu-id="bae74-151">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="bae74-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bae74-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="bae74-152">InputTensor</span></span> | <span data-ttu-id="bae74-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bae74-153">Input</span></span> | <span data-ttu-id="bae74-154">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="bae74-154">1 to 8</span></span> | <span data-ttu-id="bae74-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bae74-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bae74-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="bae74-156">OutputTensor</span></span> | <span data-ttu-id="bae74-157">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="bae74-157">Output</span></span> | <span data-ttu-id="bae74-158">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="bae74-158">1 to 8</span></span> | <span data-ttu-id="bae74-159">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="bae74-159">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="bae74-160">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bae74-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bae74-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="bae74-161">**Header**</span></span> | <span data-ttu-id="bae74-162">directml.h</span><span class="sxs-lookup"><span data-stu-id="bae74-162">directml.h</span></span> |