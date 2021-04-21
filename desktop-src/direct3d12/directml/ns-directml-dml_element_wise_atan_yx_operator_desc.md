---
UID: NS:directml.DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
title: DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
description: Berechnet den Arkatangent mit zwei Argumenten für jedes Element von *ATensor* und *BTensor,* wobei *ATensor* die *Y-Achse* und *BTensor* die *X-Achse* ist, wobei das Ergebnis im entsprechenden Element von *OutputTensor platziert wird.*
helpviewer_keywords:
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.openlocfilehash: 6031f08dc99db943d26ab5212896b4fb44987269
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804449"
---
# <a name="dml_element_wise_atan_yx_operator_desc-directmlh"></a><span data-ttu-id="d1de9-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="d1de9-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="d1de9-104">Berechnet den Arkatangent mit zwei Argumenten für jedes Element von *ATensor* und *BTensor,* wobei *ATensor* die *Y-Achse* und *BTensor* die *X-Achse* ist, wobei das Ergebnis im entsprechenden Element von *OutputTensor platziert wird.*</span><span class="sxs-lookup"><span data-stu-id="d1de9-104">Computes the 2-argument arctangent for each element of *ATensor* and *BTensor*, where *ATensor* is the *Y-axis* and *BTensor* is the *X-axis*, placing the result into the corresponding element of *OutputTensor*.</span></span> <span data-ttu-id="d1de9-105">Dieser Operator ist für den Ursprung nicht definiert (d. h., wenn *ATensor* und *BTensor* beide 0 für entsprechende Elemente sind).</span><span class="sxs-lookup"><span data-stu-id="d1de9-105">This operator is undefined for the origin (that is, when *ATensor* and *BTensor* are both 0 for corresponding elements).</span></span>

![GRU_Forward](../images/atan2.png)

```
f(y, x) = atan2(y, x)
```

<span data-ttu-id="d1de9-107">Dieser Operator unterstützt die ausführungsbasierte Ausführung, was bedeutet, dass der Ausgabetensor während der Bindung einen Alias *für ATensor* oder *BTensor* verwenden darf.</span><span class="sxs-lookup"><span data-stu-id="d1de9-107">This operator supports in-place execution, meaning that the output tensor is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1de9-108">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.5 und höher).</span><span class="sxs-lookup"><span data-stu-id="d1de9-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="d1de9-109">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="d1de9-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1de9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1de9-110">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="d1de9-111">Member</span><span class="sxs-lookup"><span data-stu-id="d1de9-111">Members</span></span>

`ATensor`

<span data-ttu-id="d1de9-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d1de9-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d1de9-113">Der Eingabetensor, aus dem die Werte der Y-Achse gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="d1de9-113">The input tensor to read the Y-axis values from.</span></span>

`BTensor`

<span data-ttu-id="d1de9-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d1de9-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d1de9-115">Der Eingabe tensor, aus dem die X-Achsenwerte gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="d1de9-115">The input tensor to read the X-axis values from.</span></span>

`OutputTensor`

<span data-ttu-id="d1de9-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d1de9-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d1de9-117">Der Ausgabe tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d1de9-117">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="d1de9-118">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="d1de9-118">Availability</span></span>
<span data-ttu-id="d1de9-119">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d1de9-119">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d1de9-120">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d1de9-120">Tensor constraints</span></span>
<span data-ttu-id="d1de9-121">*ATensor,* *BTensor* und *OutputTensor* müssen denselben *DataType,* *DimensionCount* und *die gleichen Größen aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="d1de9-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d1de9-122">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d1de9-122">Tensor support</span></span>
| <span data-ttu-id="d1de9-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="d1de9-123">Tensor</span></span> | <span data-ttu-id="d1de9-124">Typ</span><span class="sxs-lookup"><span data-stu-id="d1de9-124">Kind</span></span> | <span data-ttu-id="d1de9-125">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="d1de9-125">Supported dimension counts</span></span> | <span data-ttu-id="d1de9-126">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="d1de9-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d1de9-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="d1de9-127">ATensor</span></span> | <span data-ttu-id="d1de9-128">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d1de9-128">Input</span></span> | <span data-ttu-id="d1de9-129">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="d1de9-129">1 to 8</span></span> | <span data-ttu-id="d1de9-130">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d1de9-130">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d1de9-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="d1de9-131">BTensor</span></span> | <span data-ttu-id="d1de9-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d1de9-132">Input</span></span> | <span data-ttu-id="d1de9-133">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="d1de9-133">1 to 8</span></span> | <span data-ttu-id="d1de9-134">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d1de9-134">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d1de9-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d1de9-135">OutputTensor</span></span> | <span data-ttu-id="d1de9-136">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="d1de9-136">Output</span></span> | <span data-ttu-id="d1de9-137">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="d1de9-137">1 to 8</span></span> | <span data-ttu-id="d1de9-138">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d1de9-138">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="d1de9-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1de9-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d1de9-140">**Header**</span><span class="sxs-lookup"><span data-stu-id="d1de9-140">**Header**</span></span> | <span data-ttu-id="d1de9-141">directml.h</span><span class="sxs-lookup"><span data-stu-id="d1de9-141">directml.h</span></span> |
