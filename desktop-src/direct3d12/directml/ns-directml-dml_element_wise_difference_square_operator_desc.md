---
UID: NS:directml.DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
title: DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
description: Subtrahiert jedes Element von *BTensor* vom entsprechenden Element von *ATensor,* multipliziert das Ergebnis selbst und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*
helpviewer_keywords:
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.openlocfilehash: 3e3e7ab8f222f42def82a168ed861e58347f3b20
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804443"
---
# <a name="dml_element_wise_difference_square_operator_desc-directmlh"></a><span data-ttu-id="548e6-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="548e6-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="548e6-104">Subtrahiert jedes Element von *BTensor* vom entsprechenden Element von *ATensor,* multipliziert das Ergebnis selbst und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="548e6-104">Subtracts each element of *BTensor* from the corresponding element of *ATensor*, multiplies the result by itself, and places the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a - b) * (a - b)
```

<span data-ttu-id="548e6-105">Dieser Operator unterstützt die direkt ausgeführte Ausführung, was bedeutet, dass *OutputTensor* während der Bindung den Alias *ATensor* oder *BTensor* erhält.</span><span class="sxs-lookup"><span data-stu-id="548e6-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="548e6-106">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher).</span><span class="sxs-lookup"><span data-stu-id="548e6-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="548e6-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="548e6-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="548e6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="548e6-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="548e6-109">Member</span><span class="sxs-lookup"><span data-stu-id="548e6-109">Members</span></span>

`ATensor`

<span data-ttu-id="548e6-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="548e6-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="548e6-111">Ein Tensor, der die eingaben auf der linken Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="548e6-111">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="548e6-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="548e6-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="548e6-113">Ein Tensor, der die rechten Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="548e6-113">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="548e6-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="548e6-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="548e6-115">Der Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="548e6-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="548e6-116">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="548e6-116">Availability</span></span>
<span data-ttu-id="548e6-117">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="548e6-117">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="548e6-118">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="548e6-118">Tensor constraints</span></span>
<span data-ttu-id="548e6-119">*ATensor,* *BTensor* und *OutputTensor* müssen die gleichen *Datentypen*, *DimensionCount* und *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="548e6-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="548e6-120">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="548e6-120">Tensor support</span></span>
| <span data-ttu-id="548e6-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="548e6-121">Tensor</span></span> | <span data-ttu-id="548e6-122">Typ</span><span class="sxs-lookup"><span data-stu-id="548e6-122">Kind</span></span> | <span data-ttu-id="548e6-123">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="548e6-123">Supported dimension counts</span></span> | <span data-ttu-id="548e6-124">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="548e6-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="548e6-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="548e6-125">ATensor</span></span> | <span data-ttu-id="548e6-126">Eingabe</span><span class="sxs-lookup"><span data-stu-id="548e6-126">Input</span></span> | <span data-ttu-id="548e6-127">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="548e6-127">1 to 8</span></span> | <span data-ttu-id="548e6-128">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="548e6-128">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="548e6-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="548e6-129">BTensor</span></span> | <span data-ttu-id="548e6-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="548e6-130">Input</span></span> | <span data-ttu-id="548e6-131">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="548e6-131">1 to 8</span></span> | <span data-ttu-id="548e6-132">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="548e6-132">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="548e6-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="548e6-133">OutputTensor</span></span> | <span data-ttu-id="548e6-134">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="548e6-134">Output</span></span> | <span data-ttu-id="548e6-135">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="548e6-135">1 to 8</span></span> | <span data-ttu-id="548e6-136">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="548e6-136">FLOAT32, FLOAT16, INT32, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="548e6-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="548e6-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="548e6-138">**Header**</span><span class="sxs-lookup"><span data-stu-id="548e6-138">**Header**</span></span> | <span data-ttu-id="548e6-139">directml.h</span><span class="sxs-lookup"><span data-stu-id="548e6-139">directml.h</span></span> |
