---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Führt eine Mean-Varianz Normalisierungsfunktion für den eingabetensor aus. Dieser Operator berechnet den Mittelwert und die Varianz des Eingabe Mandanten, um die Normalisierung auszuführen.
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
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106373409"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="ca818-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="ca818-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="ca818-105">Führt eine Mean-Varianz Normalisierungsfunktion für den eingabetensor aus.</span><span class="sxs-lookup"><span data-stu-id="ca818-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="ca818-106">Dieser Operator berechnet den Mittelwert und die Varianz des Eingabe Mandanten, um die Normalisierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ca818-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="ca818-107">Dieser Operator führt die folgende Berechnung aus.</span><span class="sxs-lookup"><span data-stu-id="ca818-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="ca818-108">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="ca818-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="ca818-109">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ca818-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca818-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca818-110">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="ca818-111">Member</span><span class="sxs-lookup"><span data-stu-id="ca818-111">Members</span></span>

`InputTensor`

<span data-ttu-id="ca818-112">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca818-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca818-113">Ein tensorflow, der die Eingabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="ca818-113">A tensor containing the Input data.</span></span> <span data-ttu-id="ca818-114">Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="ca818-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`ScaleTensor`

<span data-ttu-id="ca818-115">Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca818-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca818-116">Ein optionaler tensorflow, der die Skalierungs Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ca818-116">An optional tensor containing the Scale data.</span></span> <span data-ttu-id="ca818-117">Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="ca818-117">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="ca818-118">Jede Dimension kann durch 1 ersetzt werden, um Sie in dieser Dimension zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="ca818-118">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="ca818-119">Dieser tensorflow ist erforderlich, wenn der *biastensor* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca818-119">This tensor is required if the *BiasTensor* is used.</span></span>


`BiasTensor`

<span data-ttu-id="ca818-120">Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca818-120">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca818-121">Ein optionaler tensorflow, der die Daten der Bias enthält.</span><span class="sxs-lookup"><span data-stu-id="ca818-121">An optional tensor containing the bias data.</span></span> <span data-ttu-id="ca818-122">Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="ca818-122">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="ca818-123">Jede Dimension kann durch 1 ersetzt werden, um Sie in dieser Dimension zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="ca818-123">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="ca818-124">Dieser tensorflow ist erforderlich, wenn der *scaletensor* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca818-124">This tensor is required if the *ScaleTensor* is used.</span></span>


`OutputTensor`

<span data-ttu-id="ca818-125">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca818-125">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca818-126">Ein tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ca818-126">A tensor to write the results to.</span></span> <span data-ttu-id="ca818-127">Die Dimensionen dieses Mandanten sind `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="ca818-127">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`AxisCount`

<span data-ttu-id="ca818-128">Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="ca818-128">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="ca818-129">Die Anzahl der Achsen.</span><span class="sxs-lookup"><span data-stu-id="ca818-129">The number of axes.</span></span> <span data-ttu-id="ca818-130">Dieses Feld bestimmt die Größe des *Achsen* Arrays.</span><span class="sxs-lookup"><span data-stu-id="ca818-130">This field determines the size of the *Axes* array.</span></span>


`Axes`

<span data-ttu-id="ca818-131">Type: \_ Field \_ size \_ (axiscount) **Konstanten [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="ca818-131">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span> 

<span data-ttu-id="ca818-132">Die Achsen, an denen der Mittelwert und die Varianz berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ca818-132">The axes along which to calculate the Mean and Variance.</span></span>


`NormalizeVariance`

<span data-ttu-id="ca818-133">Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="ca818-133">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="ca818-134">**True** , wenn die normalisierungs Ebene Abweichungen in der normalisierungs Berechnung einschließt.</span><span class="sxs-lookup"><span data-stu-id="ca818-134">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="ca818-135">Andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ca818-135">Otherwise, **FALSE**.</span></span> <span data-ttu-id="ca818-136">**False** gibt an, dass die normalisierungs Gleichung ist `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="ca818-136">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>


`Epsilon`

<span data-ttu-id="ca818-137">Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="ca818-137">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="ca818-138">Der Epsilon-Wert, der verwendet wird, um die Division durch Null zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="ca818-138">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="ca818-139">Der Wert 0,00001 wird als Standardwert empfohlen.</span><span class="sxs-lookup"><span data-stu-id="ca818-139">A value of 0.00001 is recommended as default.</span></span>


`FusedActivation`

<span data-ttu-id="ca818-140">Type: \_ maybenull \_ **Konstanten [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca818-140">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="ca818-141">Eine optionale, bei der Normalisierung anzuwendende, Fused-Aktivierungs Schicht.</span><span class="sxs-lookup"><span data-stu-id="ca818-141">An optional fused activation layer to apply after the normalization.</span></span>


## <a name="remarks"></a><span data-ttu-id="ca818-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca818-142">Remarks</span></span>
<span data-ttu-id="ca818-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** ist eine supermenge der Funktionen von [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="ca818-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="ca818-144">Hier ist das Festlegen des **Achsen** Arrays `{ 0, 2, 3 }` auf das Äquivalent der Einstellung von " *Crosschannel* " auf " **false** " in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; beim Festlegen des **Achsen** Arrays auf entspricht das Festlegen `{ 1, 2, 3 }` von " *Crosschannel* " auf " **true**".</span><span class="sxs-lookup"><span data-stu-id="ca818-144">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="ca818-145">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ca818-145">Availability</span></span>
<span data-ttu-id="ca818-146">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ca818-146">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ca818-147">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="ca818-147">Tensor constraints</span></span>
* <span data-ttu-id="ca818-148">*Inputtensor* und *outputtensor* müssen über die gleichen *Größen* verfügen.</span><span class="sxs-lookup"><span data-stu-id="ca818-148">*InputTensor* and *OutputTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="ca818-149">' *Biastensor*', ' *inputtensor*', ' *outputtensor*' und ' *scaletensor* ' müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ca818-149">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ca818-150">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ca818-150">Tensor support</span></span>
| <span data-ttu-id="ca818-151">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="ca818-151">Tensor</span></span> | <span data-ttu-id="ca818-152">Typ</span><span class="sxs-lookup"><span data-stu-id="ca818-152">Kind</span></span> | <span data-ttu-id="ca818-153">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="ca818-153">Dimensions</span></span> | <span data-ttu-id="ca818-154">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="ca818-154">Supported dimension counts</span></span> | <span data-ttu-id="ca818-155">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="ca818-155">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="ca818-156">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="ca818-156">InputTensor</span></span> | <span data-ttu-id="ca818-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca818-157">Input</span></span> | <span data-ttu-id="ca818-158">{BatchCount, ChannelCount, Height, Width}</span><span class="sxs-lookup"><span data-stu-id="ca818-158">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="ca818-159">4</span><span class="sxs-lookup"><span data-stu-id="ca818-159">4</span></span> | <span data-ttu-id="ca818-160">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ca818-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ca818-161">Scaletensor</span><span class="sxs-lookup"><span data-stu-id="ca818-161">ScaleTensor</span></span> | <span data-ttu-id="ca818-162">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca818-162">Optional input</span></span> | <span data-ttu-id="ca818-163">{Scalebatchcount, scalechannelcount, ScaleHeight, ScaleWidth}</span><span class="sxs-lookup"><span data-stu-id="ca818-163">{ ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth }</span></span> | <span data-ttu-id="ca818-164">4</span><span class="sxs-lookup"><span data-stu-id="ca818-164">4</span></span> | <span data-ttu-id="ca818-165">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ca818-165">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ca818-166">Biastensor</span><span class="sxs-lookup"><span data-stu-id="ca818-166">BiasTensor</span></span> | <span data-ttu-id="ca818-167">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca818-167">Optional input</span></span> | <span data-ttu-id="ca818-168">{Biasbatchcount, biaschannelcount, biasheight, biaswidth}</span><span class="sxs-lookup"><span data-stu-id="ca818-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span></span> | <span data-ttu-id="ca818-169">4</span><span class="sxs-lookup"><span data-stu-id="ca818-169">4</span></span> | <span data-ttu-id="ca818-170">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ca818-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ca818-171">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="ca818-171">OutputTensor</span></span> | <span data-ttu-id="ca818-172">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="ca818-172">Output</span></span> | <span data-ttu-id="ca818-173">{BatchCount, ChannelCount, Height, Width}</span><span class="sxs-lookup"><span data-stu-id="ca818-173">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="ca818-174">4</span><span class="sxs-lookup"><span data-stu-id="ca818-174">4</span></span> | <span data-ttu-id="ca818-175">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ca818-175">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="ca818-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca818-176">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ca818-177">**Header**</span><span class="sxs-lookup"><span data-stu-id="ca818-177">**Header**</span></span> | <span data-ttu-id="ca818-178">directml. h</span><span class="sxs-lookup"><span data-stu-id="ca818-178">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ca818-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca818-179">See also</span></span>

[<span data-ttu-id="ca818-180">Verwenden von Fused-Operatoren zur Verbesserung der Leistung</span><span class="sxs-lookup"><span data-stu-id="ca818-180">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)