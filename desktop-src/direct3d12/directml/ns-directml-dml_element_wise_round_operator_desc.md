---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Rundet jedes Element von " *inputtensor* " auf einen ganzzahligen Wert, wobei das Ergebnis in das entsprechende Element von " *outputtensor*" platziert wird.
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
ms.openlocfilehash: f0964ae133c61b3a596b644630d363f902635585
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361740"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="ed5e5-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="ed5e5-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="ed5e5-104">Rundet jedes Element von " *inputtensor* " auf einen ganzzahligen Wert, wobei das Ergebnis in das entsprechende Element von " *outputtensor*" platziert wird.</span><span class="sxs-lookup"><span data-stu-id="ed5e5-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="ed5e5-105">Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass *outputtensor* während der Bindung den Alias *inputtensor* zulässt.</span><span class="sxs-lookup"><span data-stu-id="ed5e5-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed5e5-106">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="ed5e5-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="ed5e5-107">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ed5e5-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed5e5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed5e5-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="ed5e5-109">Member</span><span class="sxs-lookup"><span data-stu-id="ed5e5-109">Members</span></span>

`InputTensor`

<span data-ttu-id="ed5e5-110">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ed5e5-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ed5e5-111">Der eingabetensor, aus dem gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="ed5e5-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="ed5e5-112">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ed5e5-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ed5e5-113">Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed5e5-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="ed5e5-114">Typ: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="ed5e5-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="ed5e5-115">Eine [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) die die Richtung bestimmt, zu der abgerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed5e5-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="ed5e5-116">Wenn **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**:-Werte auf die nächste ganze Zahl gerundet werden, wobei die Hälfte der Werte (z. b. 0,5) auf die nächste gerade ganze Zahl gerundet wird.</span><span class="sxs-lookup"><span data-stu-id="ed5e5-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="ed5e5-117">, Wenn **DML_ROUNDING_MODE_TOWARD_ZERO**:-Werte in Richtung NULL gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="ed5e5-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="ed5e5-118">Dadurch wird der Bruchteile effektiv abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="ed5e5-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="ed5e5-119">Wenn **DML_ROUNDING_MODE_TOWARD_INFINITY**:-Werte auf die nächste ganze Zahl gerundet werden, wobei die Hälfte der Werte (z. b. 0,5) von 0 (null) gerundet wird (in Richtung positiv oder minus unendlich, je nach Vorzeichen des Werts).</span><span class="sxs-lookup"><span data-stu-id="ed5e5-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="ed5e5-120">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ed5e5-120">Availability</span></span>
<span data-ttu-id="ed5e5-121">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ed5e5-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ed5e5-122">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="ed5e5-122">Tensor constraints</span></span>
<span data-ttu-id="ed5e5-123">*Inputtensor* und *outputtensor* müssen denselben *Datentyp*, jede *DimensionCount* und jede *Größe* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ed5e5-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ed5e5-124">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ed5e5-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="ed5e5-125">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="ed5e5-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="ed5e5-126">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="ed5e5-126">Tensor</span></span> | <span data-ttu-id="ed5e5-127">Typ</span><span class="sxs-lookup"><span data-stu-id="ed5e5-127">Kind</span></span> | <span data-ttu-id="ed5e5-128">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="ed5e5-128">Supported dimension counts</span></span> | <span data-ttu-id="ed5e5-129">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="ed5e5-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ed5e5-130">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="ed5e5-130">InputTensor</span></span> | <span data-ttu-id="ed5e5-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed5e5-131">Input</span></span> | <span data-ttu-id="ed5e5-132">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="ed5e5-132">1 to 8</span></span> | <span data-ttu-id="ed5e5-133">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ed5e5-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ed5e5-134">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="ed5e5-134">OutputTensor</span></span> | <span data-ttu-id="ed5e5-135">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="ed5e5-135">Output</span></span> | <span data-ttu-id="ed5e5-136">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="ed5e5-136">1 to 8</span></span> | <span data-ttu-id="ed5e5-137">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ed5e5-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="ed5e5-138">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="ed5e5-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="ed5e5-139">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="ed5e5-139">Tensor</span></span> | <span data-ttu-id="ed5e5-140">Typ</span><span class="sxs-lookup"><span data-stu-id="ed5e5-140">Kind</span></span> | <span data-ttu-id="ed5e5-141">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="ed5e5-141">Supported dimension counts</span></span> | <span data-ttu-id="ed5e5-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="ed5e5-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ed5e5-143">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="ed5e5-143">InputTensor</span></span> | <span data-ttu-id="ed5e5-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed5e5-144">Input</span></span> | <span data-ttu-id="ed5e5-145">4</span><span class="sxs-lookup"><span data-stu-id="ed5e5-145">4</span></span> | <span data-ttu-id="ed5e5-146">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ed5e5-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ed5e5-147">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="ed5e5-147">OutputTensor</span></span> | <span data-ttu-id="ed5e5-148">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="ed5e5-148">Output</span></span> | <span data-ttu-id="ed5e5-149">4</span><span class="sxs-lookup"><span data-stu-id="ed5e5-149">4</span></span> | <span data-ttu-id="ed5e5-150">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ed5e5-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="ed5e5-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed5e5-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ed5e5-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="ed5e5-152">**Header**</span></span> | <span data-ttu-id="ed5e5-153">directml. h</span><span class="sxs-lookup"><span data-stu-id="ed5e5-153">directml.h</span></span> |