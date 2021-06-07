---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
description: Berechnet den Modulus mit den gleichen Ergebnissen wie der Python-Modulus für jedes Paar der entsprechenden Elemente aus den Eingabe-Tensoren und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_floor_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.openlocfilehash: 8c70bd4649a57270807ac408802fe07edd36d98e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417874"
---
# <a name="dml_element_wise_modulus_floor_operator_desc-structure-directmlh"></a><span data-ttu-id="a08e8-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="a08e8-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a08e8-104">Berechnet den Modulus mit den gleichen Ergebnissen wie der Python-Modulus für jedes Paar der entsprechenden Elemente aus den Eingabe-Tensoren und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="a08e8-104">Computes the modulus, with the same results as the Python modulus, for each pair of corresponding elements from the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="a08e8-105">Da der Quotient auf -inf gerundet wird, hat das Ergebnis das gleiche Vorzeichen wie der Divisor.</span><span class="sxs-lookup"><span data-stu-id="a08e8-105">Because the quotient is rounded towards -inf, the result will have the same sign as the divisor.</span></span>

```
f(a, b) = a - (b * floor(a / b))
```

<span data-ttu-id="a08e8-106">Dieser Operator unterstützt die direkt ausgeführte Ausführung, d. h., *OutputTensor* darf während der Bindung einen der Eingabe-Tensoren mit einem Alias verbinden.</span><span class="sxs-lookup"><span data-stu-id="a08e8-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a08e8-107">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="a08e8-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a08e8-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="a08e8-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a08e8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a08e8-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="a08e8-110">Member</span><span class="sxs-lookup"><span data-stu-id="a08e8-110">Members</span></span>

`ATensor`

<span data-ttu-id="a08e8-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a08e8-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a08e8-112">Ein Tensor, der die linken Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="a08e8-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="a08e8-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a08e8-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a08e8-114">Ein Tensor, der die rechten Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="a08e8-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="a08e8-115">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a08e8-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a08e8-116">Der Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a08e8-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="a08e8-117">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="a08e8-117">Availability</span></span>
<span data-ttu-id="a08e8-118">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a08e8-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a08e8-119">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="a08e8-119">Tensor constraints</span></span>
<span data-ttu-id="a08e8-120">*ATensor,* *BTensor* und *OutputTensor* müssen die gleichen *Datentypen*, *DimensionCount* und *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a08e8-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a08e8-121">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a08e8-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="a08e8-122">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="a08e8-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="a08e8-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="a08e8-123">Tensor</span></span> | <span data-ttu-id="a08e8-124">Typ</span><span class="sxs-lookup"><span data-stu-id="a08e8-124">Kind</span></span> | <span data-ttu-id="a08e8-125">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="a08e8-125">Supported dimension counts</span></span> | <span data-ttu-id="a08e8-126">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="a08e8-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a08e8-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="a08e8-127">ATensor</span></span> | <span data-ttu-id="a08e8-128">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a08e8-128">Input</span></span> | <span data-ttu-id="a08e8-129">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a08e8-129">1 to 8</span></span> | <span data-ttu-id="a08e8-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a08e8-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a08e8-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="a08e8-131">BTensor</span></span> | <span data-ttu-id="a08e8-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a08e8-132">Input</span></span> | <span data-ttu-id="a08e8-133">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a08e8-133">1 to 8</span></span> | <span data-ttu-id="a08e8-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a08e8-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a08e8-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a08e8-135">OutputTensor</span></span> | <span data-ttu-id="a08e8-136">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a08e8-136">Output</span></span> | <span data-ttu-id="a08e8-137">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a08e8-137">1 to 8</span></span> | <span data-ttu-id="a08e8-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a08e8-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="a08e8-139">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="a08e8-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="a08e8-140">Tensor</span><span class="sxs-lookup"><span data-stu-id="a08e8-140">Tensor</span></span> | <span data-ttu-id="a08e8-141">Typ</span><span class="sxs-lookup"><span data-stu-id="a08e8-141">Kind</span></span> | <span data-ttu-id="a08e8-142">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="a08e8-142">Supported dimension counts</span></span> | <span data-ttu-id="a08e8-143">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="a08e8-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a08e8-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="a08e8-144">ATensor</span></span> | <span data-ttu-id="a08e8-145">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a08e8-145">Input</span></span> | <span data-ttu-id="a08e8-146">4</span><span class="sxs-lookup"><span data-stu-id="a08e8-146">4</span></span> | <span data-ttu-id="a08e8-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a08e8-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a08e8-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="a08e8-148">BTensor</span></span> | <span data-ttu-id="a08e8-149">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a08e8-149">Input</span></span> | <span data-ttu-id="a08e8-150">4</span><span class="sxs-lookup"><span data-stu-id="a08e8-150">4</span></span> | <span data-ttu-id="a08e8-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a08e8-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a08e8-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a08e8-152">OutputTensor</span></span> | <span data-ttu-id="a08e8-153">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a08e8-153">Output</span></span> | <span data-ttu-id="a08e8-154">4</span><span class="sxs-lookup"><span data-stu-id="a08e8-154">4</span></span> | <span data-ttu-id="a08e8-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a08e8-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="a08e8-156">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a08e8-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a08e8-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="a08e8-157">**Header**</span></span> | <span data-ttu-id="a08e8-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="a08e8-158">directml.h</span></span> |