---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Berechnet Rückeigenschaftenverläufe für eine regradifizierte lineare Einheit (ReLU).
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
ms.openlocfilehash: dea89f0e3366a07ee98f47703f07e2f5a9d4009d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417187"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="343e3-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="343e3-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="343e3-104">Berechnet Rückeigenschaftenverläufe für eine regradifizierte lineare Einheit (ReLU).</span><span class="sxs-lookup"><span data-stu-id="343e3-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="343e3-105">Dieser Operator führt die folgende elementweise Berechnung aus.</span><span class="sxs-lookup"><span data-stu-id="343e3-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="343e3-106">Der entsprechende Forward-Pass-Operator ist [DML_ACTIVATION_RELU_OPERATOR_DESC.](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="343e3-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="343e3-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="343e3-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="343e3-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="343e3-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="343e3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="343e3-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="343e3-110">Member</span><span class="sxs-lookup"><span data-stu-id="343e3-110">Members</span></span>

`InputTensor`

<span data-ttu-id="343e3-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="343e3-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="343e3-112">Der Eingabe-Tensor (Feature).</span><span class="sxs-lookup"><span data-stu-id="343e3-112">The input (feature) tensor.</span></span> <span data-ttu-id="343e3-113">Dies ist in der Regel die gleiche Eingabe, die während des Vorwärtspasses bereitgestellt wurde (siehe [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="343e3-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="343e3-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="343e3-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="343e3-115">Der eingehende Farbverlaufs-Tensor.</span><span class="sxs-lookup"><span data-stu-id="343e3-115">The incoming gradient tensor.</span></span> <span data-ttu-id="343e3-116">Dies wird in der Regel aus der Ausgabe der Backpropagation einer vorherigen Ebene ermittelt.</span><span class="sxs-lookup"><span data-stu-id="343e3-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="343e3-117">Die *Größen und* der Datentyp *dieses* Tensors müssen genau mit denen des *InputTensor übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="343e3-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="343e3-118">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="343e3-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="343e3-119">Ein Ausgabe tensor, der die zurückpropagierten Farbverläufe enthält.</span><span class="sxs-lookup"><span data-stu-id="343e3-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="343e3-120">Die *Größen und* der Datentyp *dieses* Tensors müssen genau mit denen des *InputTensor übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="343e3-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="343e3-121">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="343e3-121">Availability</span></span>
<span data-ttu-id="343e3-122">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="343e3-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="343e3-123">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="343e3-123">Tensor constraints</span></span>
<span data-ttu-id="343e3-124">*InputGradientTensor,* *InputTensor* und *OutputGradientTensor* müssen denselben *DataType,* *DimensionCount* und *die gleichen Größen aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="343e3-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="343e3-125">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="343e3-125">Tensor support</span></span>
| <span data-ttu-id="343e3-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="343e3-126">Tensor</span></span> | <span data-ttu-id="343e3-127">Typ</span><span class="sxs-lookup"><span data-stu-id="343e3-127">Kind</span></span> | <span data-ttu-id="343e3-128">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="343e3-128">Supported dimension counts</span></span> | <span data-ttu-id="343e3-129">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="343e3-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="343e3-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="343e3-130">InputTensor</span></span> | <span data-ttu-id="343e3-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="343e3-131">Input</span></span> | <span data-ttu-id="343e3-132">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="343e3-132">1 to 8</span></span> | <span data-ttu-id="343e3-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="343e3-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="343e3-134">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="343e3-134">InputGradientTensor</span></span> | <span data-ttu-id="343e3-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="343e3-135">Input</span></span> | <span data-ttu-id="343e3-136">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="343e3-136">1 to 8</span></span> | <span data-ttu-id="343e3-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="343e3-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="343e3-138">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="343e3-138">OutputGradientTensor</span></span> | <span data-ttu-id="343e3-139">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="343e3-139">Output</span></span> | <span data-ttu-id="343e3-140">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="343e3-140">1 to 8</span></span> | <span data-ttu-id="343e3-141">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="343e3-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="343e3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="343e3-142">See also</span></span>
[<span data-ttu-id="343e3-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="343e3-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="343e3-144">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="343e3-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="343e3-145">**Header**</span><span class="sxs-lookup"><span data-stu-id="343e3-145">**Header**</span></span> | <span data-ttu-id="343e3-146">directml.h</span><span class="sxs-lookup"><span data-stu-id="343e3-146">directml.h</span></span> |