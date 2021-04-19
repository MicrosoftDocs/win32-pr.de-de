---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: Führt eine logische Rechte Verschiebung der einzelnen Elemente des *atensor* durch eine Anzahl von Bits aus, die vom entsprechenden *btensor*-Element angegeben werden, und platziert das Ergebnis in das entsprechende Element von *outputtensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_right_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.openlocfilehash: 447b0f685b51bf8b146644de3b5f65390a492ffd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106355094"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="3cc6c-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="3cc6c-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="3cc6c-104">Führt eine logische Rechte Verschiebung der einzelnen Elemente des *atensor* durch eine Anzahl von Bits aus, die vom entsprechenden *btensor*-Element angegeben werden, und platziert das Ergebnis in das entsprechende Element von *outputtensor*.</span><span class="sxs-lookup"><span data-stu-id="3cc6c-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="3cc6c-105">Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass *outputtensor* bei der Bindung eine der Eingabe-Tensoren Alias zulässt.</span><span class="sxs-lookup"><span data-stu-id="3cc6c-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3cc6c-106">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="3cc6c-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="3cc6c-107">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="3cc6c-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc6c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cc6c-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="3cc6c-109">Member</span><span class="sxs-lookup"><span data-stu-id="3cc6c-109">Members</span></span>

`ATensor`

<span data-ttu-id="3cc6c-110">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3cc6c-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3cc6c-111">Ein tensorflow, der die Links neben Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="3cc6c-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="3cc6c-112">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3cc6c-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3cc6c-113">Ein tensorflow, der die Eingaben auf der rechten Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="3cc6c-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="3cc6c-114">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3cc6c-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3cc6c-115">Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3cc6c-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="3cc6c-116">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="3cc6c-116">Availability</span></span>
<span data-ttu-id="3cc6c-117">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="3cc6c-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="3cc6c-118">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="3cc6c-118">Tensor constraints</span></span>
<span data-ttu-id="3cc6c-119">*Atensor*, *btensor* und *outputtensor* müssen denselben *Datentyp*, jede *DimensionCount* und jede *Größe* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3cc6c-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="3cc6c-120">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="3cc6c-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="3cc6c-121">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="3cc6c-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="3cc6c-122">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="3cc6c-122">Tensor</span></span> | <span data-ttu-id="3cc6c-123">Typ</span><span class="sxs-lookup"><span data-stu-id="3cc6c-123">Kind</span></span> | <span data-ttu-id="3cc6c-124">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="3cc6c-124">Supported dimension counts</span></span> | <span data-ttu-id="3cc6c-125">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="3cc6c-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="3cc6c-126">Atensor</span><span class="sxs-lookup"><span data-stu-id="3cc6c-126">ATensor</span></span> | <span data-ttu-id="3cc6c-127">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3cc6c-127">Input</span></span> | <span data-ttu-id="3cc6c-128">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="3cc6c-128">1 to 8</span></span> | <span data-ttu-id="3cc6c-129">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="3cc6c-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="3cc6c-130">Btensor</span><span class="sxs-lookup"><span data-stu-id="3cc6c-130">BTensor</span></span> | <span data-ttu-id="3cc6c-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3cc6c-131">Input</span></span> | <span data-ttu-id="3cc6c-132">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="3cc6c-132">1 to 8</span></span> | <span data-ttu-id="3cc6c-133">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="3cc6c-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="3cc6c-134">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="3cc6c-134">OutputTensor</span></span> | <span data-ttu-id="3cc6c-135">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="3cc6c-135">Output</span></span> | <span data-ttu-id="3cc6c-136">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="3cc6c-136">1 to 8</span></span> | <span data-ttu-id="3cc6c-137">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="3cc6c-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="3cc6c-138">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="3cc6c-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="3cc6c-139">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="3cc6c-139">Tensor</span></span> | <span data-ttu-id="3cc6c-140">Typ</span><span class="sxs-lookup"><span data-stu-id="3cc6c-140">Kind</span></span> | <span data-ttu-id="3cc6c-141">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="3cc6c-141">Supported dimension counts</span></span> | <span data-ttu-id="3cc6c-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="3cc6c-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="3cc6c-143">Atensor</span><span class="sxs-lookup"><span data-stu-id="3cc6c-143">ATensor</span></span> | <span data-ttu-id="3cc6c-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3cc6c-144">Input</span></span> | <span data-ttu-id="3cc6c-145">4</span><span class="sxs-lookup"><span data-stu-id="3cc6c-145">4</span></span> | <span data-ttu-id="3cc6c-146">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="3cc6c-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="3cc6c-147">Btensor</span><span class="sxs-lookup"><span data-stu-id="3cc6c-147">BTensor</span></span> | <span data-ttu-id="3cc6c-148">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3cc6c-148">Input</span></span> | <span data-ttu-id="3cc6c-149">4</span><span class="sxs-lookup"><span data-stu-id="3cc6c-149">4</span></span> | <span data-ttu-id="3cc6c-150">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="3cc6c-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="3cc6c-151">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="3cc6c-151">OutputTensor</span></span> | <span data-ttu-id="3cc6c-152">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="3cc6c-152">Output</span></span> | <span data-ttu-id="3cc6c-153">4</span><span class="sxs-lookup"><span data-stu-id="3cc6c-153">4</span></span> | <span data-ttu-id="3cc6c-154">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="3cc6c-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="3cc6c-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cc6c-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3cc6c-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="3cc6c-156">**Header**</span></span> | <span data-ttu-id="3cc6c-157">directml. h</span><span class="sxs-lookup"><span data-stu-id="3cc6c-157">directml.h</span></span> |