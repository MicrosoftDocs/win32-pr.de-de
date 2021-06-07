---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Berechnet Backpropagation-Farbverläufe für das durchschnittliche Pooling (siehe [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
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
ms.openlocfilehash: aaa2b5d2becac421214afe7c643426c1c93cf899
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417735"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="856ce-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="856ce-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="856ce-104">Berechnet Backpropagation-Farbverläufe für das durchschnittliche Pooling (siehe [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="856ce-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="856ce-105">Betrachten Sie eine **2x2-DML_AVERAGE_POOLING_OPERATOR_DESC**, ohne Auffüllung und einen Schritt von 1, der Folgendes ausführt.</span><span class="sxs-lookup"><span data-stu-id="856ce-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="856ce-106">Jedes 2x2-Fenster im Eingabe-Tensor wird gemittelt, um ein Element der Ausgabe zu erzeugen (Nullen für Elemente außerhalb des Rands).</span><span class="sxs-lookup"><span data-stu-id="856ce-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="856ce-107">Hier ist ein Beispiel für die Ausgabe von **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** mit ähnlichen Parametern angegeben.</span><span class="sxs-lookup"><span data-stu-id="856ce-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="856ce-108">Beachten Sie, dass die Werte im *OutputGradientTensor* die gewichteten Beiträge dieses Elements zum *OutputTensor* während des ursprünglichen [DML_AVERAGE_POOLING_OPERATOR_DESC-Operators](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) darstellen.</span><span class="sxs-lookup"><span data-stu-id="856ce-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="856ce-109">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="856ce-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="856ce-110">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="856ce-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="856ce-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="856ce-111">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="856ce-112">Member</span><span class="sxs-lookup"><span data-stu-id="856ce-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="856ce-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="856ce-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="856ce-114">Der eingehende Farbverlaufs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="856ce-114">The incoming gradient tensor.</span></span> <span data-ttu-id="856ce-115">Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorangehenden Ebene abgerufen.</span><span class="sxs-lookup"><span data-stu-id="856ce-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="856ce-116">In der Regel hat dieser Tensor die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) im Vorwärtsdurchlauf.</span><span class="sxs-lookup"><span data-stu-id="856ce-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="856ce-117">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="856ce-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="856ce-118">Ein Ausgabe-Tensor, der die Zurückpropagierten Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="856ce-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="856ce-119">In der Regel hat dieser Tensor die gleichen Größen wie die *Eingabe* der entsprechenden [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) im Vorwärtsdurchlauf.</span><span class="sxs-lookup"><span data-stu-id="856ce-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="856ce-120">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="856ce-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="856ce-121">Die Anzahl der Elemente in den Arrays *Strides,* *WindowSize,* *StartPadding* und *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="856ce-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="856ce-122">Dieser Wert muss der Anzahl räumlicher Dimensionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="856ce-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="856ce-123">Die Anzahl räumlicher Dimensionen ist 2, wenn 4D-Tensoren bereitgestellt werden, oder 3, wenn 5D-Tensoren bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="856ce-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="856ce-124">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="856ce-124">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="856ce-125">Weitere Informationen finden Sie unter *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="856ce-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="856ce-126">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="856ce-126">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="856ce-127">Weitere Informationen finden Sie unter *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="856ce-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="856ce-128">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="856ce-128">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="856ce-129">Weitere Informationen finden Sie unter *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="856ce-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="856ce-130">Typ: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="856ce-130">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="856ce-131">Weitere Informationen finden Sie unter *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="856ce-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="856ce-132">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="856ce-132">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="856ce-133">Weitere Informationen finden Sie unter *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="856ce-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="856ce-134">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="856ce-134">Availability</span></span>
<span data-ttu-id="856ce-135">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="856ce-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="856ce-136">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="856ce-136">Tensor constraints</span></span>
<span data-ttu-id="856ce-137">*InputGradientTensor* und *OutputGradientTensor* müssen den gleichen *DataType* und *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="856ce-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="856ce-138">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="856ce-138">Tensor support</span></span>
| <span data-ttu-id="856ce-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="856ce-139">Tensor</span></span> | <span data-ttu-id="856ce-140">Typ</span><span class="sxs-lookup"><span data-stu-id="856ce-140">Kind</span></span> | <span data-ttu-id="856ce-141">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="856ce-141">Supported dimension counts</span></span> | <span data-ttu-id="856ce-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="856ce-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="856ce-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="856ce-143">InputGradientTensor</span></span> | <span data-ttu-id="856ce-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="856ce-144">Input</span></span> | <span data-ttu-id="856ce-145">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="856ce-145">4 to 5</span></span> | <span data-ttu-id="856ce-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="856ce-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="856ce-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="856ce-147">OutputGradientTensor</span></span> | <span data-ttu-id="856ce-148">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="856ce-148">Output</span></span> | <span data-ttu-id="856ce-149">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="856ce-149">4 to 5</span></span> | <span data-ttu-id="856ce-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="856ce-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="856ce-151">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="856ce-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="856ce-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="856ce-152">**Header**</span></span> | <span data-ttu-id="856ce-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="856ce-153">directml.h</span></span> |