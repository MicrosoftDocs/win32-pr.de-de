---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Extrahiert einen einzelnen Unterbereich (einen "Slice") eines Eingabetensors.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: f34525865be9541da879e66e88c29d4a2ab74f00
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803954"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a><span data-ttu-id="12044-103">DML_SLICE1_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="12044-103">DML_SLICE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="12044-104">Extrahiert einen einzelnen Unterbereich (einen "Slice") eines Eingabetensors.</span><span class="sxs-lookup"><span data-stu-id="12044-104">Extracts a single subregion (a "slice") of an input tensor.</span></span>

<span data-ttu-id="12044-105">Das *Eingabefenster* beschreibt die Begrenzungen des Eingabetensors, die im Slice zu berücksichtigen sind.</span><span class="sxs-lookup"><span data-stu-id="12044-105">The *input window* describes the bounds of the input tensor to consider in the slice.</span></span> <span data-ttu-id="12044-106">Das Fenster wird mit drei Werten für jede Dimension definiert.</span><span class="sxs-lookup"><span data-stu-id="12044-106">The window is defined using three values for each dimension.</span></span>

- <span data-ttu-id="12044-107">Der *Offset* markiert den *Anfang des Fensters* in einer Dimension.</span><span class="sxs-lookup"><span data-stu-id="12044-107">The *offset* marks the *beginning of the window* in a dimension.</span></span>
- <span data-ttu-id="12044-108">Die *Größe* markiert den Bereich des Fensters in einer Dimension.</span><span class="sxs-lookup"><span data-stu-id="12044-108">The *size* marks the extent of the window in a dimension.</span></span> <span data-ttu-id="12044-109">Das *Ende des Fensters* in einer Dimension ist `offset + size - 1` .</span><span class="sxs-lookup"><span data-stu-id="12044-109">The *end of the window* in a dimension is `offset + size - 1`.</span></span>
- <span data-ttu-id="12044-110">Der *-Schritt gibt* an, wie die Elemente in einer Dimension durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="12044-110">The *stride* indicates how to traverse the elements in a dimension.</span></span>
  - <span data-ttu-id="12044-111">Die Größe des Schritts gibt an, wie viele Elemente beim Kopieren innerhalb des Fensters voranschritten werden.</span><span class="sxs-lookup"><span data-stu-id="12044-111">The magnitude of the stride indicates how many elements to advance when copying within the window.</span></span>
  - <span data-ttu-id="12044-112">Wenn ein Schritt positiv ist, werden Elemente beginnend am Anfang *des* Fensters in der Dimension kopiert.</span><span class="sxs-lookup"><span data-stu-id="12044-112">If a stride is positive, elements are copied starting at the *beginning* of the window in the dimension.</span></span>
  - <span data-ttu-id="12044-113">Wenn ein Schritt negativ ist, werden Elemente beginnend am *Ende* des Fensters in der Dimension kopiert.</span><span class="sxs-lookup"><span data-stu-id="12044-113">If a stride is negative, elements are copied starting at the *end* of the window in the dimension.</span></span>

<span data-ttu-id="12044-114">Der folgende Pseudocode veranschaulicht, wie Elemente mithilfe des Eingabefensters kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="12044-114">The following pseudo-code illustrates how elements are copied using the input window.</span></span> <span data-ttu-id="12044-115">Beachten Sie, wie Elemente in einer Dimension von Anfang bis Ende mit einem positiven Schritt kopiert und von Ende kopiert werden, um mit einem negativen Schritt zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="12044-115">Note how elements in a dimension are copied from start to end with a positive stride, and copied from end to start with a negative stride.</span></span>

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

<span data-ttu-id="12044-116">Das Eingabefenster darf in einer Dimension nicht leer sein, und das Fenster darf nicht über die Dimensionen des Eingabetensors hinausgehen (lesegefängte Außerhalbgrenzen sind nicht zulässig).</span><span class="sxs-lookup"><span data-stu-id="12044-116">The input window mustn't be empty in any dimension, and the window mustn't extend beyond the dimensions of the input tensor (out-of-bounds reads aren't permitted).</span></span> <span data-ttu-id="12044-117">Die Fenstergröße und -strides begrenzen effektiv die Anzahl der Elemente, die aus jeder Dimension des `i` Eingabetensors kopiert werden können.</span><span class="sxs-lookup"><span data-stu-id="12044-117">The window's size and strides effectively limit the number of elements that may be copied from each dimension `i` of the input tensor.</span></span>

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

<span data-ttu-id="12044-118">Der Ausgabe-Tensor ist nicht erforderlich, um alle erreichbaren Elemente innerhalb des Fensters zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="12044-118">The output tensor isn't required to copy all reachable elements within the window.</span></span> <span data-ttu-id="12044-119">Der Slice ist gültig, solange `1 <= OutputSizes[i] <= MaxCopiedElements[i]` er ist.</span><span class="sxs-lookup"><span data-stu-id="12044-119">The slice is valid so long as `1 <= OutputSizes[i] <= MaxCopiedElements[i]`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12044-120">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="12044-120">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="12044-121">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="12044-121">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="12044-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="12044-122">Syntax</span></span>
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a><span data-ttu-id="12044-123">Member</span><span class="sxs-lookup"><span data-stu-id="12044-123">Members</span></span>

`InputTensor`

<span data-ttu-id="12044-124">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="12044-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="12044-125">Der Tensor, aus dem Slices extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="12044-125">The tensor to extract slices from.</span></span>


`OutputTensor`

<span data-ttu-id="12044-126">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="12044-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="12044-127">Der Tensor, in den die Datenergebnisse in Slices geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="12044-127">The tensor to write the sliced data results to.</span></span>


`DimensionCount`

<span data-ttu-id="12044-128">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="12044-128">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="12044-129">Die Anzahl der Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="12044-129">The number of dimensions.</span></span> <span data-ttu-id="12044-130">Dieses Feld bestimmt die Größe der *Arrays InputWindowOffsets,* *InputWindowSizes* und *InputWindowStrides.*</span><span class="sxs-lookup"><span data-stu-id="12044-130">This field determines the size of the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="12044-131">Dieser Wert muss mit dem *DimensionCount-Wert* der Eingabe- und Ausgabe tensors übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="12044-131">This value must match the *DimensionCount* of the input and output tensors.</span></span> <span data-ttu-id="12044-132">Dieser Wert muss zwischen 1 und 8 liegen, einschließlich ab `DML_FEATURE_LEVEL_3_0` . Frühere Featureebenen erfordern einen Wert von 4 oder 5.</span><span class="sxs-lookup"><span data-stu-id="12044-132">This value must be between 1 and 8, inclusively, starting from `DML_FEATURE_LEVEL_3_0`; earlier feature levels require a value of either 4 or 5.</span></span>


`InputWindowOffsets`

<span data-ttu-id="12044-133">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="12044-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="12044-134">Ein Array, das den Anfang (in Elementen) des Eingabefensters in jeder Dimension enthält.</span><span class="sxs-lookup"><span data-stu-id="12044-134">An array containing the beginning (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="12044-135">Werte im Array müssen die Einschränkung erfüllen. `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="12044-135">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowSizes`

<span data-ttu-id="12044-136">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="12044-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="12044-137">Ein Array, das den Umfang (in Elementen) des Eingabefensters in jeder Dimension enthält.</span><span class="sxs-lookup"><span data-stu-id="12044-137">An array containing the extent (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="12044-138">Werte im Array müssen die Einschränkung erfüllen. `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="12044-138">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowStrides`

<span data-ttu-id="12044-139">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="12044-139">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="12044-140">Ein Array, das den Schritt des Slices entlang jeder Dimension des Eingabe-Tensors in -Elementen enthält.</span><span class="sxs-lookup"><span data-stu-id="12044-140">An array containing the slice's stride along each dimension of the input tensor, in elements.</span></span> <span data-ttu-id="12044-141">Die Größe des Schritts gibt an, wie viele Elemente beim Kopieren innerhalb des Eingabefensters vorankommen sollen.</span><span class="sxs-lookup"><span data-stu-id="12044-141">The magnitude of the stride indicates how many elements to advance when copying within the input window.</span></span> <span data-ttu-id="12044-142">Das Vorzeichen des Schritts bestimmt, ob Elemente beginnend am Anfang des Fensters (positiver Schritt) oder am Ende des Fensters (negativer Schritt) kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="12044-142">The sign of the stride determines if elements are copied starting at the beginning of the window (positive stride) or end of the window (negative stride).</span></span> <span data-ttu-id="12044-143">Strides darf nicht 0 sein.</span><span class="sxs-lookup"><span data-stu-id="12044-143">Strides may not be 0.</span></span>

## <a name="examples"></a><span data-ttu-id="12044-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12044-144">Examples</span></span>

<span data-ttu-id="12044-145">In den folgenden Beispielen wird der gleiche Eingabetensor verwendet.</span><span class="sxs-lookup"><span data-stu-id="12044-145">The following examples use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a><span data-ttu-id="12044-146">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="12044-146">Example 1.</span></span> <span data-ttu-id="12044-147">Strided slice with positive strides (Strided Slice mit positiven Schritten)</span><span class="sxs-lookup"><span data-stu-id="12044-147">Strided slice with positive strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

<span data-ttu-id="12044-148">Die kopierten Elemente werden wie folgt berechnet.</span><span class="sxs-lookup"><span data-stu-id="12044-148">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a><span data-ttu-id="12044-149">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="12044-149">Example 2.</span></span> <span data-ttu-id="12044-150">Strided slice with negative strides (Strided Slice mit negativen Schritten)</span><span class="sxs-lookup"><span data-stu-id="12044-150">Strided slice with negative strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

<span data-ttu-id="12044-151">Denken Sie daran, dass Dimensionen mit negativen Fensterschritten am Ende des Eingabefensters für diese Dimension mit dem Kopieren beginnen. Dies erfolgt durch Hinzufügen `InputWindowSize[i] - 1` zum Fensteroffset.</span><span class="sxs-lookup"><span data-stu-id="12044-151">Recall that dimensions with negative window strides start copying at the end of the input window for that dimension; this is done by adding `InputWindowSize[i] - 1` to the window offset.</span></span> <span data-ttu-id="12044-152">Dimensionen mit einem positiven Schritt beginnen einfach bei `InputWindowOffset[i]` .</span><span class="sxs-lookup"><span data-stu-id="12044-152">Dimensions with a positive stride simply start at `InputWindowOffset[i]`.</span></span>
- <span data-ttu-id="12044-153">Achse 0 `+1` (Fensterschritt) beginnt mit dem Kopieren unter `InputWindowOffsets[0] = 0` .</span><span class="sxs-lookup"><span data-stu-id="12044-153">Axis 0 (`+1` window stride) starts copying at `InputWindowOffsets[0] = 0`.</span></span> 
- <span data-ttu-id="12044-154">Achse 1 `+1` (Fensterschritt) beginnt mit dem Kopieren unter `InputWindowOffsets[1] = 0` .</span><span class="sxs-lookup"><span data-stu-id="12044-154">Axis 1 (`+1` window stride) starts copying at `InputWindowOffsets[1] = 0`.</span></span> 
- <span data-ttu-id="12044-155">Achse 2 `-2` (Fensterschritt) beginnt mit dem Kopieren unter `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` .</span><span class="sxs-lookup"><span data-stu-id="12044-155">Axis 2 (`-2` window stride) starts copying at `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3`.</span></span> 
- <span data-ttu-id="12044-156">Achse 3 ( `+2` Fensterschritt) beginnt mit dem Kopieren unter `InputWindowOffsets[3] = 1` .</span><span class="sxs-lookup"><span data-stu-id="12044-156">Axis 3 (`+2` window stride) starts copying at `InputWindowOffsets[3] = 1`.</span></span> 

<span data-ttu-id="12044-157">Die kopierten Elemente werden wie folgt berechnet.</span><span class="sxs-lookup"><span data-stu-id="12044-157">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a><span data-ttu-id="12044-158">Hinweise</span><span class="sxs-lookup"><span data-stu-id="12044-158">Remarks</span></span>
<span data-ttu-id="12044-159">Dieser Operator ähnelt [der](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc)DML_SLICE_OPERATOR_DESC , unterscheidet sich jedoch auf zwei wichtige Arten.</span><span class="sxs-lookup"><span data-stu-id="12044-159">This operator is similar to [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), but it differs in two important ways.</span></span>

- <span data-ttu-id="12044-160">Slice-Strides können negativ sein, was das Umkehren von Werten entlang von Dimensionen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="12044-160">Slice strides may be negative, which allows reversing values along dimensions.</span></span>
- <span data-ttu-id="12044-161">Die Größen des Eingabefensters sind nicht notwendigerweise mit den Ausgabe tensor-Größen identisch.</span><span class="sxs-lookup"><span data-stu-id="12044-161">The input window sizes are not necessarily the same as the output tensor sizes.</span></span>

## <a name="availability"></a><span data-ttu-id="12044-162">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="12044-162">Availability</span></span>
<span data-ttu-id="12044-163">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="12044-163">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="12044-164">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="12044-164">Tensor constraints</span></span>
<span data-ttu-id="12044-165">*InputTensor und* *OutputTensor* müssen denselben *DataType und* *DimensionCount aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="12044-165">*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="12044-166">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="12044-166">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="12044-167">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="12044-167">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="12044-168">Tensor</span><span class="sxs-lookup"><span data-stu-id="12044-168">Tensor</span></span> | <span data-ttu-id="12044-169">Typ</span><span class="sxs-lookup"><span data-stu-id="12044-169">Kind</span></span> | <span data-ttu-id="12044-170">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="12044-170">Supported dimension counts</span></span> | <span data-ttu-id="12044-171">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="12044-171">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="12044-172">InputTensor</span><span class="sxs-lookup"><span data-stu-id="12044-172">InputTensor</span></span> | <span data-ttu-id="12044-173">Eingabe</span><span class="sxs-lookup"><span data-stu-id="12044-173">Input</span></span> | <span data-ttu-id="12044-174">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="12044-174">1 to 8</span></span> | <span data-ttu-id="12044-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="12044-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="12044-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="12044-176">OutputTensor</span></span> | <span data-ttu-id="12044-177">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="12044-177">Output</span></span> | <span data-ttu-id="12044-178">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="12044-178">1 to 8</span></span> | <span data-ttu-id="12044-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="12044-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="12044-180">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="12044-180">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="12044-181">Tensor</span><span class="sxs-lookup"><span data-stu-id="12044-181">Tensor</span></span> | <span data-ttu-id="12044-182">Typ</span><span class="sxs-lookup"><span data-stu-id="12044-182">Kind</span></span> | <span data-ttu-id="12044-183">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="12044-183">Supported dimension counts</span></span> | <span data-ttu-id="12044-184">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="12044-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="12044-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="12044-185">InputTensor</span></span> | <span data-ttu-id="12044-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="12044-186">Input</span></span> | <span data-ttu-id="12044-187">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="12044-187">4 to 5</span></span> | <span data-ttu-id="12044-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="12044-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="12044-189">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="12044-189">OutputTensor</span></span> | <span data-ttu-id="12044-190">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="12044-190">Output</span></span> | <span data-ttu-id="12044-191">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="12044-191">4 to 5</span></span> | <span data-ttu-id="12044-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="12044-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="12044-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12044-193">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="12044-194">**Header**</span><span class="sxs-lookup"><span data-stu-id="12044-194">**Header**</span></span> | <span data-ttu-id="12044-195">directml.h</span><span class="sxs-lookup"><span data-stu-id="12044-195">directml.h</span></span> |