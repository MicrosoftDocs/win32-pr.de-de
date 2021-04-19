---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Berechnet backpropagierungs Gradienten für Resample (siehe [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 5808381f2e812ac20399b46672e51acd063bc6a5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351832"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="e0bad-103">DML_RESAMPLE_GRAD_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="e0bad-103">DML_RESAMPLE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e0bad-104">Berechnet backpropagierungs Gradienten für Resample (siehe [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="e0bad-104">Computes backpropagation gradients for Resample (see [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span></span>

<span data-ttu-id="e0bad-105">**DML_RESAMPLE1_OPERATOR_DESC** beliebige Dimensionen des Eingabe Mandanten mithilfe von "Next-Neighbor"-Stichproben oder der bilinearen Interpolations Option neu.</span><span class="sxs-lookup"><span data-stu-id="e0bad-105">**DML_RESAMPLE1_OPERATOR_DESC** rescales arbitrary dimensions of the input tensor using either nearest-neighbor sampling or bilinear interpolation.</span></span> <span data-ttu-id="e0bad-106">Wenn ein *inputgradienttensor* mit denselben Größen wie die *Ausgabe* eines äquivalenten **DML_RESAMPLE1_OPERATOR_DESC** angegeben wird, erzeugt dieser Operator einen *outputgradienttensor* mit denselben Größen wie die *Eingabe* des **DML_RESAMPLE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="e0bad-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_RESAMPLE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of the **DML_RESAMPLE1_OPERATOR_DESC**.</span></span>

<span data-ttu-id="e0bad-107">Nehmen Sie als Beispiel eine **DML_RESAMPLE1_OPERATOR_DESC** , die eine Skalierung mit dem nächstgelegenen Nachbar Wert von 1,5 x in der Breite und 0,5 x in der Höhe ausführt.</span><span class="sxs-lookup"><span data-stu-id="e0bad-107">As an example, consider a **DML_RESAMPLE1_OPERATOR_DESC** that performs a nearest-neighbor scaling of 1.5x in the width, and 0.5x in the height.</span></span>

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

<span data-ttu-id="e0bad-108">Beachten Sie, dass das nullten-Element des Eingabe Mandanten (mit Wert 1) zu zwei Elementen in der Ausgabe beiträgt, das erste Element (mit Wert 2) zu einem Element in der Ausgabe beiträgt und das 2. und dritte Element (mit den Werten 3 und 4) zu keinen Elementen der Ausgabe beiträgt.</span><span class="sxs-lookup"><span data-stu-id="e0bad-108">Notice how the 0th element of the input tensor (with value 1) contributes to two elements in the output, the 1st element (with value 2) contributes to one element in the output, and the 2nd and 3rd elements (with values 3 and 4) contribute to no elements of the output.</span></span>

<span data-ttu-id="e0bad-109">Die entsprechende **DML_RESAMPLE_GRAD_OPERATOR_DESC** würde Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="e0bad-109">The corresponding **DML_RESAMPLE_GRAD_OPERATOR_DESC** would perform the following.</span></span>

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

<span data-ttu-id="e0bad-110">Beachten Sie, dass die Werte im *outputgradienttensor* die gewichteten Beiträge dieses Elements für *outputtensor* während des ursprünglichen **DML_RESAMPLE1_OPERATOR_DESC** Operators darstellen.</span><span class="sxs-lookup"><span data-stu-id="e0bad-110">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original **DML_RESAMPLE1_OPERATOR_DESC** operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0bad-111">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="e0bad-111">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e0bad-112">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e0bad-112">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0bad-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0bad-113">Syntax</span></span>

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a><span data-ttu-id="e0bad-114">Member</span><span class="sxs-lookup"><span data-stu-id="e0bad-114">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="e0bad-115">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e0bad-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e0bad-116">Der eingehende gradiententensor.</span><span class="sxs-lookup"><span data-stu-id="e0bad-116">The incoming gradient tensor.</span></span> <span data-ttu-id="e0bad-117">Dies wird in der Regel aus der Ausgabe der Rück Propagierung einer vorangehenden Ebene abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e0bad-117">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="e0bad-118">In der Regel hat dieser tensorflow die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) im Forward-Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="e0bad-118">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="e0bad-119">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e0bad-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e0bad-120">Ein Ausgabe Mandanten, der die zurückgegebenen Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="e0bad-120">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="e0bad-121">In der Regel hat dieser Mandanten die gleichen Größen wie die *Eingabe* der entsprechenden [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) im Forward-Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="e0bad-121">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`InterpolationMode`

<span data-ttu-id="e0bad-122">Typ: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="e0bad-122">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="e0bad-123">Siehe *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="e0bad-123">See *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`DimensionCount`

<span data-ttu-id="e0bad-124">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e0bad-124">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="e0bad-125">Die Anzahl der Elemente in den Arrays *Skalen*, *inputpixeloffsets* und *outputpixeloffsets* .</span><span class="sxs-lookup"><span data-stu-id="e0bad-125">The number of elements in the *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* arrays.</span></span> <span data-ttu-id="e0bad-126">Dieser Wert muss mit der *DimensionCount* übereinstimmen, die in *inputgradienttensor* und *outputgradienttensor* bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e0bad-126">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`Scales`

<span data-ttu-id="e0bad-127">Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e0bad-127">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="e0bad-128">Siehe *Skalen* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="e0bad-128">See *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`InputPixelOffsets`

<span data-ttu-id="e0bad-129">Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e0bad-129">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="e0bad-130">Weitere Informationen finden Sie unter *inputpixeloffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="e0bad-130">See *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`OutputPixelOffsets`

<span data-ttu-id="e0bad-131">Type: \_ Field \_ size \_ (DimensionCount) **Konstanten [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e0bad-131">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="e0bad-132">Weitere Informationen finden Sie unter *outputpixeloffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="e0bad-132">See *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="e0bad-133">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="e0bad-133">Availability</span></span>
<span data-ttu-id="e0bad-134">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="e0bad-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e0bad-135">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="e0bad-135">Tensor constraints</span></span>
<span data-ttu-id="e0bad-136">*Inputgradienttensor* und *outputgradienttensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e0bad-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e0bad-137">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="e0bad-137">Tensor support</span></span>
| <span data-ttu-id="e0bad-138">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="e0bad-138">Tensor</span></span> | <span data-ttu-id="e0bad-139">Typ</span><span class="sxs-lookup"><span data-stu-id="e0bad-139">Kind</span></span> | <span data-ttu-id="e0bad-140">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="e0bad-140">Supported dimension counts</span></span> | <span data-ttu-id="e0bad-141">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="e0bad-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e0bad-142">Input gradienttensor</span><span class="sxs-lookup"><span data-stu-id="e0bad-142">InputGradientTensor</span></span> | <span data-ttu-id="e0bad-143">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0bad-143">Input</span></span> | <span data-ttu-id="e0bad-144">4</span><span class="sxs-lookup"><span data-stu-id="e0bad-144">4</span></span> | <span data-ttu-id="e0bad-145">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e0bad-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e0bad-146">Outputgradienttensor</span><span class="sxs-lookup"><span data-stu-id="e0bad-146">OutputGradientTensor</span></span> | <span data-ttu-id="e0bad-147">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e0bad-147">Output</span></span> | <span data-ttu-id="e0bad-148">4</span><span class="sxs-lookup"><span data-stu-id="e0bad-148">4</span></span> | <span data-ttu-id="e0bad-149">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e0bad-149">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="e0bad-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0bad-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e0bad-151">**Header**</span><span class="sxs-lookup"><span data-stu-id="e0bad-151">**Header**</span></span> | <span data-ttu-id="e0bad-152">directml. h</span><span class="sxs-lookup"><span data-stu-id="e0bad-152">directml.h</span></span> |