---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
description: Führt für *jedes* Paar der entsprechenden Elemente der Eingabetensoren einen logischen kleineren oder gleich aus, und platziert das Ergebnis (1 für true, 0 für false) im entsprechenden Element von *OutputTensor*.
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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803075"
---
# <a name="dml_element_wise_logical_less_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="b4e49-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="b4e49-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b4e49-104">Führt für *jedes* Paar der entsprechenden Elemente der Eingabetensoren einen logischen kleineren oder gleich aus und platziert das Ergebnis (1 für true, 0 für false) im entsprechenden Element von *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b4e49-104">Performs a logical *less than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a <= b)
```

> [!IMPORTANT]
> <span data-ttu-id="b4e49-105">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="b4e49-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b4e49-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="b4e49-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e49-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4e49-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="b4e49-108">Member</span><span class="sxs-lookup"><span data-stu-id="b4e49-108">Members</span></span>

`ATensor`

<span data-ttu-id="b4e49-109">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b4e49-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b4e49-110">Ein Tensor, der die eingaben auf der linken Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="b4e49-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="b4e49-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b4e49-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b4e49-112">Ein Tensor, der die eingaben auf der rechten Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="b4e49-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="b4e49-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b4e49-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b4e49-114">Der Ausgabe tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b4e49-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="b4e49-115">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="b4e49-115">Availability</span></span>
<span data-ttu-id="b4e49-116">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b4e49-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b4e49-117">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="b4e49-117">Tensor constraints</span></span>
* <span data-ttu-id="b4e49-118">*ATensor und* *BTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="b4e49-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="b4e49-119">*ATensor,* *BTensor* und *OutputTensor* müssen über die gleichen *DimensionCount-* und *Sizes-Größen verfügen.*</span><span class="sxs-lookup"><span data-stu-id="b4e49-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b4e49-120">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="b4e49-120">Tensor support</span></span>
| <span data-ttu-id="b4e49-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="b4e49-121">Tensor</span></span> | <span data-ttu-id="b4e49-122">Typ</span><span class="sxs-lookup"><span data-stu-id="b4e49-122">Kind</span></span> | <span data-ttu-id="b4e49-123">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="b4e49-123">Supported dimension counts</span></span> | <span data-ttu-id="b4e49-124">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="b4e49-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b4e49-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="b4e49-125">ATensor</span></span> | <span data-ttu-id="b4e49-126">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b4e49-126">Input</span></span> | <span data-ttu-id="b4e49-127">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="b4e49-127">1 to 8</span></span> | <span data-ttu-id="b4e49-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b4e49-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b4e49-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="b4e49-129">BTensor</span></span> | <span data-ttu-id="b4e49-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b4e49-130">Input</span></span> | <span data-ttu-id="b4e49-131">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="b4e49-131">1 to 8</span></span> | <span data-ttu-id="b4e49-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b4e49-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b4e49-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b4e49-133">OutputTensor</span></span> | <span data-ttu-id="b4e49-134">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="b4e49-134">Output</span></span> | <span data-ttu-id="b4e49-135">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="b4e49-135">1 to 8</span></span> | <span data-ttu-id="b4e49-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="b4e49-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="b4e49-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4e49-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b4e49-138">**Header**</span><span class="sxs-lookup"><span data-stu-id="b4e49-138">**Header**</span></span> | <span data-ttu-id="b4e49-139">directml.h</span><span class="sxs-lookup"><span data-stu-id="b4e49-139">directml.h</span></span> |