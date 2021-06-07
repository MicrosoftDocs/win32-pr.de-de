---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Berechnet Backpropagation-Farbverläufe für maximales Pooling (siehe [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 3b0b10fa8ee17c9d06e779c3c990f134bc4ae669
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417242"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="04397-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="04397-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="04397-104">Berechnet Backpropagation-Farbverläufe für maximales Pooling (siehe [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span><span class="sxs-lookup"><span data-stu-id="04397-104">Computes backpropagation gradients for max pooling (see [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span></span>

<span data-ttu-id="04397-105">Stellen Sie sich  eine 2x2-DML_MAX_POOLING2_OPERATOR_DESC ohne Auf padding oder dilations und einen Schritt von 1 vor, der Folgendes ausführt.</span><span class="sxs-lookup"><span data-stu-id="04397-105">Consider a 2x2 **DML_MAX_POOLING2_OPERATOR_DESC** without padding nor dilations and a stride of 1, which performs the following.</span></span>

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

<span data-ttu-id="04397-106">Das größte Element jedes 2x2-Fensters im Eingabetensor erzeugt ein Element der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="04397-106">The largest element of each 2x2 window in the input tensor produces one element of the output.</span></span> <span data-ttu-id="04397-107">Im Folgenden finden Sie ein Beispiel für die Ausgabe von **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, wenn ähnliche Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="04397-107">Below is an example of the output of **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, given similar parameters.</span></span>

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

<span data-ttu-id="04397-108">Tatsächlich verwendet dieser Operator den *InputTensor,* um den Index des größten Elements aus jedem Fenster zu bestimmen, und verteilt die Werte von *InputGradientTensor* basierend auf diesen Indizes an *den OutputGradientTensor.*</span><span class="sxs-lookup"><span data-stu-id="04397-108">In effect, this operator uses the *InputTensor* to determine the index of the largest element from each window, and distributes the values of *InputGradientTensor* into the *OutputGradientTensor* based on these indices.</span></span> <span data-ttu-id="04397-109">Wenn sich Indizes überschneiden, werden die Werte summiert.</span><span class="sxs-lookup"><span data-stu-id="04397-109">Where indices overlap, the values are summed.</span></span> <span data-ttu-id="04397-110">Alle Nichtreferenzierungsausgabeelemente werden auf 0 (null) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="04397-110">Any unreferenced output elements are zeroed.</span></span>

<span data-ttu-id="04397-111">Im Fall einer Gleichstandszahl (bei der mehr als ein Element in einem Fenster den gleichen Maximalwert hat) wird das Element mit dem niedrigsten logischen Elementindex ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="04397-111">In the case of a tie (where more than one element in a window has the same maximum value), the element with the lowest logical element index is chosen.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04397-112">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="04397-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="04397-113">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="04397-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="04397-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="04397-114">Syntax</span></span>

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a><span data-ttu-id="04397-115">Member</span><span class="sxs-lookup"><span data-stu-id="04397-115">Members</span></span>

`InputTensor`

<span data-ttu-id="04397-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04397-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04397-117">Der Eingabefunktions-Tensor.</span><span class="sxs-lookup"><span data-stu-id="04397-117">The input feature tensor.</span></span> <span data-ttu-id="04397-118">Dies ist in der Regel der gleiche Tensor, der als *InputTensor* bereitgestellt wurde, um DML_MAX_POOLING2_OPERATOR_DESC [vorwärts](./ns-directml-dml_max_pooling2_operator_desc.md) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="04397-118">This is typically the same tensor that was provided as the *InputTensor* to [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="04397-119">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04397-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04397-120">Der eingehende Farbverlaufs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="04397-120">The incoming gradient tensor.</span></span> <span data-ttu-id="04397-121">Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorherigen Ebene ermittelt.</span><span class="sxs-lookup"><span data-stu-id="04397-121">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="04397-122">In der Regel hat dieser Tensor  die gleichen Größen wie die Ausgabe des entsprechenden DML_MAX_POOLING2_OPERATOR_DESC [im](./ns-directml-dml_max_pooling2_operator_desc.md) Vorwärtspass.</span><span class="sxs-lookup"><span data-stu-id="04397-122">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="04397-123">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04397-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04397-124">Ein Ausgabe-Tensor, der die zurückpropagierten Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="04397-124">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="04397-125">In der Regel hat dieser Tensor  die gleichen Größen wie die Eingabe des entsprechenden DML_MAX_POOLING2_OPERATOR_DESC [im](./ns-directml-dml_max_pooling2_operator_desc.md) Vorwärtspass.</span><span class="sxs-lookup"><span data-stu-id="04397-125">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="04397-126">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="04397-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="04397-127">Die Anzahl der Elemente in den *Arrays Strides,* *WindowSize,* *StartPadding,* *EndPadding* und *Dilations.*</span><span class="sxs-lookup"><span data-stu-id="04397-127">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, *EndPadding*, and *Dilations* arrays.</span></span> <span data-ttu-id="04397-128">Dieser Wert muss der Anzahl räumlicher Dimensionen (DimensionCount - 2 von InputTensor) entspricht.</span><span class="sxs-lookup"><span data-stu-id="04397-128">This value must equal the spatial dimension count (InputTensor's DimensionCount - 2).</span></span> <span data-ttu-id="04397-129">Da dieser Operator nur 4D-Tensoren unterstützt, ist der einzige gültige Wert für diesen Parameter 2.</span><span class="sxs-lookup"><span data-stu-id="04397-129">As this operator only supports 4D tensors, the only valid value for this parameter is 2.</span></span>

`Strides`

<span data-ttu-id="04397-130">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="04397-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="04397-131">Siehe *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="04397-131">See *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`WindowSize`

<span data-ttu-id="04397-132">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="04397-132">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="04397-133">Weitere *Informationen finden Sie unter WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="04397-133">See *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`StartPadding`

<span data-ttu-id="04397-134">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="04397-134">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="04397-135">Weitere *Informationen finden Sie unter StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="04397-135">See *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`EndPadding`

<span data-ttu-id="04397-136">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="04397-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="04397-137">Weitere *Informationen finden Sie unter EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="04397-137">See *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`Dilations`

<span data-ttu-id="04397-138">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="04397-138">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="04397-139">Weitere Informationen finden Sie unter *Dilationen* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="04397-139">See *Dilations* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

## <a name="availability"></a><span data-ttu-id="04397-140">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="04397-140">Availability</span></span>
<span data-ttu-id="04397-141">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="04397-141">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="04397-142">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="04397-142">Tensor constraints</span></span>
* <span data-ttu-id="04397-143">*InputTensor* und *OutputGradientTensor* müssen die gleichen *Größen haben.*</span><span class="sxs-lookup"><span data-stu-id="04397-143">*InputTensor* and *OutputGradientTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="04397-144">*InputGradientTensor,* *InputTensor* und *OutputGradientTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="04397-144">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="04397-145">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="04397-145">Tensor support</span></span>
| <span data-ttu-id="04397-146">Tensor</span><span class="sxs-lookup"><span data-stu-id="04397-146">Tensor</span></span> | <span data-ttu-id="04397-147">Typ</span><span class="sxs-lookup"><span data-stu-id="04397-147">Kind</span></span> | <span data-ttu-id="04397-148">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="04397-148">Dimensions</span></span> | <span data-ttu-id="04397-149">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="04397-149">Supported dimension counts</span></span> | <span data-ttu-id="04397-150">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="04397-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="04397-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="04397-151">InputTensor</span></span> | <span data-ttu-id="04397-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04397-152">Input</span></span> | <span data-ttu-id="04397-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="04397-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="04397-154">4</span><span class="sxs-lookup"><span data-stu-id="04397-154">4</span></span> | <span data-ttu-id="04397-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="04397-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="04397-156">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="04397-156">InputGradientTensor</span></span> | <span data-ttu-id="04397-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04397-157">Input</span></span> | <span data-ttu-id="04397-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="04397-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="04397-159">4</span><span class="sxs-lookup"><span data-stu-id="04397-159">4</span></span> | <span data-ttu-id="04397-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="04397-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="04397-161">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="04397-161">OutputGradientTensor</span></span> | <span data-ttu-id="04397-162">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="04397-162">Output</span></span> | <span data-ttu-id="04397-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="04397-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="04397-164">4</span><span class="sxs-lookup"><span data-stu-id="04397-164">4</span></span> | <span data-ttu-id="04397-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="04397-165">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="04397-166">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="04397-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="04397-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="04397-167">**Header**</span></span> | <span data-ttu-id="04397-168">directml.h</span><span class="sxs-lookup"><span data-stu-id="04397-168">directml.h</span></span> |