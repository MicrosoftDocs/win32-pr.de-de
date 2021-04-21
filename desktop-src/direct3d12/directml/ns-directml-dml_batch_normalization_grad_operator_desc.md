---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Berechnet Rückeigenschaftenverläufe für die [Batchnormalisierung.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: ba12541514c8121d483236afa2163a04bd991288
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804523"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="f842a-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="f842a-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="f842a-104">Berechnet Rückeigenschaftenverläufe für die [Batchnormalisierung.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="f842a-104">Computes backpropagation gradients for [batch normalization](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span></span> <span data-ttu-id="f842a-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** führt mehrere Berechnungen aus, die in den separaten Ausgabebeschreibungen ausführlich beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f842a-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** performs multiple computations, which are detailed in the separate output descriptions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f842a-106">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher).</span><span class="sxs-lookup"><span data-stu-id="f842a-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="f842a-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="f842a-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f842a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f842a-108">Syntax</span></span>
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="f842a-109">Member</span><span class="sxs-lookup"><span data-stu-id="f842a-109">Members</span></span>

`InputTensor`

<span data-ttu-id="f842a-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f842a-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f842a-111">Ein Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="f842a-111">A tensor containing the input data.</span></span> <span data-ttu-id="f842a-112">Dies ist in der Regel der gleiche Tensor, der als *InputTensor* bereitgestellt wurde, um DML_BATCH_NORMALIZATION_OPERATOR_DESC [**vorwärts**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f842a-112">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="f842a-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f842a-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f842a-114">Der eingehende Farbverlaufs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="f842a-114">The incoming gradient tensor.</span></span> <span data-ttu-id="f842a-115">Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorherigen Ebene ermittelt.</span><span class="sxs-lookup"><span data-stu-id="f842a-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="f842a-116">Dieser Tensor muss die gleichen Dimensionsgrößen wie *InputTensor aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="f842a-116">This tensor must have the same dimension sizes as *InputTensor*.</span></span>

`MeanTensor`

<span data-ttu-id="f842a-117">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f842a-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f842a-118">Ein Tensor, der die Mittelwertdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="f842a-118">A tensor containing the mean data.</span></span> <span data-ttu-id="f842a-119">Dies ist in der Regel der gleiche Tensor, der als *MeanTensor* bereitgestellt wurde, um DML_BATCH_NORMALIZATION_OPERATOR_DESC [**vorwärts**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f842a-119">This is typically the same tensor that was provided as the *MeanTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="f842a-120">Alle Dimensionen, die nicht die gleiche Größe wie die entsprechende Dimension von *InputTensor* haben, müssen eine Größe von 1 haben, damit sie für die Eingabe übertragen werden können.</span><span class="sxs-lookup"><span data-stu-id="f842a-120">Any dimensions that don't have the same size as the corresponding dimension of *InputTensor* must have a size of 1 so that they can be broadcast to match the input.</span></span>

<span data-ttu-id="f842a-121">Beispielsweise sind die folgenden Größen akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="f842a-121">For example, the following sizes are acceptable.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

<span data-ttu-id="f842a-122">Es folgt ein Fehler, da alle Dimensionen, die nicht übereinstimmen, die Größe 1 haben müssen, um übertragungskompatibel zu sein.</span><span class="sxs-lookup"><span data-stu-id="f842a-122">The following is an error since, in order to be broadcast compatible, any dimensions that don't match must be size 1.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

<span data-ttu-id="f842a-123">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f842a-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f842a-124">Ein Tensor, der die Varianzdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="f842a-124">A tensor containing the variance data.</span></span> <span data-ttu-id="f842a-125">Dies ist in der Regel derselbe Tensor, der als *VarianceTensor* für [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) im Vorwärtsdurchlauf bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f842a-125">This is typically the same tensor that was provided as the *VarianceTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="f842a-126">Dieser Tensor muss die gleichen Dimensionsgrößen wie *MeanTensor* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f842a-126">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`ScaleTensor`

<span data-ttu-id="f842a-127">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f842a-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f842a-128">Ein Tensor, der die Skalierungsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="f842a-128">A tensor containing the scale data.</span></span> <span data-ttu-id="f842a-129">Dies ist in der Regel derselbe Tensor, der als *ScaleTensor* für [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) im Vorwärtsdurchlauf bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f842a-129">This is typically the same tensor that was provided as the *ScaleTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="f842a-130">Dieser Tensor muss die gleichen Dimensionsgrößen wie *MeanTensor* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f842a-130">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`OutputGradientTensor`

<span data-ttu-id="f842a-131">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f842a-131">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f842a-132">Für jeden entsprechenden Wert in den Eingaben `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .</span><span class="sxs-lookup"><span data-stu-id="f842a-132">For every corresponding value in the inputs, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))`.</span></span>

<span data-ttu-id="f842a-133">Dieser Tensor muss die gleichen Dimensionsgrößen wie *InputTensor* / *InputGradientTensor* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f842a-133">This tensor must have the same dimension sizes as *InputTensor*/*InputGradientTensor*.</span></span>

`OutputScaleGradientTensor`

<span data-ttu-id="f842a-134">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f842a-134">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f842a-135">Dieser Tensor muss die gleichen Dimensionsgrößen wie *MeanTensor* / *VarianceTensor* / *ScaleTensor' aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="f842a-135">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="f842a-136">Die folgende Berechnung erfolgt oder jeder entsprechende Wert in den Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f842a-136">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

<span data-ttu-id="f842a-137">Wird `sum` über alle Dimensionen berechnet, die übertragen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f842a-137">The `sum` is computed across any dimensions that need to be broadcast.</span></span> <span data-ttu-id="f842a-138">Wenn keine Übertragung erforderlich ist, ist keine Summe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f842a-138">If there is no broadcast needed, then no sum is needed.</span></span>

<span data-ttu-id="f842a-139">Hier sehen Sie ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f842a-139">Here's an example.</span></span>

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

<span data-ttu-id="f842a-140">Das Element [0, **0**, 0, 0] von `OutputScaleGradientTensor` ist die Summe von für alle `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` 90 (3 \* 5 \* 6) Elemente [[0,2], **0**, [0,4], [0,5]].</span><span class="sxs-lookup"><span data-stu-id="f842a-140">Element [0, **0**, 0, 0] of `OutputScaleGradientTensor` is the sum of `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` for all 90 (3\*5\*6) elements [[0,2], **0**, [0,4], [0,5]].</span></span>

`OutputBiasGradientTensor`

<span data-ttu-id="f842a-141">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f842a-141">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f842a-142">Dieser Tensor muss die gleichen Dimensionsgrößen wie *MeanTensor* / *VarianceTensor* / *ScaleTensor' aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="f842a-142">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="f842a-143">Die folgende Berechnung erfolgt oder jeder entsprechende Wert in den Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f842a-143">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputBiasGradient = sum(InputGradient)`  

<span data-ttu-id="f842a-144">Die `sum` wird für alle Dimensionen berechnet, die übertragen werden müssen (siehe Beispiel für *OutputScaleGradientTensor*).</span><span class="sxs-lookup"><span data-stu-id="f842a-144">The `sum` is computed across any dimensions that need to be broadcast (see the example for *OutputScaleGradientTensor*).</span></span> <span data-ttu-id="f842a-145">Wenn keine Übertragung erforderlich ist, ist keine Summe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f842a-145">If there is no broadcast needed, then no sum is needed.</span></span>

`Epsilon`

<span data-ttu-id="f842a-146">Typ: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f842a-146">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="f842a-147">Ein kleiner Wert, der der Varianz hinzugefügt wird, um 0 (null) zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="f842a-147">A small value added to the variance to avoid zero.</span></span>

## <a name="availability"></a><span data-ttu-id="f842a-148">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="f842a-148">Availability</span></span>
<span data-ttu-id="f842a-149">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f842a-149">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f842a-150">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="f842a-150">Tensor constraints</span></span>
<span data-ttu-id="f842a-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor* und *VarianceTensor* müssen denselben *DataType* und *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f842a-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f842a-152">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="f842a-152">Tensor support</span></span>
| <span data-ttu-id="f842a-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="f842a-153">Tensor</span></span> | <span data-ttu-id="f842a-154">Typ</span><span class="sxs-lookup"><span data-stu-id="f842a-154">Kind</span></span> | <span data-ttu-id="f842a-155">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="f842a-155">Supported dimension counts</span></span> | <span data-ttu-id="f842a-156">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="f842a-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f842a-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f842a-157">InputTensor</span></span> | <span data-ttu-id="f842a-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f842a-158">Input</span></span> | <span data-ttu-id="f842a-159">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f842a-159">1 to 8</span></span> | <span data-ttu-id="f842a-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f842a-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f842a-161">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f842a-161">InputGradientTensor</span></span> | <span data-ttu-id="f842a-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f842a-162">Input</span></span> | <span data-ttu-id="f842a-163">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f842a-163">1 to 8</span></span> | <span data-ttu-id="f842a-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f842a-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f842a-165">MeanTensor</span><span class="sxs-lookup"><span data-stu-id="f842a-165">MeanTensor</span></span> | <span data-ttu-id="f842a-166">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f842a-166">Input</span></span> | <span data-ttu-id="f842a-167">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f842a-167">1 to 8</span></span> | <span data-ttu-id="f842a-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f842a-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f842a-169">VarianceTensor</span><span class="sxs-lookup"><span data-stu-id="f842a-169">VarianceTensor</span></span> | <span data-ttu-id="f842a-170">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f842a-170">Input</span></span> | <span data-ttu-id="f842a-171">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f842a-171">1 to 8</span></span> | <span data-ttu-id="f842a-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f842a-172">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f842a-173">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="f842a-173">ScaleTensor</span></span> | <span data-ttu-id="f842a-174">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f842a-174">Input</span></span> | <span data-ttu-id="f842a-175">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f842a-175">1 to 8</span></span> | <span data-ttu-id="f842a-176">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f842a-176">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f842a-177">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f842a-177">OutputGradientTensor</span></span> | <span data-ttu-id="f842a-178">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f842a-178">Output</span></span> | <span data-ttu-id="f842a-179">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f842a-179">1 to 8</span></span> | <span data-ttu-id="f842a-180">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f842a-180">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f842a-181">OutputScaleGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f842a-181">OutputScaleGradientTensor</span></span> | <span data-ttu-id="f842a-182">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f842a-182">Output</span></span> | <span data-ttu-id="f842a-183">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f842a-183">1 to 8</span></span> | <span data-ttu-id="f842a-184">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f842a-184">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f842a-185">OutputBiasGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f842a-185">OutputBiasGradientTensor</span></span> | <span data-ttu-id="f842a-186">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f842a-186">Output</span></span> | <span data-ttu-id="f842a-187">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f842a-187">1 to 8</span></span> | <span data-ttu-id="f842a-188">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f842a-188">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="f842a-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f842a-189">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f842a-190">**Header**</span><span class="sxs-lookup"><span data-stu-id="f842a-190">**Header**</span></span> | <span data-ttu-id="f842a-191">directml.h</span><span class="sxs-lookup"><span data-stu-id="f842a-191">directml.h</span></span> |
