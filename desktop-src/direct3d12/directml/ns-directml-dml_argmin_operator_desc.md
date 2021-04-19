---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Gibt die Indizes der minimal wertigen Elemente innerhalb einer oder mehrerer Dimensionen des Eingabe Mandanten aus.
helpviewer_keywords:
- DML_ARGMIN_OPERATOR_DESC
- DML_ARGMIN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMIN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMIN_OPERATOR_DESC, DML_ARGMIN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
- directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
ms.openlocfilehash: 30d281c6ab35675e0cfce80b7eb025292c501041
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106367261"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a><span data-ttu-id="26baa-103">DML_ARGMIN_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="26baa-103">DML_ARGMIN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="26baa-104">Gibt die Indizes der minimal wertigen Elemente innerhalb einer oder mehrerer Dimensionen des Eingabe Mandanten aus.</span><span class="sxs-lookup"><span data-stu-id="26baa-104">Outputs the indices of the minimum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="26baa-105">Jedes Output-Element ist das Ergebnis der Anwendung einer *argmin* -Reduzierung auf eine Teilmenge des eingabetensors.</span><span class="sxs-lookup"><span data-stu-id="26baa-105">Each output element is the result of applying an *argmin* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="26baa-106">Die *argmin* -Funktion gibt den Index des Minimalwert Elements innerhalb eines Satzes von Eingabe Elementen aus.</span><span class="sxs-lookup"><span data-stu-id="26baa-106">The *argmin* function outputs the index of the minimum-valued element within a set of input elements.</span></span> <span data-ttu-id="26baa-107">Die Eingabeelemente, die an jeder Reduzierung beteiligt sind, werden durch die bereitgestellten Eingabe Achsen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="26baa-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="26baa-108">Ebenso ist jeder Ausgabe Index in Bezug auf die bereitgestellten Eingabe Achsen.</span><span class="sxs-lookup"><span data-stu-id="26baa-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="26baa-109">Wenn alle Eingabe Achsen angegeben sind, wendet der Operator eine einzelne *argmin* -Reduzierung an und erzeugt ein einzelnes Output-Element.</span><span class="sxs-lookup"><span data-stu-id="26baa-109">If all input axes are specified, then the operator applies a single *argmin* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26baa-110">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="26baa-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="26baa-111">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="26baa-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="26baa-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="26baa-112">Syntax</span></span>
```cpp
struct DML_ARGMIN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="26baa-113">Member</span><span class="sxs-lookup"><span data-stu-id="26baa-113">Members</span></span>

`InputTensor`

<span data-ttu-id="26baa-114">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="26baa-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="26baa-115">Der zu lesende tensorflow.</span><span class="sxs-lookup"><span data-stu-id="26baa-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="26baa-116">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="26baa-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="26baa-117">Der tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26baa-117">The tensor to write the results to.</span></span> <span data-ttu-id="26baa-118">Jedes Output-Element ist das Ergebnis einer *argmin* -Reduzierung für eine Teilmenge von Elementen aus dem *inputtensor*.</span><span class="sxs-lookup"><span data-stu-id="26baa-118">Each output element is the result of an *argmin* reduction on a subset of elements from the *InputTensor*.</span></span>

- <span data-ttu-id="26baa-119">*DimensionCount* muss mit *inputtensor. DimensionCount* (der Rang des Eingabe Mandanten beibehalten) identisch sein.</span><span class="sxs-lookup"><span data-stu-id="26baa-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="26baa-120">*Größen* müssen mit " *inputtensor. sizes*" verglichen werden, mit Ausnahme der Dimensionen, die in den reduzierten *Achsen* enthalten sind, die die Größe 1 aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="26baa-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="26baa-121">Typ: **[uint](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="26baa-121">Type: **[UINT](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="26baa-122">Die Anzahl der zu reduzierenden Achsen.</span><span class="sxs-lookup"><span data-stu-id="26baa-122">The number of axes to reduce.</span></span> <span data-ttu-id="26baa-123">Dieses Feld bestimmt die Größe des *Achsen* Arrays.</span><span class="sxs-lookup"><span data-stu-id="26baa-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="26baa-124">Typ: \_ Field_size \_ (axiscount) **Konstanten [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="26baa-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="26baa-125">Die Achsen, auf die reduziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="26baa-125">The axes along which to reduce.</span></span> <span data-ttu-id="26baa-126">Die Werte müssen im Bereich liegen `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="26baa-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="26baa-127">DML_AXIS_DIRECTION axisdirection;</span><span class="sxs-lookup"><span data-stu-id="26baa-127">DML_AXIS_DIRECTION AxisDirection;</span></span>

<span data-ttu-id="26baa-128">Typ: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="26baa-128">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="26baa-129">Bestimmt, welcher Index ausgewählt werden soll, wenn mehrere Eingabeelemente denselben Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="26baa-129">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="26baa-130">**DML_AXIS_DIRECTION_INCREASING** gibt den Index des ersten Elements mit dem Minimalwert zurück (z. b. `argmin({1,2,3,2,1}) = 0` ).</span><span class="sxs-lookup"><span data-stu-id="26baa-130">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first minimum-valued element (for example, `argmin({1,2,3,2,1}) = 0`)</span></span>
- <span data-ttu-id="26baa-131">**DML_AXIS_DIRECTION_DECREASING** gibt den Index des letzten Minimalwert Elements zurück (z. b. `argmin({1,2,3,2,1}) = 4` ).</span><span class="sxs-lookup"><span data-stu-id="26baa-131">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last minimum-valued element (for example, `argmin({1,2,3,2,1}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="26baa-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26baa-132">Examples</span></span>

<span data-ttu-id="26baa-133">In den Beispielen in diesem Abschnitt wird der gleiche zweidimensionale Eingabe Mandanten verwendet.</span><span class="sxs-lookup"><span data-stu-id="26baa-133">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a><span data-ttu-id="26baa-134">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="26baa-134">Example 1.</span></span> <span data-ttu-id="26baa-135">Anwenden von *argmin* auf Spalten</span><span class="sxs-lookup"><span data-stu-id="26baa-135">Applying *argmin* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a><span data-ttu-id="26baa-136">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="26baa-136">Example 2.</span></span> <span data-ttu-id="26baa-137">Anwenden von *argmin* auf Zeilen</span><span class="sxs-lookup"><span data-stu-id="26baa-137">Applying *argmin* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a><span data-ttu-id="26baa-138">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="26baa-138">Example 3.</span></span> <span data-ttu-id="26baa-139">Anwenden von *argmin* auf alle Achsen (der gesamte Tensor)</span><span class="sxs-lookup"><span data-stu-id="26baa-139">Applying *argmin* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="26baa-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26baa-140">Remarks</span></span>
<span data-ttu-id="26baa-141">Die Ausgabe Mandanten Größen müssen mit den Eingabe-tensorflow-Größen identisch sein, mit Ausnahme der reduzierten Achsen, die 1 sein müssen.</span><span class="sxs-lookup"><span data-stu-id="26baa-141">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="26baa-142">Wenn *axisdirection* [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction)ist, entspricht diese API [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) mit [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="26baa-142">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="26baa-143">Eine Teilmenge dieser Funktionalität wird durch den [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) -Operator verfügbar gemacht und auf früheren directml-featureebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="26baa-143">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="26baa-144">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="26baa-144">Availability</span></span>
<span data-ttu-id="26baa-145">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="26baa-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="26baa-146">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="26baa-146">Tensor constraints</span></span>
<span data-ttu-id="26baa-147">*Inputtensor* und *outputtensor* müssen dieselbe *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="26baa-147">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="26baa-148">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="26baa-148">Tensor support</span></span>
| <span data-ttu-id="26baa-149">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="26baa-149">Tensor</span></span> | <span data-ttu-id="26baa-150">Typ</span><span class="sxs-lookup"><span data-stu-id="26baa-150">Kind</span></span> | <span data-ttu-id="26baa-151">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="26baa-151">Supported dimension counts</span></span> | <span data-ttu-id="26baa-152">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="26baa-152">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="26baa-153">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="26baa-153">InputTensor</span></span> | <span data-ttu-id="26baa-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="26baa-154">Input</span></span> | <span data-ttu-id="26baa-155">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="26baa-155">1 to 8</span></span> | <span data-ttu-id="26baa-156">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="26baa-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="26baa-157">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="26baa-157">OutputTensor</span></span> | <span data-ttu-id="26baa-158">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="26baa-158">Output</span></span> | <span data-ttu-id="26baa-159">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="26baa-159">1 to 8</span></span> | <span data-ttu-id="26baa-160">Int64, Int32, UINT64, UInt32</span><span class="sxs-lookup"><span data-stu-id="26baa-160">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="26baa-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26baa-161">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="26baa-162">**Header**</span><span class="sxs-lookup"><span data-stu-id="26baa-162">**Header**</span></span> | <span data-ttu-id="26baa-163">directml. h</span><span class="sxs-lookup"><span data-stu-id="26baa-163">directml.h</span></span> |