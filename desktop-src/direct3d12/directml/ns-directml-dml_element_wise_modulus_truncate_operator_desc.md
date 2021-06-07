---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
description: Berechnet den C-Modulusoperator für jedes Paar der entsprechenden Elemente der Eingabe tensors und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_truncate_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
ms.openlocfilehash: 461a7882e17d86b25cf27e0a28c05673f8899cea
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417616"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="07d0d-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="07d0d-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="07d0d-104">Berechnet den C-Modulusoperator für jedes Paar der entsprechenden Elemente der Eingabe tensors und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="07d0d-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="07d0d-105">Da der Quotient auf 0 gerundet wird, hat das Ergebnis das gleiche Vorzeichen wie der Dividend.</span><span class="sxs-lookup"><span data-stu-id="07d0d-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="07d0d-106">Dieser Operator unterstützt die direkt ausgeführte Ausführung, d. h., *OutputTensor* darf während der Bindung einen der Eingabe-Tensoren mit einem Alias verbinden.</span><span class="sxs-lookup"><span data-stu-id="07d0d-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07d0d-107">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="07d0d-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="07d0d-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="07d0d-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="07d0d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="07d0d-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="07d0d-110">Member</span><span class="sxs-lookup"><span data-stu-id="07d0d-110">Members</span></span>

`ATensor`

<span data-ttu-id="07d0d-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="07d0d-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="07d0d-112">Ein Tensor, der die linken Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="07d0d-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="07d0d-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="07d0d-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="07d0d-114">Ein Tensor, der die rechten Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="07d0d-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="07d0d-115">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="07d0d-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="07d0d-116">Der Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="07d0d-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="07d0d-117">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="07d0d-117">Availability</span></span>
<span data-ttu-id="07d0d-118">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="07d0d-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="07d0d-119">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="07d0d-119">Tensor constraints</span></span>
<span data-ttu-id="07d0d-120">*ATensor,* *BTensor* und *OutputTensor* müssen die gleichen *Datentypen*, *DimensionCount* und *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="07d0d-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="07d0d-121">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="07d0d-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="07d0d-122">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="07d0d-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="07d0d-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="07d0d-123">Tensor</span></span> | <span data-ttu-id="07d0d-124">Typ</span><span class="sxs-lookup"><span data-stu-id="07d0d-124">Kind</span></span> | <span data-ttu-id="07d0d-125">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="07d0d-125">Supported dimension counts</span></span> | <span data-ttu-id="07d0d-126">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="07d0d-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="07d0d-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="07d0d-127">ATensor</span></span> | <span data-ttu-id="07d0d-128">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07d0d-128">Input</span></span> | <span data-ttu-id="07d0d-129">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="07d0d-129">1 to 8</span></span> | <span data-ttu-id="07d0d-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="07d0d-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="07d0d-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="07d0d-131">BTensor</span></span> | <span data-ttu-id="07d0d-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07d0d-132">Input</span></span> | <span data-ttu-id="07d0d-133">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="07d0d-133">1 to 8</span></span> | <span data-ttu-id="07d0d-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="07d0d-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="07d0d-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="07d0d-135">OutputTensor</span></span> | <span data-ttu-id="07d0d-136">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="07d0d-136">Output</span></span> | <span data-ttu-id="07d0d-137">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="07d0d-137">1 to 8</span></span> | <span data-ttu-id="07d0d-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="07d0d-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="07d0d-139">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="07d0d-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="07d0d-140">Tensor</span><span class="sxs-lookup"><span data-stu-id="07d0d-140">Tensor</span></span> | <span data-ttu-id="07d0d-141">Typ</span><span class="sxs-lookup"><span data-stu-id="07d0d-141">Kind</span></span> | <span data-ttu-id="07d0d-142">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="07d0d-142">Supported dimension counts</span></span> | <span data-ttu-id="07d0d-143">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="07d0d-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="07d0d-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="07d0d-144">ATensor</span></span> | <span data-ttu-id="07d0d-145">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07d0d-145">Input</span></span> | <span data-ttu-id="07d0d-146">4</span><span class="sxs-lookup"><span data-stu-id="07d0d-146">4</span></span> | <span data-ttu-id="07d0d-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="07d0d-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="07d0d-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="07d0d-148">BTensor</span></span> | <span data-ttu-id="07d0d-149">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07d0d-149">Input</span></span> | <span data-ttu-id="07d0d-150">4</span><span class="sxs-lookup"><span data-stu-id="07d0d-150">4</span></span> | <span data-ttu-id="07d0d-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="07d0d-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="07d0d-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="07d0d-152">OutputTensor</span></span> | <span data-ttu-id="07d0d-153">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="07d0d-153">Output</span></span> | <span data-ttu-id="07d0d-154">4</span><span class="sxs-lookup"><span data-stu-id="07d0d-154">4</span></span> | <span data-ttu-id="07d0d-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="07d0d-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="07d0d-156">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="07d0d-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="07d0d-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="07d0d-157">**Header**</span></span> | <span data-ttu-id="07d0d-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="07d0d-158">directml.h</span></span> |