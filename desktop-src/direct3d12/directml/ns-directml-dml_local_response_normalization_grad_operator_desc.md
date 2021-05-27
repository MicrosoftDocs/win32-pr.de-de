---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Berechnet Rückeigenschaftenverläufe für die [lokale Antwortnormalisierung.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: e858b8ce20df4b1bf12ac9efe360941eb93c54d1
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550405"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="73be7-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="73be7-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="73be7-104">Berechnet Rückeigenschaftenverläufe für die [lokale Antwortnormalisierung.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="73be7-104">Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span></span>

<span data-ttu-id="73be7-105">Der Datentyp und die Größe aller Tensoren müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="73be7-105">The data type and size of all tensors must be the same.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73be7-106">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher).</span><span class="sxs-lookup"><span data-stu-id="73be7-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="73be7-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="73be7-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="73be7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="73be7-108">Syntax</span></span>
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a><span data-ttu-id="73be7-109">Member</span><span class="sxs-lookup"><span data-stu-id="73be7-109">Members</span></span>

`InputTensor`

<span data-ttu-id="73be7-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="73be7-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="73be7-111">Der Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="73be7-111">The tensor containing the input data.</span></span> <span data-ttu-id="73be7-112">Die Größen dieses Tensors *sollten* `{ BatchCount, ChannelCount, Height, Width }` sein.</span><span class="sxs-lookup"><span data-stu-id="73be7-112">This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`InputGradientTensor`

<span data-ttu-id="73be7-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="73be7-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="73be7-114">Der eingehende Farbverlaufs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="73be7-114">The incoming gradient tensor.</span></span> <span data-ttu-id="73be7-115">Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorherigen Ebene ermittelt.</span><span class="sxs-lookup"><span data-stu-id="73be7-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span>

`OutputGradientTensor`

<span data-ttu-id="73be7-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="73be7-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="73be7-117">Ein Ausgabe tensor, der die zurückpropagierten Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="73be7-117">An output tensor containing the backpropagated gradients.</span></span>

`CrossChannel`

<span data-ttu-id="73be7-118">Typ: **[BOOL](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73be7-118">Type: **[BOOL](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73be7-119">**TRUE,** wenn die LRN-Schicht kanalübergreifend summiert wird; **FALSE,** wenn die LRN-Schicht über räumliche Dimensionen summiert wird.</span><span class="sxs-lookup"><span data-stu-id="73be7-119">**TRUE** if the LRN layer sums across channels; **FALSE** if the LRN layer sums across spatial dimensions.</span></span>

`LocalSize`

<span data-ttu-id="73be7-120">Typ: **[UINT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73be7-120">Type: **[UINT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73be7-121">Die maximale Anzahl von Elementen, die pro Dimension summiert werden sollen (der lokale Bereich wird abgeschnitten, sodass sich alle Elemente innerhalb der Grenzen befinden).</span><span class="sxs-lookup"><span data-stu-id="73be7-121">The maximum number of elements to sum over per dimension (the local region is clipped so that all elements are within bounds).</span></span> <span data-ttu-id="73be7-122">Wenn *CrossChannel* **true ist,** ist dies die Breite und Höhe des lokalen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="73be7-122">If *CrossChannel* is **TRUE**, then this is the width and height of the local region.</span></span> <span data-ttu-id="73be7-123">Wenn *CrossChannel* **FALSE ist,** ist dies die Anzahl der Elemente in der lokalen Region.</span><span class="sxs-lookup"><span data-stu-id="73be7-123">If *CrossChannel* is **FALSE**, then this is the number of elements in the local region.</span></span> <span data-ttu-id="73be7-124">Dieser Wert muss mindestens 1 sein.</span><span class="sxs-lookup"><span data-stu-id="73be7-124">This value must be at least 1.</span></span>

`Alpha`

<span data-ttu-id="73be7-125">Typ: **[FLOAT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73be7-125">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73be7-126">Der Wert des Skalierungsparameters.</span><span class="sxs-lookup"><span data-stu-id="73be7-126">The value of the scaling parameter.</span></span> <span data-ttu-id="73be7-127">Es wird empfohlen, den Standardwert 0,0001 zu haben.</span><span class="sxs-lookup"><span data-stu-id="73be7-127">We recommend a value of 0.0001 as default.</span></span>

`Beta`

<span data-ttu-id="73be7-128">Typ: **[FLOAT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73be7-128">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73be7-129">Der Wert des Exponenten.</span><span class="sxs-lookup"><span data-stu-id="73be7-129">The value of the exponent.</span></span> <span data-ttu-id="73be7-130">Der Standardwert ist 0,75.</span><span class="sxs-lookup"><span data-stu-id="73be7-130">We recommend a value of 0.75 as default.</span></span>

`Bias`

<span data-ttu-id="73be7-131">Typ: **[FLOAT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73be7-131">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73be7-132">Der Wert von Bias.</span><span class="sxs-lookup"><span data-stu-id="73be7-132">The value of bias.</span></span> <span data-ttu-id="73be7-133">Es wird empfohlen, standardmäßig den Wert 1 zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="73be7-133">We recommend a value of 1 as default.</span></span>

## <a name="availability"></a><span data-ttu-id="73be7-134">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="73be7-134">Availability</span></span>
<span data-ttu-id="73be7-135">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="73be7-135">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="73be7-136">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="73be7-136">Tensor constraints</span></span>
<span data-ttu-id="73be7-137">*InputGradientTensor,* *InputTensor* und *OutputGradientTensor* müssen den gleichen *Datentyp* und die gleichen *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="73be7-137">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="73be7-138">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="73be7-138">Tensor support</span></span>
| <span data-ttu-id="73be7-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="73be7-139">Tensor</span></span> | <span data-ttu-id="73be7-140">Typ</span><span class="sxs-lookup"><span data-stu-id="73be7-140">Kind</span></span> | <span data-ttu-id="73be7-141">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="73be7-141">Supported dimension counts</span></span> | <span data-ttu-id="73be7-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="73be7-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="73be7-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="73be7-143">InputTensor</span></span> | <span data-ttu-id="73be7-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="73be7-144">Input</span></span> | <span data-ttu-id="73be7-145">4</span><span class="sxs-lookup"><span data-stu-id="73be7-145">4</span></span> | <span data-ttu-id="73be7-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="73be7-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="73be7-147">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="73be7-147">InputGradientTensor</span></span> | <span data-ttu-id="73be7-148">Eingabe</span><span class="sxs-lookup"><span data-stu-id="73be7-148">Input</span></span> | <span data-ttu-id="73be7-149">4</span><span class="sxs-lookup"><span data-stu-id="73be7-149">4</span></span> | <span data-ttu-id="73be7-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="73be7-150">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="73be7-151">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="73be7-151">OutputGradientTensor</span></span> | <span data-ttu-id="73be7-152">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="73be7-152">Output</span></span> | <span data-ttu-id="73be7-153">4</span><span class="sxs-lookup"><span data-stu-id="73be7-153">4</span></span> | <span data-ttu-id="73be7-154">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="73be7-154">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="73be7-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73be7-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="73be7-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="73be7-156">**Header**</span></span> | <span data-ttu-id="73be7-157">directml.h</span><span class="sxs-lookup"><span data-stu-id="73be7-157">directml.h</span></span> |