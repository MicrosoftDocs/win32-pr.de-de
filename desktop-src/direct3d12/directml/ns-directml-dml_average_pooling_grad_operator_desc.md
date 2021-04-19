---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Berechnet backpropagierungs Gradienten für das durchschnittliche Pooling (siehe [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
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
ms.openlocfilehash: 79a43e93f504e8d6f36553a4f672ef7e5845610f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106363828"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="690ed-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="690ed-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="690ed-104">Berechnet backpropagierungs Gradienten für das durchschnittliche Pooling (siehe [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="690ed-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="690ed-105">Angenommen, ein 2 x 2- **DML_AVERAGE_POOLING_OPERATOR_DESC**, ohne Auffüll Zeichen und ein Schritt von 1, der Folgendes ausführt:</span><span class="sxs-lookup"><span data-stu-id="690ed-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="690ed-106">Jedes 2 x 2-Fenster im eingabetensor wird als Mittelwert für ein Element der Ausgabe (Lesevorgänge für Elemente, die über den Rand hinausgehen) erzeugt.</span><span class="sxs-lookup"><span data-stu-id="690ed-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="690ed-107">Im folgenden finden Sie ein Beispiel für die Ausgabe von **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** mit ähnlichen Parametern.</span><span class="sxs-lookup"><span data-stu-id="690ed-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="690ed-108">Beachten Sie, dass die Werte im *outputgradienttensor* die gewichteten Beiträge dieses Elements für *outputtensor* während des ursprünglichen [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) Operators darstellen.</span><span class="sxs-lookup"><span data-stu-id="690ed-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="690ed-109">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="690ed-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="690ed-110">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="690ed-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="690ed-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="690ed-111">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="690ed-112">Member</span><span class="sxs-lookup"><span data-stu-id="690ed-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="690ed-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="690ed-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="690ed-114">Der eingehende gradiententensor.</span><span class="sxs-lookup"><span data-stu-id="690ed-114">The incoming gradient tensor.</span></span> <span data-ttu-id="690ed-115">Dies wird in der Regel aus der Ausgabe der Rück Propagierung einer vorangehenden Ebene abgerufen.</span><span class="sxs-lookup"><span data-stu-id="690ed-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="690ed-116">In der Regel hat dieser tensorflow die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) im Forward-Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="690ed-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="690ed-117">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="690ed-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="690ed-118">Ein Ausgabe Mandanten, der die zurückgegebenen Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="690ed-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="690ed-119">In der Regel hat dieser Mandanten die gleichen Größen wie die *Eingabe* der entsprechenden [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) im Forward-Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="690ed-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="690ed-120">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="690ed-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="690ed-121">Die Anzahl der Elemente *in den Arrays*"Step", " *WindowSize*", " *startpadding*" und " *endpadding* ".</span><span class="sxs-lookup"><span data-stu-id="690ed-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="690ed-122">Dieser Wert muss gleich der Anzahl räumlicher Dimensionen sein.</span><span class="sxs-lookup"><span data-stu-id="690ed-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="690ed-123">Die Anzahl räumlicher Dimensionen ist 2, wenn 4D-Tensoren bereitgestellt werden, oder 3, wenn 5D-Tensoren bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="690ed-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="690ed-124">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="690ed-124">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="690ed-125">Siehe *Schritte* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="690ed-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="690ed-126">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="690ed-126">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="690ed-127">Siehe *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="690ed-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="690ed-128">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="690ed-128">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="690ed-129">Siehe *startpadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="690ed-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="690ed-130">Typ: \_ Field_size \_ (DimensionCount) Konstante **[uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="690ed-130">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="690ed-131">Siehe *endpadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="690ed-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="690ed-132">Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="690ed-132">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="690ed-133">Weitere Informationen finden Sie unter *includepadditions* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="690ed-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="690ed-134">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="690ed-134">Availability</span></span>
<span data-ttu-id="690ed-135">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="690ed-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="690ed-136">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="690ed-136">Tensor constraints</span></span>
<span data-ttu-id="690ed-137">*Inputgradienttensor* und *outputgradienttensor* müssen denselben *Datentyp* und *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="690ed-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="690ed-138">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="690ed-138">Tensor support</span></span>
| <span data-ttu-id="690ed-139">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="690ed-139">Tensor</span></span> | <span data-ttu-id="690ed-140">Typ</span><span class="sxs-lookup"><span data-stu-id="690ed-140">Kind</span></span> | <span data-ttu-id="690ed-141">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="690ed-141">Supported dimension counts</span></span> | <span data-ttu-id="690ed-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="690ed-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="690ed-143">Input gradienttensor</span><span class="sxs-lookup"><span data-stu-id="690ed-143">InputGradientTensor</span></span> | <span data-ttu-id="690ed-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="690ed-144">Input</span></span> | <span data-ttu-id="690ed-145">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="690ed-145">4 to 5</span></span> | <span data-ttu-id="690ed-146">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="690ed-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="690ed-147">Outputgradienttensor</span><span class="sxs-lookup"><span data-stu-id="690ed-147">OutputGradientTensor</span></span> | <span data-ttu-id="690ed-148">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="690ed-148">Output</span></span> | <span data-ttu-id="690ed-149">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="690ed-149">4 to 5</span></span> | <span data-ttu-id="690ed-150">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="690ed-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="690ed-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="690ed-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="690ed-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="690ed-152">**Header**</span></span> | <span data-ttu-id="690ed-153">directml. h</span><span class="sxs-lookup"><span data-stu-id="690ed-153">directml.h</span></span> |