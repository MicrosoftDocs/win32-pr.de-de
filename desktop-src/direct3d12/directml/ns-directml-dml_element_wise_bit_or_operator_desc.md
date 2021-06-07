---
UID: NS:directml.DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
description: Berechnet das bitweise OR zwischen jedem entsprechenden Element der Eingabetensoren und schreibt das Ergebnis in den Ausgabetensor.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.openlocfilehash: 7138c6647e1bd4df5d8957468ca67f103f4a3f5a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417879"
---
# <a name="dml_element_wise_bit_or_operator_desc-structure-directmlh"></a><span data-ttu-id="e8a01-103">DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="e8a01-103">DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e8a01-104">Berechnet das bitweise OR zwischen jedem entsprechenden Element der Eingabetensoren und schreibt das Ergebnis in den Ausgabetensor.</span><span class="sxs-lookup"><span data-stu-id="e8a01-104">Computes the bitwise OR between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="e8a01-105">Der Eingabe- und Ausgabe-Tensor muss denselben *DimensionCount-,* *Sizes-* und *DataType-Wert aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="e8a01-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="e8a01-106">Dieser Operator unterstützt die ausführungsbasierte Ausführung, was bedeutet, dass der Ausgabetensor während der Bindung einen Alias für einen oder mehrere Eingabetensoren verwenden darf.</span><span class="sxs-lookup"><span data-stu-id="e8a01-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8a01-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="e8a01-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e8a01-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="e8a01-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a01-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8a01-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="e8a01-110">Member</span><span class="sxs-lookup"><span data-stu-id="e8a01-110">Members</span></span>

`ATensor`

<span data-ttu-id="e8a01-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8a01-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8a01-112">Ein Tensor, der die eingaben auf der linken Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="e8a01-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="e8a01-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8a01-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8a01-114">Ein Tensor, der die eingaben auf der rechten Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="e8a01-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="e8a01-115">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8a01-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8a01-116">Der Ausgabe tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e8a01-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="e8a01-117">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="e8a01-117">Availability</span></span>
<span data-ttu-id="e8a01-118">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e8a01-118">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e8a01-119">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="e8a01-119">Tensor constraints</span></span>
<span data-ttu-id="e8a01-120">*ATensor,* *BTensor* und *OutputTensor* müssen denselben *DataType,* *DimensionCount* und *die gleichen Größen aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="e8a01-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e8a01-121">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="e8a01-121">Tensor support</span></span>
| <span data-ttu-id="e8a01-122">Tensor</span><span class="sxs-lookup"><span data-stu-id="e8a01-122">Tensor</span></span> | <span data-ttu-id="e8a01-123">Typ</span><span class="sxs-lookup"><span data-stu-id="e8a01-123">Kind</span></span> | <span data-ttu-id="e8a01-124">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="e8a01-124">Supported dimension counts</span></span> | <span data-ttu-id="e8a01-125">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="e8a01-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e8a01-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="e8a01-126">ATensor</span></span> | <span data-ttu-id="e8a01-127">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8a01-127">Input</span></span> | <span data-ttu-id="e8a01-128">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="e8a01-128">1 to 8</span></span> | <span data-ttu-id="e8a01-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e8a01-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e8a01-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="e8a01-130">BTensor</span></span> | <span data-ttu-id="e8a01-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8a01-131">Input</span></span> | <span data-ttu-id="e8a01-132">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="e8a01-132">1 to 8</span></span> | <span data-ttu-id="e8a01-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e8a01-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e8a01-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e8a01-134">OutputTensor</span></span> | <span data-ttu-id="e8a01-135">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e8a01-135">Output</span></span> | <span data-ttu-id="e8a01-136">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="e8a01-136">1 to 8</span></span> | <span data-ttu-id="e8a01-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e8a01-137">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="e8a01-138">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e8a01-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e8a01-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="e8a01-139">**Header**</span></span> | <span data-ttu-id="e8a01-140">directml.h</span><span class="sxs-lookup"><span data-stu-id="e8a01-140">directml.h</span></span> |