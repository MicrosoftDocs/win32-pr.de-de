---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Berechnet Backpropagation-Farbverläufe für durchschnittliches Pooling (siehe [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 5c2803fc300ca862d54a74aee1c864e9097e3d8e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803370"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="02ba1-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="02ba1-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="02ba1-104">Berechnet Backpropagation-Farbverläufe für durchschnittliches Pooling (siehe [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="02ba1-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="02ba1-105">Betrachten Sie eine **2x2-DML_AVERAGE_POOLING_OPERATOR_DESC**, ohne Auf padding und einen Schritt von 1, der Folgendes ausführt.</span><span class="sxs-lookup"><span data-stu-id="02ba1-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="02ba1-106">Jedes 2x2-Fenster im Eingabe tensor wird gemittelt, um ein Element der Ausgabe zu erzeugen (nullen für Elemente außerhalb des Edges zu lesen).</span><span class="sxs-lookup"><span data-stu-id="02ba1-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="02ba1-107">Im Folgenden finden Sie ein Beispiel für die Ausgabe **von** DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC mit ähnlichen Parametern.</span><span class="sxs-lookup"><span data-stu-id="02ba1-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="02ba1-108">Beachten Sie, dass die Werte im *OutputGradientTensor* die gewichteten Beiträge dieses Elements zum *OutputTensor* während des ursprünglichen DML_AVERAGE_POOLING_OPERATOR_DESC [darstellen.](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="02ba1-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02ba1-109">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="02ba1-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="02ba1-110">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="02ba1-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="02ba1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="02ba1-111">Syntax</span></span>

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a><span data-ttu-id="02ba1-112">Member</span><span class="sxs-lookup"><span data-stu-id="02ba1-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="02ba1-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="02ba1-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="02ba1-114">Der eingehende Farbverlaufs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="02ba1-114">The incoming gradient tensor.</span></span> <span data-ttu-id="02ba1-115">Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorherigen Ebene ermittelt.</span><span class="sxs-lookup"><span data-stu-id="02ba1-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="02ba1-116">In der Regel hat dieser Tensor  die gleichen Größen wie die Ausgabe des entsprechenden DML_AVERAGE_POOLING_OPERATOR_DESC [im](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) Vorwärtspass.</span><span class="sxs-lookup"><span data-stu-id="02ba1-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="02ba1-117">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="02ba1-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="02ba1-118">Ein Ausgabe tensor, der die zurückpropagierten Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="02ba1-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="02ba1-119">In der Regel hat dieser Tensor  die gleichen Größen wie die Eingabe des entsprechenden DML_AVERAGE_POOLING_OPERATOR_DESC [im](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) Vorwärtspass.</span><span class="sxs-lookup"><span data-stu-id="02ba1-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="02ba1-120">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="02ba1-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="02ba1-121">Die Anzahl der Elemente in den *Arrays Strides,* *WindowSize,* *StartPadding* und *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="02ba1-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="02ba1-122">Dieser Wert muss der Anzahl räumlicher Dimensionen entspricht.</span><span class="sxs-lookup"><span data-stu-id="02ba1-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="02ba1-123">Die Anzahl räumlicher Dimensionen beträgt 2, wenn 4D-Tensoren bereitgestellt werden, oder 3, wenn 5D-Tensoren bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="02ba1-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="02ba1-124">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="02ba1-124">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="02ba1-125">Weitere Informationen finden Sie unter *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="02ba1-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="02ba1-126">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="02ba1-126">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="02ba1-127">Weitere Informationen finden Sie unter *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="02ba1-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="02ba1-128">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="02ba1-128">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="02ba1-129">Weitere Informationen finden Sie unter *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="02ba1-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="02ba1-130">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="02ba1-130">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="02ba1-131">Weitere Informationen finden Sie unter *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="02ba1-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="02ba1-132">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="02ba1-132">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="02ba1-133">Weitere Informationen finden Sie unter *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="02ba1-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="02ba1-134">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="02ba1-134">Availability</span></span>
<span data-ttu-id="02ba1-135">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="02ba1-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="02ba1-136">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="02ba1-136">Tensor constraints</span></span>
<span data-ttu-id="02ba1-137">*InputGradientTensor* und *OutputGradientTensor* müssen den gleichen *DataType* und *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="02ba1-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="02ba1-138">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="02ba1-138">Tensor support</span></span>
| <span data-ttu-id="02ba1-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="02ba1-139">Tensor</span></span> | <span data-ttu-id="02ba1-140">Typ</span><span class="sxs-lookup"><span data-stu-id="02ba1-140">Kind</span></span> | <span data-ttu-id="02ba1-141">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="02ba1-141">Supported dimension counts</span></span> | <span data-ttu-id="02ba1-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="02ba1-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="02ba1-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="02ba1-143">InputGradientTensor</span></span> | <span data-ttu-id="02ba1-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02ba1-144">Input</span></span> | <span data-ttu-id="02ba1-145">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="02ba1-145">4 to 5</span></span> | <span data-ttu-id="02ba1-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="02ba1-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="02ba1-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="02ba1-147">OutputGradientTensor</span></span> | <span data-ttu-id="02ba1-148">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="02ba1-148">Output</span></span> | <span data-ttu-id="02ba1-149">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="02ba1-149">4 to 5</span></span> | <span data-ttu-id="02ba1-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="02ba1-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="02ba1-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02ba1-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="02ba1-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="02ba1-152">**Header**</span></span> | <span data-ttu-id="02ba1-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="02ba1-153">directml.h</span></span> |