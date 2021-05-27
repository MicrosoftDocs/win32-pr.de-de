---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: Berechnet Backpropagation-Farbverläufe für [elementweise Clip.](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 3b993ca1c027119ae64157db2327a2836445bf43
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550205"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a><span data-ttu-id="f4cb1-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="f4cb1-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="f4cb1-104">Berechnet Backpropagation-Farbverläufe für [elementweise Clip.](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="f4cb1-104">Computes backpropagation gradients for [element-wise clip](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).</span></span>

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

<span data-ttu-id="f4cb1-105">Dieser Operator unterstützt die ausführungsbasierte Ausführung, was bedeutet, dass `OutputTensor` *inputTensor während* der Bindung als Alias verwendet werden darf.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-105">This operator supports in-place execution, meaning `OutputTensor` is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4cb1-106">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher).</span><span class="sxs-lookup"><span data-stu-id="f4cb1-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="f4cb1-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="f4cb1-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4cb1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4cb1-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a><span data-ttu-id="f4cb1-109">Member</span><span class="sxs-lookup"><span data-stu-id="f4cb1-109">Members</span></span>

`InputTensor`

<span data-ttu-id="f4cb1-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f4cb1-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f4cb1-111">Der Eingabefunktions-Tensor.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-111">The input feature tensor.</span></span> <span data-ttu-id="f4cb1-112">Dies ist in der Regel der gleiche Tensor, der als *InputTensor* bereitgestellt wurde, um DML_ELEMENT_WISE_CLIP_OPERATOR_DESC [vorwärts](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-112">This is typically the same tensor that was provided as the *InputTensor* to [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="f4cb1-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f4cb1-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f4cb1-114">Der eingehende Farbverlaufs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-114">The incoming gradient tensor.</span></span> <span data-ttu-id="f4cb1-115">Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorherigen Ebene ermittelt.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="f4cb1-116">In der Regel hat dieser Tensor die gleichen Größen wie *die* Ausgabe des entsprechenden DML_OPERATOR_ELEMENT_WISE_CLIP **im** Vorwärtspass.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-116">Typically this tensor would have the same sizes as the *output* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="f4cb1-117">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f4cb1-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f4cb1-118">Ein Ausgabe tensor, der die zurückpropagierten Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="f4cb1-119">In der Regel hat dieser Tensor  die gleichen Größen wie die Eingabe des entsprechenden DML_OPERATOR_ELEMENT_WISE_CLIP **im** Vorwärtspass.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-119">Typically this tensor would have the same sizes as the *input* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`Min`

<span data-ttu-id="f4cb1-120">Typ: **[FLOAT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4cb1-120">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4cb1-121">Der Minimalwert.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-121">The minimum value.</span></span> <span data-ttu-id="f4cb1-122">Wenn x bei oder unter diesem Wert liegt, ist das Farbverlaufsergebnis 0.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-122">If x is at or below this value, then the gradient result is 0.</span></span>

`Max`

<span data-ttu-id="f4cb1-123">Typ: **[FLOAT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4cb1-123">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4cb1-124">Der Maximalwert.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-124">The maximum value.</span></span> <span data-ttu-id="f4cb1-125">Wenn x bei oder über diesem Wert liegt, ist das Farbverlaufsergebnis 0.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-125">If x is at or above this value, then the gradient result is 0.</span></span>

## <a name="availability"></a><span data-ttu-id="f4cb1-126">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="f4cb1-126">Availability</span></span>
<span data-ttu-id="f4cb1-127">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-127">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f4cb1-128">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="f4cb1-128">Tensor constraints</span></span>
<span data-ttu-id="f4cb1-129">*InputGradientTensor,* *InputTensor* und *OutputGradientTensor* müssen die gleichen *Datentypen*, *DimensionCount* und *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f4cb1-129">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f4cb1-130">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="f4cb1-130">Tensor support</span></span>
| <span data-ttu-id="f4cb1-131">Tensor</span><span class="sxs-lookup"><span data-stu-id="f4cb1-131">Tensor</span></span> | <span data-ttu-id="f4cb1-132">Typ</span><span class="sxs-lookup"><span data-stu-id="f4cb1-132">Kind</span></span> | <span data-ttu-id="f4cb1-133">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="f4cb1-133">Supported dimension counts</span></span> | <span data-ttu-id="f4cb1-134">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="f4cb1-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f4cb1-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f4cb1-135">InputTensor</span></span> | <span data-ttu-id="f4cb1-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f4cb1-136">Input</span></span> | <span data-ttu-id="f4cb1-137">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f4cb1-137">1 to 8</span></span> | <span data-ttu-id="f4cb1-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f4cb1-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f4cb1-139">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f4cb1-139">InputGradientTensor</span></span> | <span data-ttu-id="f4cb1-140">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f4cb1-140">Input</span></span> | <span data-ttu-id="f4cb1-141">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f4cb1-141">1 to 8</span></span> | <span data-ttu-id="f4cb1-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f4cb1-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f4cb1-143">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f4cb1-143">OutputGradientTensor</span></span> | <span data-ttu-id="f4cb1-144">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f4cb1-144">Output</span></span> | <span data-ttu-id="f4cb1-145">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f4cb1-145">1 to 8</span></span> | <span data-ttu-id="f4cb1-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f4cb1-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="f4cb1-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4cb1-147">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f4cb1-148">**Header**</span><span class="sxs-lookup"><span data-stu-id="f4cb1-148">**Header**</span></span> | <span data-ttu-id="f4cb1-149">directml.h</span><span class="sxs-lookup"><span data-stu-id="f4cb1-149">directml.h</span></span> |