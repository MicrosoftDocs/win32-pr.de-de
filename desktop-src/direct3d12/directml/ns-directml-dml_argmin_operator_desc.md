---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Gibt die Indizes der Minimalwertelemente innerhalb einer oder mehrere Dimensionen des Eingabetensors aus.
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
ms.openlocfilehash: da270ea5354e361067335ba1c789efe18310437a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550475"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a><span data-ttu-id="afa22-103">DML_ARGMIN_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="afa22-103">DML_ARGMIN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="afa22-104">Gibt die Indizes der Minimalwertelemente innerhalb einer oder mehrere Dimensionen des Eingabetensors aus.</span><span class="sxs-lookup"><span data-stu-id="afa22-104">Outputs the indices of the minimum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="afa22-105">Jedes Ausgabeelement ist das Ergebnis der Anwendung einer *Argminverringerung* auf eine Teilmenge des Eingabetensors.</span><span class="sxs-lookup"><span data-stu-id="afa22-105">Each output element is the result of applying an *argmin* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="afa22-106">Die *argmin-Funktion* gibt den Index des Minimalwertelements in einem Satz von Eingabeelementen aus.</span><span class="sxs-lookup"><span data-stu-id="afa22-106">The *argmin* function outputs the index of the minimum-valued element within a set of input elements.</span></span> <span data-ttu-id="afa22-107">Die an jeder Reduzierung beteiligten Eingabeelemente werden durch die bereitgestellten Eingabeachsen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="afa22-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="afa22-108">Ebenso gilt jeder Ausgabeindex in Bezug auf die bereitgestellten Eingabeachsen.</span><span class="sxs-lookup"><span data-stu-id="afa22-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="afa22-109">Wenn alle Eingabeachsen angegeben sind, wendet der Operator eine einzelne *Argminverringerung* an und erzeugt ein einzelnes Ausgabeelement.</span><span class="sxs-lookup"><span data-stu-id="afa22-109">If all input axes are specified, then the operator applies a single *argmin* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="afa22-110">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="afa22-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="afa22-111">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="afa22-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="afa22-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="afa22-112">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="afa22-113">Member</span><span class="sxs-lookup"><span data-stu-id="afa22-113">Members</span></span>

`InputTensor`

<span data-ttu-id="afa22-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="afa22-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="afa22-115">Der Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="afa22-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="afa22-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="afa22-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="afa22-117">Der Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="afa22-117">The tensor to write the results to.</span></span> <span data-ttu-id="afa22-118">Jedes Ausgabeelement ist das Ergebnis einer *Argminreduzierung* für eine Teilmenge von Elementen aus *dem InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="afa22-118">Each output element is the result of an *argmin* reduction on a subset of elements from the *InputTensor*.</span></span>

- <span data-ttu-id="afa22-119">*DimensionCount* muss mit *InputTensor.DimensionCount übereinstimmen* (der Rang des Eingabetensors wird beibehalten).</span><span class="sxs-lookup"><span data-stu-id="afa22-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="afa22-120">*Größen müssen* mit *InputTensor.Sizes übereinstimmen,* mit Ausnahme der Dimensionen, die in den reduzierten Achsen enthalten *sind,* die die Größe 1 haben müssen.</span><span class="sxs-lookup"><span data-stu-id="afa22-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="afa22-121">Typ: **[UINT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="afa22-121">Type: **[UINT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="afa22-122">Die Anzahl der zu reduzierenden Achsen.</span><span class="sxs-lookup"><span data-stu-id="afa22-122">The number of axes to reduce.</span></span> <span data-ttu-id="afa22-123">Dieses Feld bestimmt die Größe des *Achsenarrays.*</span><span class="sxs-lookup"><span data-stu-id="afa22-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="afa22-124">Typ: \_ Field_size \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="afa22-124">Type: \_Field_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="afa22-125">Die Achsen, entlang derer reduziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="afa22-125">The axes along which to reduce.</span></span> <span data-ttu-id="afa22-126">Werte müssen im Bereich `[0, InputTensor.DimensionCount - 1]` liegen.</span><span class="sxs-lookup"><span data-stu-id="afa22-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="afa22-127">DML_AXIS_DIRECTION AxisDirection;</span><span class="sxs-lookup"><span data-stu-id="afa22-127">DML_AXIS_DIRECTION AxisDirection;</span></span>

<span data-ttu-id="afa22-128">Typ: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="afa22-128">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="afa22-129">Bestimmt, welcher Index ausgewählt werden soll, wenn mehrere Eingabeelemente denselben Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="afa22-129">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="afa22-130">**DML_AXIS_DIRECTION_INCREASING** gibt den Index des ersten Mindestwertelements zurück (z. B. `argmin({1,2,3,2,1}) = 0` ).</span><span class="sxs-lookup"><span data-stu-id="afa22-130">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first minimum-valued element (for example, `argmin({1,2,3,2,1}) = 0`)</span></span>
- <span data-ttu-id="afa22-131">**DML_AXIS_DIRECTION_DECREASING** gibt den Index des letzten Mindestwertelements zurück (z. B. `argmin({1,2,3,2,1}) = 4` ).</span><span class="sxs-lookup"><span data-stu-id="afa22-131">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last minimum-valued element (for example, `argmin({1,2,3,2,1}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="afa22-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afa22-132">Examples</span></span>

<span data-ttu-id="afa22-133">In den Beispielen in diesem Abschnitt wird der gleiche zweidimensionale Eingabe-Tensor verwendet.</span><span class="sxs-lookup"><span data-stu-id="afa22-133">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a><span data-ttu-id="afa22-134">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="afa22-134">Example 1.</span></span> <span data-ttu-id="afa22-135">Anwenden von *Argmin* auf Spalten</span><span class="sxs-lookup"><span data-stu-id="afa22-135">Applying *argmin* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a><span data-ttu-id="afa22-136">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="afa22-136">Example 2.</span></span> <span data-ttu-id="afa22-137">Anwenden von *Argmin* auf Zeilen</span><span class="sxs-lookup"><span data-stu-id="afa22-137">Applying *argmin* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a><span data-ttu-id="afa22-138">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="afa22-138">Example 3.</span></span> <span data-ttu-id="afa22-139">Anwenden von *Argmin* auf alle Achsen (den gesamten Tensor)</span><span class="sxs-lookup"><span data-stu-id="afa22-139">Applying *argmin* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="afa22-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="afa22-140">Remarks</span></span>
<span data-ttu-id="afa22-141">Die Ausgabe-Tensorgrößen müssen mit den Eingabe-Tensorgrößen identisch sein, mit Ausnahme der reduzierten Achsen, die 1 sein müssen.</span><span class="sxs-lookup"><span data-stu-id="afa22-141">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="afa22-142">Wenn *AxisDirection* [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction)ist, entspricht diese API [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) mit [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="afa22-142">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="afa22-143">Eine Teilmenge dieser Funktionalität wird über den [operator DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) verfügbar gemacht und auf früheren DirectML-Featureebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="afa22-143">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="afa22-144">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="afa22-144">Availability</span></span>
<span data-ttu-id="afa22-145">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="afa22-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="afa22-146">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="afa22-146">Tensor constraints</span></span>
<span data-ttu-id="afa22-147">*InputTensor* und *OutputTensor* müssen über den gleichen *DimensionCount verfügen.*</span><span class="sxs-lookup"><span data-stu-id="afa22-147">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="afa22-148">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="afa22-148">Tensor support</span></span>
| <span data-ttu-id="afa22-149">Tensor</span><span class="sxs-lookup"><span data-stu-id="afa22-149">Tensor</span></span> | <span data-ttu-id="afa22-150">Typ</span><span class="sxs-lookup"><span data-stu-id="afa22-150">Kind</span></span> | <span data-ttu-id="afa22-151">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="afa22-151">Supported dimension counts</span></span> | <span data-ttu-id="afa22-152">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="afa22-152">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="afa22-153">InputTensor</span><span class="sxs-lookup"><span data-stu-id="afa22-153">InputTensor</span></span> | <span data-ttu-id="afa22-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="afa22-154">Input</span></span> | <span data-ttu-id="afa22-155">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="afa22-155">1 to 8</span></span> | <span data-ttu-id="afa22-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="afa22-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="afa22-157">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="afa22-157">OutputTensor</span></span> | <span data-ttu-id="afa22-158">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="afa22-158">Output</span></span> | <span data-ttu-id="afa22-159">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="afa22-159">1 to 8</span></span> | <span data-ttu-id="afa22-160">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="afa22-160">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="afa22-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afa22-161">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="afa22-162">**Header**</span><span class="sxs-lookup"><span data-stu-id="afa22-162">**Header**</span></span> | <span data-ttu-id="afa22-163">directml.h</span><span class="sxs-lookup"><span data-stu-id="afa22-163">directml.h</span></span> |