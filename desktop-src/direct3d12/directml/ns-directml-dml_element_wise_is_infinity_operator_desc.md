---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Überprüft jedes Element von *InputTensor* je nach dem angegebenen *InfinityMode* auf IEEE-754 -inf, inf oder beides und platziert das Ergebnis (1 für true, 0 für false) in das entsprechende Element von *OutputTensor.*
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417722"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="871f5-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="871f5-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="871f5-104">Überprüft jedes Element von *InputTensor* je nach dem angegebenen *InfinityMode* auf IEEE-754 -inf, inf oder beides und platziert das Ergebnis (1 für true, 0 für false) in das entsprechende Element von *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="871f5-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="871f5-105">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="871f5-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="871f5-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="871f5-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="871f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="871f5-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="871f5-108">Member</span><span class="sxs-lookup"><span data-stu-id="871f5-108">Members</span></span>

`InputTensor`

<span data-ttu-id="871f5-109">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="871f5-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="871f5-110">Der Eingabetensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="871f5-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="871f5-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="871f5-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="871f5-112">Der Ausgabe tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="871f5-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="871f5-113">Typ: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="871f5-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="871f5-114">Ein [DML_IS_INFINITY_MODE,](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) der das Vorzeichen der Unendlichkeit bestimmt, auf die überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="871f5-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="871f5-115">Wenn **DML_IS_INFINITY_MODE_EITHER,** wird 1 zurückgegeben, wenn das Element -inf oder inf ist, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="871f5-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="871f5-116">Wenn **DML_IS_INFINITY_MODE_POSITIVE,** wird 1 zurückgegeben, wenn das Element inf ist, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="871f5-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="871f5-117">Wenn **DML_IS_INFINITY_MODE_NEGATIVE** ist, wird 1 zurückgegeben, wenn das Element -inf ist, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="871f5-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="871f5-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="871f5-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="871f5-119">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="871f5-119">Availability</span></span>
<span data-ttu-id="871f5-120">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="871f5-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="871f5-121">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="871f5-121">Tensor constraints</span></span>
<span data-ttu-id="871f5-122">*InputTensor und* *OutputTensor* müssen über die gleichen *DimensionCount-* und *Sizes-Größen verfügen.*</span><span class="sxs-lookup"><span data-stu-id="871f5-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="871f5-123">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="871f5-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="871f5-124">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="871f5-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="871f5-125">Tensor</span><span class="sxs-lookup"><span data-stu-id="871f5-125">Tensor</span></span> | <span data-ttu-id="871f5-126">Typ</span><span class="sxs-lookup"><span data-stu-id="871f5-126">Kind</span></span> | <span data-ttu-id="871f5-127">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="871f5-127">Supported dimension counts</span></span> | <span data-ttu-id="871f5-128">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="871f5-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="871f5-129">InputTensor</span><span class="sxs-lookup"><span data-stu-id="871f5-129">InputTensor</span></span> | <span data-ttu-id="871f5-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="871f5-130">Input</span></span> | <span data-ttu-id="871f5-131">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="871f5-131">1 to 8</span></span> | <span data-ttu-id="871f5-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="871f5-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="871f5-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="871f5-133">OutputTensor</span></span> | <span data-ttu-id="871f5-134">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="871f5-134">Output</span></span> | <span data-ttu-id="871f5-135">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="871f5-135">1 to 8</span></span> | <span data-ttu-id="871f5-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="871f5-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="871f5-137">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="871f5-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="871f5-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="871f5-138">Tensor</span></span> | <span data-ttu-id="871f5-139">Typ</span><span class="sxs-lookup"><span data-stu-id="871f5-139">Kind</span></span> | <span data-ttu-id="871f5-140">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="871f5-140">Supported dimension counts</span></span> | <span data-ttu-id="871f5-141">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="871f5-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="871f5-142">InputTensor</span><span class="sxs-lookup"><span data-stu-id="871f5-142">InputTensor</span></span> | <span data-ttu-id="871f5-143">Eingabe</span><span class="sxs-lookup"><span data-stu-id="871f5-143">Input</span></span> | <span data-ttu-id="871f5-144">4</span><span class="sxs-lookup"><span data-stu-id="871f5-144">4</span></span> | <span data-ttu-id="871f5-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="871f5-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="871f5-146">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="871f5-146">OutputTensor</span></span> | <span data-ttu-id="871f5-147">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="871f5-147">Output</span></span> | <span data-ttu-id="871f5-148">4</span><span class="sxs-lookup"><span data-stu-id="871f5-148">4</span></span> | <span data-ttu-id="871f5-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="871f5-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="871f5-150">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="871f5-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="871f5-151">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="871f5-151">**Minimum supported client**</span></span> | <span data-ttu-id="871f5-152">Windows 10, Version 2004 (10.0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="871f5-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="871f5-153">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="871f5-153">**Minimum supported server**</span></span> | <span data-ttu-id="871f5-154">Windows Server, Version 2004 (10.0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="871f5-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="871f5-155">**Header**</span><span class="sxs-lookup"><span data-stu-id="871f5-155">**Header**</span></span> | <span data-ttu-id="871f5-156">directml.h</span><span class="sxs-lookup"><span data-stu-id="871f5-156">directml.h</span></span> |