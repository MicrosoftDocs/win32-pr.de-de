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
ms.openlocfilehash: eecf849a06ee8e99ac9c015ecd4568496120b2d9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804439"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="2e968-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="2e968-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="2e968-104">Berechnet Rückeigenschaftenverläufe für die [lokale Antwortnormalisierung.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="2e968-104">Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span></span>

<span data-ttu-id="2e968-105">Datentyp und Größe aller Tensoren müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="2e968-105">The data type and size of all tensors must be the same.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e968-106">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher).</span><span class="sxs-lookup"><span data-stu-id="2e968-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="2e968-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="2e968-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e968-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e968-108">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="2e968-109">Member</span><span class="sxs-lookup"><span data-stu-id="2e968-109">Members</span></span>

`InputTensor`

<span data-ttu-id="2e968-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2e968-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2e968-111">Der Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="2e968-111">The tensor containing the input data.</span></span> <span data-ttu-id="2e968-112">Die Größen dieses Tensors *sollten* `{ BatchCount, ChannelCount, Height, Width }` sein.</span><span class="sxs-lookup"><span data-stu-id="2e968-112">This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`InputGradientTensor`

<span data-ttu-id="2e968-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2e968-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2e968-114">Der eingehende Farbverlaufs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="2e968-114">The incoming gradient tensor.</span></span> <span data-ttu-id="2e968-115">Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorherigen Ebene ermittelt.</span><span class="sxs-lookup"><span data-stu-id="2e968-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span>

`OutputGradientTensor`

<span data-ttu-id="2e968-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2e968-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2e968-117">Ein Ausgabe-Tensor, der die zurückpropagierten Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="2e968-117">An output tensor containing the backpropagated gradients.</span></span>

`CrossChannel`

<span data-ttu-id="2e968-118">Typ: **[BOOL](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2e968-118">Type: **[BOOL](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="2e968-119">**TRUE,** wenn die LRN-Schicht kanalübergreifend summiert wird; **FALSE,** wenn die LRN-Schicht über räumliche Dimensionen summiert wird.</span><span class="sxs-lookup"><span data-stu-id="2e968-119">**TRUE** if the LRN layer sums across channels; **FALSE** if the LRN layer sums across spatial dimensions.</span></span>

`LocalSize`

<span data-ttu-id="2e968-120">Typ: **[UINT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2e968-120">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="2e968-121">Die maximale Anzahl von Elementen, die pro Dimension summiert werden sollen (der lokale Bereich wird abgeschnitten, sodass sich alle Elemente innerhalb der Grenzen befinden).</span><span class="sxs-lookup"><span data-stu-id="2e968-121">The maximum number of elements to sum over per dimension (the local region is clipped so that all elements are within bounds).</span></span> <span data-ttu-id="2e968-122">Wenn *CrossChannel* **true ist,** ist dies die Breite und Höhe des lokalen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="2e968-122">If *CrossChannel* is **TRUE**, then this is the width and height of the local region.</span></span> <span data-ttu-id="2e968-123">Wenn *CrossChannel* **FALSE** ist, ist dies die Anzahl der Elemente in der lokalen Region.</span><span class="sxs-lookup"><span data-stu-id="2e968-123">If *CrossChannel* is **FALSE**, then this is the number of elements in the local region.</span></span> <span data-ttu-id="2e968-124">Dieser Wert muss mindestens 1 sein.</span><span class="sxs-lookup"><span data-stu-id="2e968-124">This value must be at least 1.</span></span>

`Alpha`

<span data-ttu-id="2e968-125">Typ: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2e968-125">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="2e968-126">Der Wert des Skalierungsparameters.</span><span class="sxs-lookup"><span data-stu-id="2e968-126">The value of the scaling parameter.</span></span> <span data-ttu-id="2e968-127">Der Standardwert ist 0,0001.</span><span class="sxs-lookup"><span data-stu-id="2e968-127">We recommend a value of 0.0001 as default.</span></span>

`Beta`

<span data-ttu-id="2e968-128">Typ: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2e968-128">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="2e968-129">Der Wert des Exponenten.</span><span class="sxs-lookup"><span data-stu-id="2e968-129">The value of the exponent.</span></span> <span data-ttu-id="2e968-130">Der Standardwert ist 0,75.</span><span class="sxs-lookup"><span data-stu-id="2e968-130">We recommend a value of 0.75 as default.</span></span>

`Bias`

<span data-ttu-id="2e968-131">Typ: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2e968-131">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="2e968-132">Der Wert von Bias.</span><span class="sxs-lookup"><span data-stu-id="2e968-132">The value of bias.</span></span> <span data-ttu-id="2e968-133">Es wird empfohlen, standardmäßig den Wert 1 zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="2e968-133">We recommend a value of 1 as default.</span></span>

## <a name="availability"></a><span data-ttu-id="2e968-134">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="2e968-134">Availability</span></span>
<span data-ttu-id="2e968-135">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2e968-135">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2e968-136">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="2e968-136">Tensor constraints</span></span>
<span data-ttu-id="2e968-137">*InputGradientTensor,* *InputTensor* und *OutputGradientTensor* müssen den gleichen *Datentyp* und die gleichen *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2e968-137">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2e968-138">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="2e968-138">Tensor support</span></span>
| <span data-ttu-id="2e968-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="2e968-139">Tensor</span></span> | <span data-ttu-id="2e968-140">Typ</span><span class="sxs-lookup"><span data-stu-id="2e968-140">Kind</span></span> | <span data-ttu-id="2e968-141">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="2e968-141">Supported dimension counts</span></span> | <span data-ttu-id="2e968-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="2e968-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2e968-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="2e968-143">InputTensor</span></span> | <span data-ttu-id="2e968-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e968-144">Input</span></span> | <span data-ttu-id="2e968-145">4</span><span class="sxs-lookup"><span data-stu-id="2e968-145">4</span></span> | <span data-ttu-id="2e968-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2e968-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2e968-147">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="2e968-147">InputGradientTensor</span></span> | <span data-ttu-id="2e968-148">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e968-148">Input</span></span> | <span data-ttu-id="2e968-149">4</span><span class="sxs-lookup"><span data-stu-id="2e968-149">4</span></span> | <span data-ttu-id="2e968-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2e968-150">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2e968-151">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="2e968-151">OutputGradientTensor</span></span> | <span data-ttu-id="2e968-152">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="2e968-152">Output</span></span> | <span data-ttu-id="2e968-153">4</span><span class="sxs-lookup"><span data-stu-id="2e968-153">4</span></span> | <span data-ttu-id="2e968-154">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2e968-154">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="2e968-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e968-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2e968-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="2e968-156">**Header**</span></span> | <span data-ttu-id="2e968-157">directml.h</span><span class="sxs-lookup"><span data-stu-id="2e968-157">directml.h</span></span> |
