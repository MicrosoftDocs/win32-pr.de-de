---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Rundet jedes Element von *InputTensor* auf einen ganzzahligen Wert und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*
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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803050"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="351f9-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="351f9-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="351f9-104">Rundet jedes Element von *InputTensor* auf einen ganzzahligen Wert und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="351f9-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="351f9-105">Dieser Operator unterstützt die direkt ausgeführte Ausführung, was bedeutet, dass *OutputTensor* während der Bindung den Alias *InputTensor* zulässt.</span><span class="sxs-lookup"><span data-stu-id="351f9-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="351f9-106">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="351f9-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="351f9-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="351f9-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="351f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="351f9-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="351f9-109">Member</span><span class="sxs-lookup"><span data-stu-id="351f9-109">Members</span></span>

`InputTensor`

<span data-ttu-id="351f9-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="351f9-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="351f9-111">Der Eingabe-Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="351f9-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="351f9-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="351f9-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="351f9-113">Der Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="351f9-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="351f9-114">Typ: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="351f9-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="351f9-115">Ein [DML_ROUNDING_MODE,](/windows/win32/api/directml/ne-directml-dml_rounding_mode) der die Richtung bestimmt, in die gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="351f9-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="351f9-116">Wenn **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN:** Werte werden auf die nächste ganze Zahl gerundet, wobei werte in der Mitte (z. B. 0,5) auf die nächste gerade ganze Zahl gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="351f9-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="351f9-117">Wenn **DML_ROUNDING_MODE_TOWARD_ZERO**: Werte werden auf 0 (null) gerundet.</span><span class="sxs-lookup"><span data-stu-id="351f9-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="351f9-118">Dadurch wird der Bruchteil effektiv abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="351f9-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="351f9-119">Wenn **DML_ROUNDING_MODE_TOWARD_INFINITY**: Werte werden auf die nächste ganze Zahl gerundet, wobei die werte auf halbem Weg (z. B. 0,5) von 0 (in Richtung positiv oder negativ unendlich, abhängig vom Vorzeichen des Werts) gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="351f9-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="351f9-120">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="351f9-120">Availability</span></span>
<span data-ttu-id="351f9-121">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="351f9-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="351f9-122">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="351f9-122">Tensor constraints</span></span>
<span data-ttu-id="351f9-123">*InputTensor* und *OutputTensor* müssen die gleichen *Datentypen*, *DimensionCount* und *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="351f9-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="351f9-124">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="351f9-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="351f9-125">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="351f9-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="351f9-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="351f9-126">Tensor</span></span> | <span data-ttu-id="351f9-127">Typ</span><span class="sxs-lookup"><span data-stu-id="351f9-127">Kind</span></span> | <span data-ttu-id="351f9-128">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="351f9-128">Supported dimension counts</span></span> | <span data-ttu-id="351f9-129">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="351f9-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="351f9-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="351f9-130">InputTensor</span></span> | <span data-ttu-id="351f9-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="351f9-131">Input</span></span> | <span data-ttu-id="351f9-132">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="351f9-132">1 to 8</span></span> | <span data-ttu-id="351f9-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="351f9-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="351f9-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="351f9-134">OutputTensor</span></span> | <span data-ttu-id="351f9-135">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="351f9-135">Output</span></span> | <span data-ttu-id="351f9-136">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="351f9-136">1 to 8</span></span> | <span data-ttu-id="351f9-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="351f9-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="351f9-138">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="351f9-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="351f9-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="351f9-139">Tensor</span></span> | <span data-ttu-id="351f9-140">Typ</span><span class="sxs-lookup"><span data-stu-id="351f9-140">Kind</span></span> | <span data-ttu-id="351f9-141">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="351f9-141">Supported dimension counts</span></span> | <span data-ttu-id="351f9-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="351f9-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="351f9-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="351f9-143">InputTensor</span></span> | <span data-ttu-id="351f9-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="351f9-144">Input</span></span> | <span data-ttu-id="351f9-145">4</span><span class="sxs-lookup"><span data-stu-id="351f9-145">4</span></span> | <span data-ttu-id="351f9-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="351f9-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="351f9-147">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="351f9-147">OutputTensor</span></span> | <span data-ttu-id="351f9-148">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="351f9-148">Output</span></span> | <span data-ttu-id="351f9-149">4</span><span class="sxs-lookup"><span data-stu-id="351f9-149">4</span></span> | <span data-ttu-id="351f9-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="351f9-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="351f9-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="351f9-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="351f9-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="351f9-152">**Header**</span></span> | <span data-ttu-id="351f9-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="351f9-153">directml.h</span></span> |