---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
description: Führt einen logischen *kleiner-als-oder gleich* -Wert für jedes Paar entsprechender Elemente der Eingabe-Tensoren aus, wobei das Ergebnis (1 für true, 0 für false) in das entsprechende Element von *outputtensor* gestellt wird.
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
ms.openlocfilehash: 815c7ea148d6754cb410da6aeedaf31ab6cd7ece
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106349755"
---
# <a name="dml_element_wise_logical_less_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="fe211-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="fe211-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="fe211-104">Führt einen logischen *kleiner-als-oder gleich* -Wert für jedes Paar entsprechender Elemente der Eingabe-Tensoren aus, wobei das Ergebnis (1 für true, 0 für false) in das entsprechende Element von *outputtensor* gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fe211-104">Performs a logical *less than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a <= b)
```

> [!IMPORTANT]
> <span data-ttu-id="fe211-105">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="fe211-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="fe211-106">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fe211-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe211-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe211-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="fe211-108">Member</span><span class="sxs-lookup"><span data-stu-id="fe211-108">Members</span></span>

`ATensor`

<span data-ttu-id="fe211-109">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe211-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe211-110">Ein tensorflow, der die Links neben Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="fe211-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="fe211-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe211-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe211-112">Ein tensorflow, der die Eingaben auf der rechten Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="fe211-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="fe211-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe211-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe211-114">Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fe211-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="fe211-115">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="fe211-115">Availability</span></span>
<span data-ttu-id="fe211-116">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="fe211-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="fe211-117">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="fe211-117">Tensor constraints</span></span>
* <span data-ttu-id="fe211-118">*Atensor* und *btensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fe211-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="fe211-119">*Atensor*, *btensor* und *outputtensor* müssen die gleiche *DimensionCount* und *Größe* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fe211-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fe211-120">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="fe211-120">Tensor support</span></span>
| <span data-ttu-id="fe211-121">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="fe211-121">Tensor</span></span> | <span data-ttu-id="fe211-122">Typ</span><span class="sxs-lookup"><span data-stu-id="fe211-122">Kind</span></span> | <span data-ttu-id="fe211-123">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="fe211-123">Supported dimension counts</span></span> | <span data-ttu-id="fe211-124">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="fe211-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fe211-125">Atensor</span><span class="sxs-lookup"><span data-stu-id="fe211-125">ATensor</span></span> | <span data-ttu-id="fe211-126">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe211-126">Input</span></span> | <span data-ttu-id="fe211-127">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="fe211-127">1 to 8</span></span> | <span data-ttu-id="fe211-128">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="fe211-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fe211-129">Btensor</span><span class="sxs-lookup"><span data-stu-id="fe211-129">BTensor</span></span> | <span data-ttu-id="fe211-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe211-130">Input</span></span> | <span data-ttu-id="fe211-131">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="fe211-131">1 to 8</span></span> | <span data-ttu-id="fe211-132">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="fe211-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fe211-133">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="fe211-133">OutputTensor</span></span> | <span data-ttu-id="fe211-134">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fe211-134">Output</span></span> | <span data-ttu-id="fe211-135">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="fe211-135">1 to 8</span></span> | <span data-ttu-id="fe211-136">UInt32, Uint8</span><span class="sxs-lookup"><span data-stu-id="fe211-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="fe211-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe211-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fe211-138">**Header**</span><span class="sxs-lookup"><span data-stu-id="fe211-138">**Header**</span></span> | <span data-ttu-id="fe211-139">directml. h</span><span class="sxs-lookup"><span data-stu-id="fe211-139">directml.h</span></span> |