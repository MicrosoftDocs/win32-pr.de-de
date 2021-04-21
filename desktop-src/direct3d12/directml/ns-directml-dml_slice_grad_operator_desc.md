---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Berechnet Backpropagation-Farbverläufe für Slice (siehe [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: a22efe9b0b74f5fdc7b498b97784086f40f243b9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803967"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="c9bd9-103">DML_SLICE_GRAD_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="c9bd9-103">DML_SLICE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="c9bd9-104">Berechnet Backpropagation-Farbverläufe für Slice (siehe [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="c9bd9-104">Computes backpropagation gradients for Slice (see [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span></span>

<span data-ttu-id="c9bd9-105">Denken Sie daran, dass [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) einen Unterbereich eines Eingabe-Tensors extrahiert.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-105">Recall that [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extracts a subregion of an input tensor.</span></span> <span data-ttu-id="c9bd9-106">Bei einem *InputGradientTensor* mit denselben Größen wie die *Ausgabe* eines entsprechenden **DML_SLICE1_OPERATOR_DESC** erzeugt dieser Operator einen *OutputGradientTensor* mit den gleichen Größen wie die *Eingabe* von **DML_SLICE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_SLICE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of **DML_SLICE1_OPERATOR_DESC**.</span></span> <span data-ttu-id="c9bd9-107">Die segmentierten Elemente werden an die Ausgabe weitergegeben, und alle anderen Elemente werden auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-107">The sliced elements are propagated to the output, and all other elements are set to 0.</span></span>

<span data-ttu-id="c9bd9-108">Betrachten Sie beispielsweise einen **DML_SLICE1_OPERATOR_DESC,** der die folgenden Elemente aus einem Tensor extrahiert:</span><span class="sxs-lookup"><span data-stu-id="c9bd9-108">As an example, consider a **DML_SLICE1_OPERATOR_DESC** that extracts the following elements from a tensor:</span></span>

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

<span data-ttu-id="c9bd9-109">Wenn die gleichen *EingabewindowOffsets-Größen* wie im obigen Beispiel angegeben /  /  werden, würde dieser Operator dann die folgende Transformation ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-109">If provided the same *InputWindowOffsets*/*Sizes*/*Strides* as in the above example, this operator would then perform the following transform.</span></span>

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> <span data-ttu-id="c9bd9-110">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="c9bd9-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="c9bd9-111">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="c9bd9-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9bd9-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9bd9-112">Syntax</span></span>

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a><span data-ttu-id="c9bd9-113">Member</span><span class="sxs-lookup"><span data-stu-id="c9bd9-113">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="c9bd9-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c9bd9-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c9bd9-115">Der eingehende Farbverlaufs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-115">The incoming gradient tensor.</span></span> <span data-ttu-id="c9bd9-116">Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorangehenden Ebene abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="c9bd9-117">In der Regel hat dieser Tensor die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) im Vorwärtsdurchlauf.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-117">Typically, this tensor would have the same sizes as the *output* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="c9bd9-118">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c9bd9-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c9bd9-119">Ein Ausgabe-Tensor, der die Zurückpropagierten Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="c9bd9-120">In der Regel hat dieser Tensor die gleichen Größen wie die *Eingabe* der entsprechenden [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) im Vorwärtsdurchlauf.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-120">Typically, this tensor would have the same sizes as the *input* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="c9bd9-121">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c9bd9-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c9bd9-122">Die Anzahl der Elemente in den *Arrays InputWindowOffsets,* *InputWindowSizes* und *InputWindowStrides.*</span><span class="sxs-lookup"><span data-stu-id="c9bd9-122">The number of elements in the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="c9bd9-123">Dieser Wert muss gleich dem *DimensionCount-Wert* sein, der in *InputGradientTensor* und *OutputGradientTensor* bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-123">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`InputWindowOffsets`

<span data-ttu-id="c9bd9-124">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="c9bd9-124">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="c9bd9-125">Weitere *Informationen finden Sie unter InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="c9bd9-125">See *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowSizes`

<span data-ttu-id="c9bd9-126">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="c9bd9-126">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="c9bd9-127">Weitere *Informationen finden Sie unter InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="c9bd9-127">See *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowStrides`

<span data-ttu-id="c9bd9-128">Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="c9bd9-128">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="c9bd9-129">Weitere Informationen finden Sie unter *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="c9bd9-129">See *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

<span data-ttu-id="c9bd9-130">Beachten Sie, **dass DML_SLICE1_OPERATOR_DESC** Operator im Gegensatz zu anderen Strides ungleich 0 (null) erfordert.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-130">Note that unlike **DML_SLICE1_OPERATOR_DESC**, this operator requires non-zero strides.</span></span> <span data-ttu-id="c9bd9-131">Das liegt daran, dass bei einem 0-Schritt nicht eindeutig ist, welches Eingabeelement jedem Ausgabeelement zuordnen soll, und daher kann keine Rückpropagierung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-131">That's because with a zero stride, it's ambiguous as to which input element should map to each output element, and therefore backpropagation can't be performed.</span></span> <span data-ttu-id="c9bd9-132">Wie **DML_SLICE1_OPERATOR_DESC** kippen negative Strides die Richtung des Eingabefensters entlang dieser Achse.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-132">Like **DML_SLICE1_OPERATOR_DESC**, negative strides flip the input window direction along that axis.</span></span>

## <a name="availability"></a><span data-ttu-id="c9bd9-133">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="c9bd9-133">Availability</span></span>
<span data-ttu-id="c9bd9-134">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c9bd9-135">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="c9bd9-135">Tensor constraints</span></span>
<span data-ttu-id="c9bd9-136">*InputGradientTensor und* *OutputGradientTensor* müssen denselben *DataType und* *DimensionCount aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="c9bd9-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c9bd9-137">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="c9bd9-137">Tensor support</span></span>
| <span data-ttu-id="c9bd9-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="c9bd9-138">Tensor</span></span> | <span data-ttu-id="c9bd9-139">Typ</span><span class="sxs-lookup"><span data-stu-id="c9bd9-139">Kind</span></span> | <span data-ttu-id="c9bd9-140">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="c9bd9-140">Supported dimension counts</span></span> | <span data-ttu-id="c9bd9-141">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="c9bd9-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c9bd9-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="c9bd9-142">InputGradientTensor</span></span> | <span data-ttu-id="c9bd9-143">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c9bd9-143">Input</span></span> | <span data-ttu-id="c9bd9-144">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="c9bd9-144">1 to 8</span></span> | <span data-ttu-id="c9bd9-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c9bd9-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c9bd9-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="c9bd9-146">OutputGradientTensor</span></span> | <span data-ttu-id="c9bd9-147">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c9bd9-147">Output</span></span> | <span data-ttu-id="c9bd9-148">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="c9bd9-148">1 to 8</span></span> | <span data-ttu-id="c9bd9-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c9bd9-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="c9bd9-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9bd9-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c9bd9-151">**Header**</span><span class="sxs-lookup"><span data-stu-id="c9bd9-151">**Header**</span></span> | <span data-ttu-id="c9bd9-152">directml.h</span><span class="sxs-lookup"><span data-stu-id="c9bd9-152">directml.h</span></span> |