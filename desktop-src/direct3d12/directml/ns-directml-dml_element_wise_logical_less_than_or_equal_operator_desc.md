---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
description: Führt ein logisches *kleiner als oder gleich für* jedes Paar der entsprechenden Elemente der Eingabe tensors aus, wobei das Ergebnis (1 für TRUE, 0 für FALSE) in das entsprechende Element von *OutputTensor* platziert wird.
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: d1b8a282154b2b714daf061e2bb3f88b359209d4
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417623"
---
# <a name="dml_element_wise_logical_less_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="ae8a6-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="ae8a6-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="ae8a6-104">Führt ein logisches *kleiner als oder gleich für* jedes Paar der entsprechenden Elemente der Eingabe tensors aus, wobei das Ergebnis (1 für TRUE, 0 für FALSE) in das entsprechende Element von *OutputTensor* platziert wird.</span><span class="sxs-lookup"><span data-stu-id="ae8a6-104">Performs a logical *less than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a <= b)
```

> [!IMPORTANT]
> <span data-ttu-id="ae8a6-105">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="ae8a6-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ae8a6-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="ae8a6-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae8a6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae8a6-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="ae8a6-108">Member</span><span class="sxs-lookup"><span data-stu-id="ae8a6-108">Members</span></span>

`ATensor`

<span data-ttu-id="ae8a6-109">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ae8a6-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ae8a6-110">Ein Tensor, der die linken Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="ae8a6-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="ae8a6-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ae8a6-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ae8a6-112">Ein Tensor, der die rechten Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="ae8a6-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="ae8a6-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ae8a6-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ae8a6-114">Der Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae8a6-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="ae8a6-115">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ae8a6-115">Availability</span></span>
<span data-ttu-id="ae8a6-116">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ae8a6-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ae8a6-117">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="ae8a6-117">Tensor constraints</span></span>
* <span data-ttu-id="ae8a6-118">*ATensor* und *BTensor* müssen den gleichen *Datentyp aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="ae8a6-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="ae8a6-119">*ATensor,* *BTensor* und *OutputTensor* müssen die gleichen *DimensionCount-* und *Größen aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="ae8a6-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ae8a6-120">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ae8a6-120">Tensor support</span></span>
| <span data-ttu-id="ae8a6-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="ae8a6-121">Tensor</span></span> | <span data-ttu-id="ae8a6-122">Typ</span><span class="sxs-lookup"><span data-stu-id="ae8a6-122">Kind</span></span> | <span data-ttu-id="ae8a6-123">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="ae8a6-123">Supported dimension counts</span></span> | <span data-ttu-id="ae8a6-124">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="ae8a6-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ae8a6-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="ae8a6-125">ATensor</span></span> | <span data-ttu-id="ae8a6-126">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ae8a6-126">Input</span></span> | <span data-ttu-id="ae8a6-127">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="ae8a6-127">1 to 8</span></span> | <span data-ttu-id="ae8a6-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="ae8a6-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="ae8a6-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="ae8a6-129">BTensor</span></span> | <span data-ttu-id="ae8a6-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ae8a6-130">Input</span></span> | <span data-ttu-id="ae8a6-131">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="ae8a6-131">1 to 8</span></span> | <span data-ttu-id="ae8a6-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="ae8a6-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="ae8a6-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="ae8a6-133">OutputTensor</span></span> | <span data-ttu-id="ae8a6-134">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="ae8a6-134">Output</span></span> | <span data-ttu-id="ae8a6-135">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="ae8a6-135">1 to 8</span></span> | <span data-ttu-id="ae8a6-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="ae8a6-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="ae8a6-137">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ae8a6-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ae8a6-138">**Header**</span><span class="sxs-lookup"><span data-stu-id="ae8a6-138">**Header**</span></span> | <span data-ttu-id="ae8a6-139">directml.h</span><span class="sxs-lookup"><span data-stu-id="ae8a6-139">directml.h</span></span> |