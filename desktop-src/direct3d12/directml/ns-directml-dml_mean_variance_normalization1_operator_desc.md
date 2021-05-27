---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Führt eine durchschnittliche Varianznormalisierungsfunktion für den Eingabe-Tensor aus. Dieser Operator berechnet den Mittelwert und die Varianz des Eingabe-Tensors, um eine Normalisierung durchzuführen.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: ae22b004f1e879eb020ddcfe39a5f26481a508b0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549776"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="58cca-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="58cca-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="58cca-105">Führt eine durchschnittliche Varianznormalisierungsfunktion für den Eingabe-Tensor aus.</span><span class="sxs-lookup"><span data-stu-id="58cca-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="58cca-106">Dieser Operator berechnet den Mittelwert und die Varianz des Eingabe-Tensors, um eine Normalisierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="58cca-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="58cca-107">Dieser Operator führt die folgende Berechnung aus.</span><span class="sxs-lookup"><span data-stu-id="58cca-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="58cca-108">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="58cca-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="58cca-109">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="58cca-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="58cca-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="58cca-110">Syntax</span></span>
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```
## <a name="members"></a><span data-ttu-id="58cca-111">Member</span><span class="sxs-lookup"><span data-stu-id="58cca-111">Members</span></span>

`InputTensor`

<span data-ttu-id="58cca-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="58cca-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="58cca-113">Ein Tensor, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="58cca-113">A tensor containing the Input data.</span></span> <span data-ttu-id="58cca-114">Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, Height, Width }` sein.</span><span class="sxs-lookup"><span data-stu-id="58cca-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="58cca-115">Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="58cca-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="58cca-116">Ein optionaler Tensor, der die Skalierungsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="58cca-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="58cca-117">Wenn **DML_FEATURE_LEVEL** kleiner als **DML_FEATURE_LEVEL_4_0** ist, sollten die Dimensionen dieses Tensors `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` sein.</span><span class="sxs-lookup"><span data-stu-id="58cca-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="58cca-118">Die Dimensionen ScaleBatchCount, ScaleHeight und ScaleWidth sollten entweder mit *InputTensor* übereinstimmen oder auf 1 festgelegt werden, um diese Dimensionen automatisch über die Eingabe zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="58cca-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="58cca-119">Wenn **DML_FEATURE_LEVEL** größer oder gleich **DML_FEATURE_LEVEL_4_0** ist, kann jede Dimension auf 1 festgelegt und automatisch an *InputTensor* gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="58cca-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="58cca-120">Dieser Tensor ist erforderlich, wenn *BiasTensor* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58cca-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="58cca-121">Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="58cca-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="58cca-122">Ein optionaler Tensor, der die Bias-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="58cca-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="58cca-123">Wenn **DML_FEATURE_LEVEL** kleiner als **DML_FEATURE_LEVEL_4_0** ist, sollten die Dimensionen dieses Tensors `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` sein.</span><span class="sxs-lookup"><span data-stu-id="58cca-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="58cca-124">Die Dimensionen BiasBatchCount, BiasHeight und BiasWidth sollten entweder *mit InputTensor* übereinstimmen oder auf 1 festgelegt werden, um diese Dimensionen automatisch über die Eingabe zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="58cca-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="58cca-125">Wenn **DML_FEATURE_LEVEL** größer oder gleich DML_FEATURE_LEVEL_4_0 **ist,** kann jede Dimension auf 1 festgelegt und automatisch an *InputTensor übertragen werden.*</span><span class="sxs-lookup"><span data-stu-id="58cca-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="58cca-126">Dieser Tensor ist erforderlich, wenn *der ScaleTensor* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58cca-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="58cca-127">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="58cca-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="58cca-128">Ein Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="58cca-128">A tensor to write the results to.</span></span> <span data-ttu-id="58cca-129">Die Dimensionen dieses Tensors sind `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="58cca-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="58cca-130">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="58cca-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="58cca-131">Die Anzahl der Achsen.</span><span class="sxs-lookup"><span data-stu-id="58cca-131">The number of axes.</span></span> <span data-ttu-id="58cca-132">Dieses Feld bestimmt die Größe des *Achsenarrays.*</span><span class="sxs-lookup"><span data-stu-id="58cca-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="58cca-133">Typ: \_ \_ Feldgröße \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="58cca-133">Type: \_Field\_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span> 

<span data-ttu-id="58cca-134">Die Achsen, auf denen der Mittelwert und die Varianz berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="58cca-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="58cca-135">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="58cca-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="58cca-136">**TRUE,** wenn die Normalisierungsebene Varianz in der Normalisierungsberechnung enthält.</span><span class="sxs-lookup"><span data-stu-id="58cca-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="58cca-137">Andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="58cca-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="58cca-138">False **gibt an,** dass die Normalisierungsgleichung `Output = FusedActivation(Scale * (Input - Mean) + Bias)` ist.</span><span class="sxs-lookup"><span data-stu-id="58cca-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="58cca-139">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="58cca-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="58cca-140">Der epsilon-Wert, der verwendet werden soll, um eine Division durch 0 (null) zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="58cca-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="58cca-141">Als Standardwert wird der Wert 0,00001 empfohlen.</span><span class="sxs-lookup"><span data-stu-id="58cca-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="58cca-142">Typ: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="58cca-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="58cca-143">Eine optionale fused-Aktivierungsebene, die nach der Normalisierung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58cca-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="58cca-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="58cca-144">Remarks</span></span>
<span data-ttu-id="58cca-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** ist eine Obermenge der Funktionalität [von DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="58cca-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="58cca-146">Hier entspricht  das Festlegen des Axes-Arrays auf `{ 0, 2, 3 }` dem Festlegen von *CrossChannel* auf **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**. Das Festlegen des **Axes-Arrays** auf entspricht dem `{ 1, 2, 3 }` Festlegen von *CrossChannel* auf **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="58cca-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="58cca-147">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="58cca-147">Availability</span></span>
<span data-ttu-id="58cca-148">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="58cca-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="58cca-149">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="58cca-149">Tensor constraints</span></span>

<span data-ttu-id="58cca-150">*BiasTensor,* *InputTensor,* *OutputTensor* und *ScaleTensor* müssen den gleichen *DataType* und *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="58cca-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="58cca-151">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="58cca-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="58cca-152">DML_FEATURE_LEVEL_3_1 und höher</span><span class="sxs-lookup"><span data-stu-id="58cca-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="58cca-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="58cca-153">Tensor</span></span> | <span data-ttu-id="58cca-154">Typ</span><span class="sxs-lookup"><span data-stu-id="58cca-154">Kind</span></span> | <span data-ttu-id="58cca-155">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="58cca-155">Supported dimension counts</span></span> | <span data-ttu-id="58cca-156">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="58cca-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="58cca-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="58cca-157">InputTensor</span></span> | <span data-ttu-id="58cca-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="58cca-158">Input</span></span> | <span data-ttu-id="58cca-159">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="58cca-159">1 to 8</span></span> | <span data-ttu-id="58cca-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="58cca-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="58cca-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="58cca-161">ScaleTensor</span></span> | <span data-ttu-id="58cca-162">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="58cca-162">Optional input</span></span> | <span data-ttu-id="58cca-163">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="58cca-163">1 to 8</span></span> | <span data-ttu-id="58cca-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="58cca-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="58cca-165">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="58cca-165">BiasTensor</span></span> | <span data-ttu-id="58cca-166">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="58cca-166">Optional input</span></span> | <span data-ttu-id="58cca-167">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="58cca-167">1 to 8</span></span> | <span data-ttu-id="58cca-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="58cca-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="58cca-169">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="58cca-169">OutputTensor</span></span> | <span data-ttu-id="58cca-170">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="58cca-170">Output</span></span> | <span data-ttu-id="58cca-171">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="58cca-171">1 to 8</span></span> | <span data-ttu-id="58cca-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="58cca-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="58cca-173">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="58cca-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="58cca-174">Tensor</span><span class="sxs-lookup"><span data-stu-id="58cca-174">Tensor</span></span> | <span data-ttu-id="58cca-175">Typ</span><span class="sxs-lookup"><span data-stu-id="58cca-175">Kind</span></span> | <span data-ttu-id="58cca-176">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="58cca-176">Supported dimension counts</span></span> | <span data-ttu-id="58cca-177">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="58cca-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="58cca-178">InputTensor</span><span class="sxs-lookup"><span data-stu-id="58cca-178">InputTensor</span></span> | <span data-ttu-id="58cca-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="58cca-179">Input</span></span> | <span data-ttu-id="58cca-180">4</span><span class="sxs-lookup"><span data-stu-id="58cca-180">4</span></span> | <span data-ttu-id="58cca-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="58cca-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="58cca-182">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="58cca-182">ScaleTensor</span></span> | <span data-ttu-id="58cca-183">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="58cca-183">Optional input</span></span> | <span data-ttu-id="58cca-184">4</span><span class="sxs-lookup"><span data-stu-id="58cca-184">4</span></span> | <span data-ttu-id="58cca-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="58cca-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="58cca-186">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="58cca-186">BiasTensor</span></span> | <span data-ttu-id="58cca-187">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="58cca-187">Optional input</span></span> | <span data-ttu-id="58cca-188">4</span><span class="sxs-lookup"><span data-stu-id="58cca-188">4</span></span> | <span data-ttu-id="58cca-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="58cca-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="58cca-190">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="58cca-190">OutputTensor</span></span> | <span data-ttu-id="58cca-191">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="58cca-191">Output</span></span> | <span data-ttu-id="58cca-192">4</span><span class="sxs-lookup"><span data-stu-id="58cca-192">4</span></span> | <span data-ttu-id="58cca-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="58cca-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="58cca-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58cca-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="58cca-195">**Header**</span><span class="sxs-lookup"><span data-stu-id="58cca-195">**Header**</span></span> | <span data-ttu-id="58cca-196">directml.h</span><span class="sxs-lookup"><span data-stu-id="58cca-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="58cca-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58cca-197">See also</span></span>

[<span data-ttu-id="58cca-198">Verwenden von Fused-Operatoren zur Verbesserung der Leistung</span><span class="sxs-lookup"><span data-stu-id="58cca-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)