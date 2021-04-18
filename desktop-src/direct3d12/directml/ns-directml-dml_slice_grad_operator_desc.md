---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Berechnet backpropagierungs Gradienten für Slice (siehe [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
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
ms.openlocfilehash: 63ea67454965d976247c3cdd50aa183f6a676138
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106365212"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="cb170-103">DML_SLICE_GRAD_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="cb170-103">DML_SLICE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="cb170-104">Berechnet backpropagierungs Gradienten für Slice (siehe [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="cb170-104">Computes backpropagation gradients for Slice (see [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span></span>

<span data-ttu-id="cb170-105">Denken Sie daran, dass [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) einen Unterbereich eines Eingabe Mandanten extrahiert.</span><span class="sxs-lookup"><span data-stu-id="cb170-105">Recall that [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extracts a subregion of an input tensor.</span></span> <span data-ttu-id="cb170-106">Wenn ein *inputgradienttensor* mit denselben Größen wie die *Ausgabe* eines äquivalenten **DML_SLICE1_OPERATOR_DESC** angegeben wird, erzeugt dieser Operator einen *outputgradienttensor* mit denselben Größen wie die *Eingabe* von **DML_SLICE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="cb170-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_SLICE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of **DML_SLICE1_OPERATOR_DESC**.</span></span> <span data-ttu-id="cb170-107">Die in Slices aufgeschnittenen Elemente werden an die Ausgabe weitergegeben, und alle anderen Elemente werden auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb170-107">The sliced elements are propagated to the output, and all other elements are set to 0.</span></span>

<span data-ttu-id="cb170-108">Sehen Sie sich als Beispiel eine **DML_SLICE1_OPERATOR_DESC** an, die die folgenden Elemente aus einem Mandanten extrahiert:</span><span class="sxs-lookup"><span data-stu-id="cb170-108">As an example, consider a **DML_SLICE1_OPERATOR_DESC** that extracts the following elements from a tensor:</span></span>

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

<span data-ttu-id="cb170-109">Wenn sich die gleichen *inputwindowoffsets*- / *Größen* /  wie im obigen Beispiel befinden, führt dieser Operator die folgende Transformation aus.</span><span class="sxs-lookup"><span data-stu-id="cb170-109">If provided the same *InputWindowOffsets*/*Sizes*/*Strides* as in the above example, this operator would then perform the following transform.</span></span>

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> <span data-ttu-id="cb170-110">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="cb170-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="cb170-111">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="cb170-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb170-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb170-112">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="cb170-113">Member</span><span class="sxs-lookup"><span data-stu-id="cb170-113">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="cb170-114">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cb170-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cb170-115">Der eingehende gradiententensor.</span><span class="sxs-lookup"><span data-stu-id="cb170-115">The incoming gradient tensor.</span></span> <span data-ttu-id="cb170-116">Dies wird in der Regel aus der Ausgabe der Rück Propagierung einer vorangehenden Ebene abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cb170-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="cb170-117">In der Regel hat dieser tensorflow die gleichen Größen wie die *Ausgabe* der entsprechenden [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) im Forward-Pass.</span><span class="sxs-lookup"><span data-stu-id="cb170-117">Typically, this tensor would have the same sizes as the *output* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="cb170-118">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cb170-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cb170-119">Ein Ausgabe Mandanten, der die zurückgegebenen Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="cb170-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="cb170-120">In der Regel hat dieser Mandanten die gleichen Größen wie die *Eingabe* des entsprechenden [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) im Forward-Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="cb170-120">Typically, this tensor would have the same sizes as the *input* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="cb170-121">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cb170-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="cb170-122">Die Anzahl der Elemente in den Arrays *inputwindowoffsets*, *inputwindowsizes* und *inputwindowclaims* .</span><span class="sxs-lookup"><span data-stu-id="cb170-122">The number of elements in the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="cb170-123">Dieser Wert muss mit der *DimensionCount* übereinstimmen, die in *inputgradienttensor* und *outputgradienttensor* bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cb170-123">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`InputWindowOffsets`

<span data-ttu-id="cb170-124">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="cb170-124">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="cb170-125">Weitere Informationen finden Sie unter *inputwindowoffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="cb170-125">See *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowSizes`

<span data-ttu-id="cb170-126">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="cb170-126">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="cb170-127">Weitere Informationen finden Sie unter *inputwindowsizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="cb170-127">See *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowStrides`

<span data-ttu-id="cb170-128">Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="cb170-128">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="cb170-129">Weitere Informationen finden Sie unter *inputwindowclaims* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="cb170-129">See *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

<span data-ttu-id="cb170-130">Beachten Sie, dass dieser Operator im Gegensatz zu **DML_SLICE1_OPERATOR_DESC** Schritte ungleich 0 (null) erfordert.</span><span class="sxs-lookup"><span data-stu-id="cb170-130">Note that unlike **DML_SLICE1_OPERATOR_DESC**, this operator requires non-zero strides.</span></span> <span data-ttu-id="cb170-131">Das liegt daran, dass bei einem NULL-Stride nicht eindeutig ist, welche Eingabeelemente den einzelnen Ausgabe Elementen zugeordnet werden sollen. Daher kann die Rück Verbreitung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cb170-131">That's because with a zero stride, it's ambiguous as to which input element should map to each output element, and therefore backpropagation can't be performed.</span></span> <span data-ttu-id="cb170-132">Wie **DML_SLICE1_OPERATOR_DESC** kippen negative Fortschritte die Eingabefenster Richtung entlang dieser Achse.</span><span class="sxs-lookup"><span data-stu-id="cb170-132">Like **DML_SLICE1_OPERATOR_DESC**, negative strides flip the input window direction along that axis.</span></span>

## <a name="availability"></a><span data-ttu-id="cb170-133">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="cb170-133">Availability</span></span>
<span data-ttu-id="cb170-134">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="cb170-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cb170-135">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="cb170-135">Tensor constraints</span></span>
<span data-ttu-id="cb170-136">*Inputgradienttensor* und *outputgradienttensor* müssen denselben *Datentyp* und *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cb170-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cb170-137">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="cb170-137">Tensor support</span></span>
| <span data-ttu-id="cb170-138">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="cb170-138">Tensor</span></span> | <span data-ttu-id="cb170-139">Typ</span><span class="sxs-lookup"><span data-stu-id="cb170-139">Kind</span></span> | <span data-ttu-id="cb170-140">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="cb170-140">Supported dimension counts</span></span> | <span data-ttu-id="cb170-141">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="cb170-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cb170-142">Input gradienttensor</span><span class="sxs-lookup"><span data-stu-id="cb170-142">InputGradientTensor</span></span> | <span data-ttu-id="cb170-143">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cb170-143">Input</span></span> | <span data-ttu-id="cb170-144">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="cb170-144">1 to 8</span></span> | <span data-ttu-id="cb170-145">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="cb170-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="cb170-146">Outputgradienttensor</span><span class="sxs-lookup"><span data-stu-id="cb170-146">OutputGradientTensor</span></span> | <span data-ttu-id="cb170-147">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="cb170-147">Output</span></span> | <span data-ttu-id="cb170-148">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="cb170-148">1 to 8</span></span> | <span data-ttu-id="cb170-149">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="cb170-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="cb170-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb170-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cb170-151">**Header**</span><span class="sxs-lookup"><span data-stu-id="cb170-151">**Header**</span></span> | <span data-ttu-id="cb170-152">directml. h</span><span class="sxs-lookup"><span data-stu-id="cb170-152">directml.h</span></span> |