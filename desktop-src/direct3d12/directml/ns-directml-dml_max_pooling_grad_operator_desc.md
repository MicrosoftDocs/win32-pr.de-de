---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Berechnet backpropagierungs Gradienten für Max Pooling (siehe [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
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
ms.openlocfilehash: b7314cb6b9456d9ac9f99e90100085e86f88ffd9
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354285"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="bc3c4-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="bc3c4-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="bc3c4-104">Berechnet backpropagierungs Gradienten für Max Pooling (siehe [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span><span class="sxs-lookup"><span data-stu-id="bc3c4-104">Computes backpropagation gradients for max pooling (see [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span></span>

<span data-ttu-id="bc3c4-105">Angenommen, ein 2 x 2- **DML_MAX_POOLING2_OPERATOR_DESC** ohne Auffüll-und Vergrößerungen und ein Schritt von 1, der Folgendes ausführt:</span><span class="sxs-lookup"><span data-stu-id="bc3c4-105">Consider a 2x2 **DML_MAX_POOLING2_OPERATOR_DESC** without padding nor dilations and a stride of 1, which performs the following.</span></span>

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

<span data-ttu-id="bc3c4-106">Das größte Element jedes 2 x 2-Fensters im Eingabe Mandanten erzeugt ein Element der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-106">The largest element of each 2x2 window in the input tensor produces one element of the output.</span></span> <span data-ttu-id="bc3c4-107">Im folgenden finden Sie ein Beispiel für die Ausgabe von **DML_MAX_POOLING_GRAD_OPERATOR_DESC** mit ähnlichen Parametern.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-107">Below is an example of the output of **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, given similar parameters.</span></span>

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

<span data-ttu-id="bc3c4-108">In der Tat verwendet dieser Operator den *inputtensor* , um den Index des größten Elements in jedem Fenster zu bestimmen, und verteilt die Werte von *inputgradienttensor* basierend auf diesen Indizes in den *outputgradienttensor* .</span><span class="sxs-lookup"><span data-stu-id="bc3c4-108">In effect, this operator uses the *InputTensor* to determine the index of the largest element from each window, and distributes the values of *InputGradientTensor* into the *OutputGradientTensor* based on these indices.</span></span> <span data-ttu-id="bc3c4-109">Wenn Indizes überlappen, werden die Werte summiert.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-109">Where indices overlap, the values are summed.</span></span> <span data-ttu-id="bc3c4-110">Alle nicht referenzierten Ausgabe Elemente werden nulgerert.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-110">Any unreferenced output elements are zeroed.</span></span>

<span data-ttu-id="bc3c4-111">Im Fall einer Verknüpfung (bei der mehr als ein Element in einem Fenster denselben maximalen Wert aufweist), wird das Element mit dem niedrigsten logischen Element Index ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-111">In the case of a tie (where more than one element in a window has the same maximum value), the element with the lowest logical element index is chosen.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc3c4-112">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="bc3c4-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="bc3c4-113">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="bc3c4-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3c4-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc3c4-114">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="bc3c4-115">Member</span><span class="sxs-lookup"><span data-stu-id="bc3c4-115">Members</span></span>

`InputTensor`

<span data-ttu-id="bc3c4-116">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bc3c4-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bc3c4-117">Der eingabefeaturetensor.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-117">The input feature tensor.</span></span> <span data-ttu-id="bc3c4-118">Dabei handelt es sich in der Regel um denselben tensorflow, der als *inputtensor* zur [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) im Forward-Durchlauf bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-118">This is typically the same tensor that was provided as the *InputTensor* to [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="bc3c4-119">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bc3c4-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bc3c4-120">Der eingehende gradiententensor.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-120">The incoming gradient tensor.</span></span> <span data-ttu-id="bc3c4-121">Dies wird in der Regel aus der Ausgabe der Rück Propagierung einer vorangehenden Ebene abgerufen.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-121">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="bc3c4-122">In der Regel hat dieser tensorflow die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) im Forward-Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-122">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="bc3c4-123">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bc3c4-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bc3c4-124">Ein Ausgabe Mandanten, der die zurückgegebenen Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-124">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="bc3c4-125">In der Regel hat dieser Mandanten die gleichen Größen wie die *Eingabe* der entsprechenden [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) im Forward-Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-125">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="bc3c4-126">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bc3c4-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="bc3c4-127">Die Anzahl der Elemente in den Arrays "Step", " *WindowSize*", " *startpadding* *", "* *endpadding*" und " *Vergrößerungen* ".</span><span class="sxs-lookup"><span data-stu-id="bc3c4-127">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, *EndPadding*, and *Dilations* arrays.</span></span> <span data-ttu-id="bc3c4-128">Dieser Wert muss gleich der Anzahl räumlicher Dimensionen ("DimensionCount-2" von inputtensor) sein.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-128">This value must equal the spatial dimension count (InputTensor's DimensionCount - 2).</span></span> <span data-ttu-id="bc3c4-129">Da dieser Operator nur 4D-Tensoren unterstützt, ist der einzige gültige Wert für diesen Parameter 2.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-129">As this operator only supports 4D tensors, the only valid value for this parameter is 2.</span></span>

`Strides`

<span data-ttu-id="bc3c4-130">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="bc3c4-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="bc3c4-131">Siehe *Schritte* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="bc3c4-131">See *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`WindowSize`

<span data-ttu-id="bc3c4-132">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="bc3c4-132">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="bc3c4-133">Siehe *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="bc3c4-133">See *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`StartPadding`

<span data-ttu-id="bc3c4-134">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="bc3c4-134">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="bc3c4-135">Siehe *startpadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="bc3c4-135">See *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`EndPadding`

<span data-ttu-id="bc3c4-136">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="bc3c4-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="bc3c4-137">Siehe *endpadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="bc3c4-137">See *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`Dilations`

<span data-ttu-id="bc3c4-138">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="bc3c4-138">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="bc3c4-139">Weitere *Informationen* finden Sie unter [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="bc3c4-139">See *Dilations* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

## <a name="availability"></a><span data-ttu-id="bc3c4-140">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="bc3c4-140">Availability</span></span>
<span data-ttu-id="bc3c4-141">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="bc3c4-141">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="bc3c4-142">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="bc3c4-142">Tensor constraints</span></span>
* <span data-ttu-id="bc3c4-143">*Inputtensor* und *outputgradienttensor* müssen die gleichen *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-143">*InputTensor* and *OutputGradientTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="bc3c4-144">*Inputgradienttensor*, *inputtensor* und *outputgradienttensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bc3c4-144">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="bc3c4-145">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="bc3c4-145">Tensor support</span></span>
| <span data-ttu-id="bc3c4-146">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="bc3c4-146">Tensor</span></span> | <span data-ttu-id="bc3c4-147">Typ</span><span class="sxs-lookup"><span data-stu-id="bc3c4-147">Kind</span></span> | <span data-ttu-id="bc3c4-148">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="bc3c4-148">Dimensions</span></span> | <span data-ttu-id="bc3c4-149">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="bc3c4-149">Supported dimension counts</span></span> | <span data-ttu-id="bc3c4-150">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="bc3c4-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="bc3c4-151">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="bc3c4-151">InputTensor</span></span> | <span data-ttu-id="bc3c4-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc3c4-152">Input</span></span> | <span data-ttu-id="bc3c4-153">{BatchCount, ChannelCount, inputheight, inputwidth}</span><span class="sxs-lookup"><span data-stu-id="bc3c4-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="bc3c4-154">4</span><span class="sxs-lookup"><span data-stu-id="bc3c4-154">4</span></span> | <span data-ttu-id="bc3c4-155">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="bc3c4-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="bc3c4-156">Input gradienttensor</span><span class="sxs-lookup"><span data-stu-id="bc3c4-156">InputGradientTensor</span></span> | <span data-ttu-id="bc3c4-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc3c4-157">Input</span></span> | <span data-ttu-id="bc3c4-158">{BatchCount, ChannelCount, OutputHeight, OutputWidth}</span><span class="sxs-lookup"><span data-stu-id="bc3c4-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="bc3c4-159">4</span><span class="sxs-lookup"><span data-stu-id="bc3c4-159">4</span></span> | <span data-ttu-id="bc3c4-160">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="bc3c4-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="bc3c4-161">Outputgradienttensor</span><span class="sxs-lookup"><span data-stu-id="bc3c4-161">OutputGradientTensor</span></span> | <span data-ttu-id="bc3c4-162">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="bc3c4-162">Output</span></span> | <span data-ttu-id="bc3c4-163">{BatchCount, ChannelCount, inputheight, inputwidth}</span><span class="sxs-lookup"><span data-stu-id="bc3c4-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="bc3c4-164">4</span><span class="sxs-lookup"><span data-stu-id="bc3c4-164">4</span></span> | <span data-ttu-id="bc3c4-165">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="bc3c4-165">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="bc3c4-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc3c4-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bc3c4-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="bc3c4-167">**Header**</span></span> | <span data-ttu-id="bc3c4-168">directml. h</span><span class="sxs-lookup"><span data-stu-id="bc3c4-168">directml.h</span></span> |