---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Berechnet backpropagierungs Gradienten für eine korrigierte lineare Einheit (relu).
helpviewer_keywords:
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC, DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.openlocfilehash: 567a1de50c1c91de83a9fda2978f83af8daf1a6e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361106"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="a9891-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="a9891-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a9891-104">Berechnet backpropagierungs Gradienten für eine korrigierte lineare Einheit (relu).</span><span class="sxs-lookup"><span data-stu-id="a9891-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="a9891-105">Dieser Operator führt die folgende Element Weise Berechnung aus.</span><span class="sxs-lookup"><span data-stu-id="a9891-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="a9891-106">Der entsprechende Forward-Pass-Operator ist [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="a9891-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9891-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="a9891-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="a9891-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="a9891-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9891-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9891-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="a9891-110">Member</span><span class="sxs-lookup"><span data-stu-id="a9891-110">Members</span></span>

`InputTensor`

<span data-ttu-id="a9891-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9891-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9891-112">Der Eingabe-Tensor (Feature).</span><span class="sxs-lookup"><span data-stu-id="a9891-112">The input (feature) tensor.</span></span> <span data-ttu-id="a9891-113">Dabei handelt es sich in der Regel um die gleiche Eingabe wie bei der Weiterleitung (siehe [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="a9891-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="a9891-114">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9891-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9891-115">Der eingehende gradiententensor.</span><span class="sxs-lookup"><span data-stu-id="a9891-115">The incoming gradient tensor.</span></span> <span data-ttu-id="a9891-116">Dies wird in der Regel aus der Ausgabe der Rück Propagierung einer vorangehenden Ebene abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a9891-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="a9891-117">Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *inputtensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a9891-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="a9891-118">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9891-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9891-119">Ein Ausgabe Mandanten, der die zurückgegebenen Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="a9891-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="a9891-120">Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *inputtensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a9891-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="a9891-121">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="a9891-121">Availability</span></span>
<span data-ttu-id="a9891-122">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="a9891-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a9891-123">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="a9891-123">Tensor constraints</span></span>
<span data-ttu-id="a9891-124">*Inputgradienttensor*, *inputtensor* und *outputgradienttensor* müssen denselben *Datentyp*, jede *DimensionCount* und jede *Größe* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a9891-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a9891-125">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a9891-125">Tensor support</span></span>
| <span data-ttu-id="a9891-126">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="a9891-126">Tensor</span></span> | <span data-ttu-id="a9891-127">Typ</span><span class="sxs-lookup"><span data-stu-id="a9891-127">Kind</span></span> | <span data-ttu-id="a9891-128">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="a9891-128">Supported dimension counts</span></span> | <span data-ttu-id="a9891-129">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="a9891-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a9891-130">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="a9891-130">InputTensor</span></span> | <span data-ttu-id="a9891-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9891-131">Input</span></span> | <span data-ttu-id="a9891-132">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a9891-132">1 to 8</span></span> | <span data-ttu-id="a9891-133">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a9891-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a9891-134">Input gradienttensor</span><span class="sxs-lookup"><span data-stu-id="a9891-134">InputGradientTensor</span></span> | <span data-ttu-id="a9891-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9891-135">Input</span></span> | <span data-ttu-id="a9891-136">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a9891-136">1 to 8</span></span> | <span data-ttu-id="a9891-137">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a9891-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a9891-138">Outputgradienttensor</span><span class="sxs-lookup"><span data-stu-id="a9891-138">OutputGradientTensor</span></span> | <span data-ttu-id="a9891-139">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a9891-139">Output</span></span> | <span data-ttu-id="a9891-140">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a9891-140">1 to 8</span></span> | <span data-ttu-id="a9891-141">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a9891-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="a9891-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9891-142">See also</span></span>
[<span data-ttu-id="a9891-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="a9891-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="a9891-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9891-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a9891-145">**Header**</span><span class="sxs-lookup"><span data-stu-id="a9891-145">**Header**</span></span> | <span data-ttu-id="a9891-146">directml. h</span><span class="sxs-lookup"><span data-stu-id="a9891-146">directml.h</span></span> |