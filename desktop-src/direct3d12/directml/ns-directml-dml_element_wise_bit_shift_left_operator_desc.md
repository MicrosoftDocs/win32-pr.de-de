---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
description: Führt eine logische Linksverschiebung jedes Elements von *ATensor* um eine Anzahl von Bits aus, die vom entsprechenden Element von *BTensor* angegeben werden, und platziert das Ergebnis im entsprechenden Element von *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_left_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
ms.openlocfilehash: 993e8f2969752c8e2133f685685d69942c77b506
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417626"
---
# <a name="dml_element_wise_bit_shift_left_operator_desc-structure-directmlh"></a><span data-ttu-id="9d777-103">DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="9d777-103">DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="9d777-104">Führt eine logische Linksverschiebung jedes Elements von *ATensor* um eine Anzahl von Bits aus, die vom entsprechenden Element von *BTensor* angegeben werden, und platziert das Ergebnis im entsprechenden Element von *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="9d777-104">Performs a logical left shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a << b)
```

<span data-ttu-id="9d777-105">Dieser Operator unterstützt die ausführungsbasierte Ausführung, was bedeutet, dass *OutputTensor* während der Bindung einen Alias für einen der Eingabetensoren verwenden darf.</span><span class="sxs-lookup"><span data-stu-id="9d777-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d777-106">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="9d777-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="9d777-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="9d777-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d777-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d777-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="9d777-109">Member</span><span class="sxs-lookup"><span data-stu-id="9d777-109">Members</span></span>

`ATensor`

<span data-ttu-id="9d777-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9d777-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9d777-111">Ein Tensor, der die eingaben auf der linken Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="9d777-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="9d777-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9d777-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9d777-113">Ein Tensor, der die eingaben auf der rechten Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="9d777-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="9d777-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9d777-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9d777-115">Der Ausgabe tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9d777-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="9d777-116">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="9d777-116">Availability</span></span>
<span data-ttu-id="9d777-117">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9d777-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="9d777-118">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="9d777-118">Tensor constraints</span></span>
<span data-ttu-id="9d777-119">*ATensor,* *BTensor* und *OutputTensor* müssen denselben *DataType,* *DimensionCount* und *die gleichen Größen aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="9d777-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="9d777-120">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="9d777-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="9d777-121">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="9d777-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="9d777-122">Tensor</span><span class="sxs-lookup"><span data-stu-id="9d777-122">Tensor</span></span> | <span data-ttu-id="9d777-123">Typ</span><span class="sxs-lookup"><span data-stu-id="9d777-123">Kind</span></span> | <span data-ttu-id="9d777-124">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="9d777-124">Supported dimension counts</span></span> | <span data-ttu-id="9d777-125">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="9d777-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="9d777-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="9d777-126">ATensor</span></span> | <span data-ttu-id="9d777-127">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9d777-127">Input</span></span> | <span data-ttu-id="9d777-128">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="9d777-128">1 to 8</span></span> | <span data-ttu-id="9d777-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="9d777-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="9d777-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="9d777-130">BTensor</span></span> | <span data-ttu-id="9d777-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9d777-131">Input</span></span> | <span data-ttu-id="9d777-132">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="9d777-132">1 to 8</span></span> | <span data-ttu-id="9d777-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="9d777-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="9d777-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="9d777-134">OutputTensor</span></span> | <span data-ttu-id="9d777-135">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="9d777-135">Output</span></span> | <span data-ttu-id="9d777-136">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="9d777-136">1 to 8</span></span> | <span data-ttu-id="9d777-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="9d777-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="9d777-138">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="9d777-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="9d777-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="9d777-139">Tensor</span></span> | <span data-ttu-id="9d777-140">Typ</span><span class="sxs-lookup"><span data-stu-id="9d777-140">Kind</span></span> | <span data-ttu-id="9d777-141">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="9d777-141">Supported dimension counts</span></span> | <span data-ttu-id="9d777-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="9d777-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="9d777-143">ATensor</span><span class="sxs-lookup"><span data-stu-id="9d777-143">ATensor</span></span> | <span data-ttu-id="9d777-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9d777-144">Input</span></span> | <span data-ttu-id="9d777-145">4</span><span class="sxs-lookup"><span data-stu-id="9d777-145">4</span></span> | <span data-ttu-id="9d777-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="9d777-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="9d777-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="9d777-147">BTensor</span></span> | <span data-ttu-id="9d777-148">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9d777-148">Input</span></span> | <span data-ttu-id="9d777-149">4</span><span class="sxs-lookup"><span data-stu-id="9d777-149">4</span></span> | <span data-ttu-id="9d777-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="9d777-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="9d777-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="9d777-151">OutputTensor</span></span> | <span data-ttu-id="9d777-152">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="9d777-152">Output</span></span> | <span data-ttu-id="9d777-153">4</span><span class="sxs-lookup"><span data-stu-id="9d777-153">4</span></span> | <span data-ttu-id="9d777-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="9d777-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="9d777-155">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9d777-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9d777-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="9d777-156">**Header**</span></span> | <span data-ttu-id="9d777-157">directml.h</span><span class="sxs-lookup"><span data-stu-id="9d777-157">directml.h</span></span> |