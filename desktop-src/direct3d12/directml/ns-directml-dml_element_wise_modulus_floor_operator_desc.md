---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
description: Berechnet den Modulus mit den gleichen Ergebnissen wie der python-Modulus für jedes Paar entsprechender Elemente aus den Eingabe-Tensoren, wobei das Ergebnis in das entsprechende Element von *outputtensor* platziert wird.
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
ms.openlocfilehash: a732a593fb10a5c8e18ec6dd9416ce8d62f43563
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106369919"
---
# <a name="dml_element_wise_modulus_floor_operator_desc-structure-directmlh"></a><span data-ttu-id="dad94-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="dad94-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="dad94-104">Berechnet den Modulus mit den gleichen Ergebnissen wie der python-Modulus für jedes Paar entsprechender Elemente aus den Eingabe-Tensoren, wobei das Ergebnis in das entsprechende Element von *outputtensor* platziert wird.</span><span class="sxs-lookup"><span data-stu-id="dad94-104">Computes the modulus, with the same results as the Python modulus, for each pair of corresponding elements from the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="dad94-105">Da der Quotienten auf-INF gerundet wird, hat das Ergebnis dasselbe Vorzeichen wie der Divisor.</span><span class="sxs-lookup"><span data-stu-id="dad94-105">Because the quotient is rounded towards -inf, the result will have the same sign as the divisor.</span></span>

```
f(a, b) = a - (b * floor(a / b))
```

<span data-ttu-id="dad94-106">Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass *outputtensor* bei der Bindung eine der Eingabe-Tensoren Alias zulässt.</span><span class="sxs-lookup"><span data-stu-id="dad94-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dad94-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="dad94-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="dad94-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="dad94-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dad94-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dad94-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="dad94-110">Member</span><span class="sxs-lookup"><span data-stu-id="dad94-110">Members</span></span>

`ATensor`

<span data-ttu-id="dad94-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dad94-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dad94-112">Ein tensorflow, der die Links neben Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="dad94-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="dad94-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dad94-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dad94-114">Ein tensorflow, der die Eingaben auf der rechten Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="dad94-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="dad94-115">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dad94-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dad94-116">Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dad94-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="dad94-117">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="dad94-117">Availability</span></span>
<span data-ttu-id="dad94-118">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="dad94-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="dad94-119">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="dad94-119">Tensor constraints</span></span>
<span data-ttu-id="dad94-120">*Atensor*, *btensor* und *outputtensor* müssen denselben *Datentyp*, jede *DimensionCount* und jede *Größe* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dad94-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="dad94-121">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="dad94-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="dad94-122">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="dad94-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="dad94-123">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="dad94-123">Tensor</span></span> | <span data-ttu-id="dad94-124">Typ</span><span class="sxs-lookup"><span data-stu-id="dad94-124">Kind</span></span> | <span data-ttu-id="dad94-125">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="dad94-125">Supported dimension counts</span></span> | <span data-ttu-id="dad94-126">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="dad94-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="dad94-127">Atensor</span><span class="sxs-lookup"><span data-stu-id="dad94-127">ATensor</span></span> | <span data-ttu-id="dad94-128">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dad94-128">Input</span></span> | <span data-ttu-id="dad94-129">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="dad94-129">1 to 8</span></span> | <span data-ttu-id="dad94-130">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="dad94-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="dad94-131">Btensor</span><span class="sxs-lookup"><span data-stu-id="dad94-131">BTensor</span></span> | <span data-ttu-id="dad94-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dad94-132">Input</span></span> | <span data-ttu-id="dad94-133">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="dad94-133">1 to 8</span></span> | <span data-ttu-id="dad94-134">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="dad94-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="dad94-135">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="dad94-135">OutputTensor</span></span> | <span data-ttu-id="dad94-136">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="dad94-136">Output</span></span> | <span data-ttu-id="dad94-137">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="dad94-137">1 to 8</span></span> | <span data-ttu-id="dad94-138">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="dad94-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="dad94-139">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="dad94-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="dad94-140">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="dad94-140">Tensor</span></span> | <span data-ttu-id="dad94-141">Typ</span><span class="sxs-lookup"><span data-stu-id="dad94-141">Kind</span></span> | <span data-ttu-id="dad94-142">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="dad94-142">Supported dimension counts</span></span> | <span data-ttu-id="dad94-143">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="dad94-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="dad94-144">Atensor</span><span class="sxs-lookup"><span data-stu-id="dad94-144">ATensor</span></span> | <span data-ttu-id="dad94-145">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dad94-145">Input</span></span> | <span data-ttu-id="dad94-146">4</span><span class="sxs-lookup"><span data-stu-id="dad94-146">4</span></span> | <span data-ttu-id="dad94-147">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="dad94-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="dad94-148">Btensor</span><span class="sxs-lookup"><span data-stu-id="dad94-148">BTensor</span></span> | <span data-ttu-id="dad94-149">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dad94-149">Input</span></span> | <span data-ttu-id="dad94-150">4</span><span class="sxs-lookup"><span data-stu-id="dad94-150">4</span></span> | <span data-ttu-id="dad94-151">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="dad94-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="dad94-152">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="dad94-152">OutputTensor</span></span> | <span data-ttu-id="dad94-153">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="dad94-153">Output</span></span> | <span data-ttu-id="dad94-154">4</span><span class="sxs-lookup"><span data-stu-id="dad94-154">4</span></span> | <span data-ttu-id="dad94-155">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="dad94-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="dad94-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dad94-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="dad94-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="dad94-157">**Header**</span></span> | <span data-ttu-id="dad94-158">directml. h</span><span class="sxs-lookup"><span data-stu-id="dad94-158">directml.h</span></span> |