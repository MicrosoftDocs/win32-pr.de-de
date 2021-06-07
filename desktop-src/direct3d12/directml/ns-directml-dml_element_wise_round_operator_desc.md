---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Rundet jedes Element von *InputTensor* auf einen ganzzahligen Wert und platziert das Ergebnis im entsprechenden Element von *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure
- direct3d12.dml_element_wise_round_operator_desc
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.openlocfilehash: cb9414d0c3e628fa95784480c7402b242d12095b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417855"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="f46a8-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="f46a8-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f46a8-104">Rundet jedes Element von *InputTensor* auf einen ganzzahligen Wert und platziert das Ergebnis im entsprechenden Element von *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="f46a8-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="f46a8-105">Dieser Operator unterstützt die ausführungsbasierte Ausführung, was bedeutet, dass *OutputTensor* während der Bindung einen *Alias für InputTensor* verwenden darf.</span><span class="sxs-lookup"><span data-stu-id="f46a8-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f46a8-106">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="f46a8-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f46a8-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="f46a8-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f46a8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f46a8-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="f46a8-109">Member</span><span class="sxs-lookup"><span data-stu-id="f46a8-109">Members</span></span>

`InputTensor`

<span data-ttu-id="f46a8-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f46a8-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f46a8-111">Der Eingabetensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f46a8-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="f46a8-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f46a8-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f46a8-113">Der Ausgabe tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f46a8-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="f46a8-114">Typ: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="f46a8-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="f46a8-115">Ein [DML_ROUNDING_MODE,](/windows/win32/api/directml/ne-directml-dml_rounding_mode) der die Richtung bestimmt, auf die gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f46a8-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="f46a8-116">Wenn **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN:** Werte werden auf die nächste ganze Zahl gerundet, und die Hälftenwerte (z. B. 0,5) werden auf die nächste gerade ganze Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="f46a8-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="f46a8-117">Wenn **DML_ROUNDING_MODE_TOWARD_ZERO:** Werte werden auf Null gerundet.</span><span class="sxs-lookup"><span data-stu-id="f46a8-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="f46a8-118">Dadurch wird der Bruchteil effektiv abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="f46a8-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="f46a8-119">Wenn **DML_ROUNDING_MODE_TOWARD_INFINITY:** Werte werden auf die nächste ganze Zahl gerundet, und die Hälftenwerte (z. B. 0,5) werden von 0 (in Richtung positiv oder negativ unendlich, je nach Vorzeichen des Werts) gerundet.</span><span class="sxs-lookup"><span data-stu-id="f46a8-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="f46a8-120">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="f46a8-120">Availability</span></span>
<span data-ttu-id="f46a8-121">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f46a8-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f46a8-122">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="f46a8-122">Tensor constraints</span></span>
<span data-ttu-id="f46a8-123">*InputTensor und* *OutputTensor* müssen denselben *DataType,* *DimensionCount* und *die gleichen Größen aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="f46a8-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f46a8-124">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="f46a8-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="f46a8-125">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="f46a8-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="f46a8-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="f46a8-126">Tensor</span></span> | <span data-ttu-id="f46a8-127">Typ</span><span class="sxs-lookup"><span data-stu-id="f46a8-127">Kind</span></span> | <span data-ttu-id="f46a8-128">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="f46a8-128">Supported dimension counts</span></span> | <span data-ttu-id="f46a8-129">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="f46a8-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f46a8-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f46a8-130">InputTensor</span></span> | <span data-ttu-id="f46a8-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f46a8-131">Input</span></span> | <span data-ttu-id="f46a8-132">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f46a8-132">1 to 8</span></span> | <span data-ttu-id="f46a8-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f46a8-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f46a8-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f46a8-134">OutputTensor</span></span> | <span data-ttu-id="f46a8-135">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f46a8-135">Output</span></span> | <span data-ttu-id="f46a8-136">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="f46a8-136">1 to 8</span></span> | <span data-ttu-id="f46a8-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f46a8-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="f46a8-138">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="f46a8-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="f46a8-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="f46a8-139">Tensor</span></span> | <span data-ttu-id="f46a8-140">Typ</span><span class="sxs-lookup"><span data-stu-id="f46a8-140">Kind</span></span> | <span data-ttu-id="f46a8-141">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="f46a8-141">Supported dimension counts</span></span> | <span data-ttu-id="f46a8-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="f46a8-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f46a8-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f46a8-143">InputTensor</span></span> | <span data-ttu-id="f46a8-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f46a8-144">Input</span></span> | <span data-ttu-id="f46a8-145">4</span><span class="sxs-lookup"><span data-stu-id="f46a8-145">4</span></span> | <span data-ttu-id="f46a8-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f46a8-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f46a8-147">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f46a8-147">OutputTensor</span></span> | <span data-ttu-id="f46a8-148">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f46a8-148">Output</span></span> | <span data-ttu-id="f46a8-149">4</span><span class="sxs-lookup"><span data-stu-id="f46a8-149">4</span></span> | <span data-ttu-id="f46a8-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f46a8-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="f46a8-151">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f46a8-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f46a8-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="f46a8-152">**Header**</span></span> | <span data-ttu-id="f46a8-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="f46a8-153">directml.h</span></span> |