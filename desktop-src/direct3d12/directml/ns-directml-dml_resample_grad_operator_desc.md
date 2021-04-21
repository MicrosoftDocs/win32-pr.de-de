---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Berechnet Backpropagation-Farbverläufe für Resample (siehe [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
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
ms.openlocfilehash: 0caba1a560b72a94ed04cacd824414964af82c35
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804053"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="05c33-103">DML_RESAMPLE_GRAD_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="05c33-103">DML_RESAMPLE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="05c33-104">Berechnet Backpropagation-Farbverläufe für Resample (siehe [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="05c33-104">Computes backpropagation gradients for Resample (see [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span></span>

<span data-ttu-id="05c33-105">**DML_RESAMPLE1_OPERATOR_DESC** skaliert beliebige Dimensionen des Eingabe-Tensors mithilfe von Nearest-Neighbor-Sampling oder bilinearer Interpolation neu.</span><span class="sxs-lookup"><span data-stu-id="05c33-105">**DML_RESAMPLE1_OPERATOR_DESC** rescales arbitrary dimensions of the input tensor using either nearest-neighbor sampling or bilinear interpolation.</span></span> <span data-ttu-id="05c33-106">Bei einem *InputGradientTensor* mit denselben Größen wie die *Ausgabe* eines entsprechenden **DML_RESAMPLE1_OPERATOR_DESC** erzeugt dieser Operator einen *OutputGradientTensor* mit den gleichen Größen wie die *Eingabe* des **DML_RESAMPLE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="05c33-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_RESAMPLE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of the **DML_RESAMPLE1_OPERATOR_DESC**.</span></span>

<span data-ttu-id="05c33-107">Betrachten Sie beispielsweise eine **DML_RESAMPLE1_OPERATOR_DESC,** die eine nächsthöheren Nachbarskalierung von 1,5x in der Breite und 0,5x in der Höhe ausführt.</span><span class="sxs-lookup"><span data-stu-id="05c33-107">As an example, consider a **DML_RESAMPLE1_OPERATOR_DESC** that performs a nearest-neighbor scaling of 1.5x in the width, and 0.5x in the height.</span></span>

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

<span data-ttu-id="05c33-108">Beachten Sie, dass das 0. Element des Eingabe-Tensors (mit dem Wert 1) zu zwei Elementen in der Ausgabe beiträgt, das erste Element (mit dem Wert 2) zu einem Element in der Ausgabe und das zweite und dritte Element (mit den Werten 3 und 4) zu keinen Elementen der Ausgabe beitragen.</span><span class="sxs-lookup"><span data-stu-id="05c33-108">Notice how the 0th element of the input tensor (with value 1) contributes to two elements in the output, the 1st element (with value 2) contributes to one element in the output, and the 2nd and 3rd elements (with values 3 and 4) contribute to no elements of the output.</span></span>

<span data-ttu-id="05c33-109">Der entsprechende **DML_RESAMPLE_GRAD_OPERATOR_DESC** würde Folgendes ausführen.</span><span class="sxs-lookup"><span data-stu-id="05c33-109">The corresponding **DML_RESAMPLE_GRAD_OPERATOR_DESC** would perform the following.</span></span>

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

<span data-ttu-id="05c33-110">Beachten Sie, dass die Werte im *OutputGradientTensor* die gewichteten Beiträge dieses Elements zum *OutputTensor* während des ursprünglichen **DML_RESAMPLE1_OPERATOR_DESC-Operators** darstellen.</span><span class="sxs-lookup"><span data-stu-id="05c33-110">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original **DML_RESAMPLE1_OPERATOR_DESC** operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05c33-111">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="05c33-111">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="05c33-112">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="05c33-112">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="05c33-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="05c33-113">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="05c33-114">Member</span><span class="sxs-lookup"><span data-stu-id="05c33-114">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="05c33-115">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="05c33-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="05c33-116">Der eingehende Farbverlaufs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="05c33-116">The incoming gradient tensor.</span></span> <span data-ttu-id="05c33-117">Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorangehenden Ebene abgerufen.</span><span class="sxs-lookup"><span data-stu-id="05c33-117">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="05c33-118">In der Regel hat dieser Tensor die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) im Vorwärtsdurchlauf.</span><span class="sxs-lookup"><span data-stu-id="05c33-118">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="05c33-119">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="05c33-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="05c33-120">Ein Ausgabe-Tensor, der die Zurückpropagierten Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="05c33-120">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="05c33-121">In der Regel hat dieser Tensor  die gleichen Größen wie die Eingabe des entsprechenden DML_RESAMPLE1_OPERATOR_DESC [im](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) Vorwärtspass.</span><span class="sxs-lookup"><span data-stu-id="05c33-121">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`InterpolationMode`

<span data-ttu-id="05c33-122">Typ: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="05c33-122">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="05c33-123">Weitere Informationen *finden Sie unter InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05c33-123">See *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`DimensionCount`

<span data-ttu-id="05c33-124">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="05c33-124">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="05c33-125">Die Anzahl der Elemente in den *Arrays Scales,* *InputPixelOffsets* und *OutputPixelOffsets.*</span><span class="sxs-lookup"><span data-stu-id="05c33-125">The number of elements in the *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* arrays.</span></span> <span data-ttu-id="05c33-126">Dieser Wert muss dem *DimensionCount-Wert in* *InputGradientTensor* und *OutputGradientTensor entspricht.*</span><span class="sxs-lookup"><span data-stu-id="05c33-126">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`Scales`

<span data-ttu-id="05c33-127">Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="05c33-127">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="05c33-128">Weitere Informationen finden Sie unter *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05c33-128">See *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`InputPixelOffsets`

<span data-ttu-id="05c33-129">Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="05c33-129">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="05c33-130">Weitere Informationen finden Sie unter *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05c33-130">See *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`OutputPixelOffsets`

<span data-ttu-id="05c33-131">Typ: \_ \_ Feldgröße \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="05c33-131">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="05c33-132">Weitere Informationen finden Sie unter *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05c33-132">See *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="05c33-133">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="05c33-133">Availability</span></span>
<span data-ttu-id="05c33-134">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="05c33-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="05c33-135">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="05c33-135">Tensor constraints</span></span>
<span data-ttu-id="05c33-136">*InputGradientTensor und* *OutputGradientTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="05c33-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="05c33-137">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="05c33-137">Tensor support</span></span>
| <span data-ttu-id="05c33-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="05c33-138">Tensor</span></span> | <span data-ttu-id="05c33-139">Typ</span><span class="sxs-lookup"><span data-stu-id="05c33-139">Kind</span></span> | <span data-ttu-id="05c33-140">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="05c33-140">Supported dimension counts</span></span> | <span data-ttu-id="05c33-141">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="05c33-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="05c33-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="05c33-142">InputGradientTensor</span></span> | <span data-ttu-id="05c33-143">Eingabe</span><span class="sxs-lookup"><span data-stu-id="05c33-143">Input</span></span> | <span data-ttu-id="05c33-144">4</span><span class="sxs-lookup"><span data-stu-id="05c33-144">4</span></span> | <span data-ttu-id="05c33-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="05c33-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="05c33-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="05c33-146">OutputGradientTensor</span></span> | <span data-ttu-id="05c33-147">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="05c33-147">Output</span></span> | <span data-ttu-id="05c33-148">4</span><span class="sxs-lookup"><span data-stu-id="05c33-148">4</span></span> | <span data-ttu-id="05c33-149">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="05c33-149">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="05c33-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05c33-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="05c33-151">**Header**</span><span class="sxs-lookup"><span data-stu-id="05c33-151">**Header**</span></span> | <span data-ttu-id="05c33-152">directml.h</span><span class="sxs-lookup"><span data-stu-id="05c33-152">directml.h</span></span> |