---
UID: NS:directml.DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
description: Berechnet die bitweise Aufzählung (die Anzahl von Bits, die auf 1 festgelegt ist) für jedes Element des Eingabetensors und schreibt das Ergebnis in den Ausgabetensor.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.openlocfilehash: 3c8dddc3159ebcd857c7423b76856fbeba465d2e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803229"
---
# <a name="dml_element_wise_bit_count_operator_desc-structure-directmlh"></a><span data-ttu-id="b19cd-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="b19cd-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b19cd-104">Berechnet die bitweise Aufzählung (die Anzahl von Bits, die auf 1 festgelegt ist) für jedes Element des Eingabetensors und schreibt das Ergebnis in den Ausgabetensor.</span><span class="sxs-lookup"><span data-stu-id="b19cd-104">Computes the bitwise population count (the number of bits set to 1) for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="b19cd-105">Der Eingabe- und Ausgabe-Tensor muss über die gleichen *DimensionCount-* und *Sizes-Größen* verfügen, obwohl sie sich in *DataType unterscheiden können.*</span><span class="sxs-lookup"><span data-stu-id="b19cd-105">The input and output tensor must have the same *DimensionCount* and *Sizes*, although they may differ in *DataType*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b19cd-106">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="b19cd-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b19cd-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="b19cd-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b19cd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b19cd-108">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="b19cd-109">Member</span><span class="sxs-lookup"><span data-stu-id="b19cd-109">Members</span></span>

`InputTensor`

<span data-ttu-id="b19cd-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b19cd-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b19cd-111">Der Eingabetensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b19cd-111">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="b19cd-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b19cd-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b19cd-113">Der Ausgabe tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b19cd-113">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="b19cd-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b19cd-114">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0,   123], // 0b0000000000, 0b0001111011
 [456, 789]] // 0b0111001000, 0b1100010101

OutputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0, 6],
 [4, 5]]
```

## <a name="availability"></a><span data-ttu-id="b19cd-115">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="b19cd-115">Availability</span></span>
<span data-ttu-id="b19cd-116">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b19cd-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b19cd-117">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="b19cd-117">Tensor constraints</span></span>
<span data-ttu-id="b19cd-118">*InputTensor und* *OutputTensor* müssen über die gleichen *DimensionCount-* und *Sizes-Größen verfügen.*</span><span class="sxs-lookup"><span data-stu-id="b19cd-118">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b19cd-119">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="b19cd-119">Tensor support</span></span>
| <span data-ttu-id="b19cd-120">Tensor</span><span class="sxs-lookup"><span data-stu-id="b19cd-120">Tensor</span></span> | <span data-ttu-id="b19cd-121">Typ</span><span class="sxs-lookup"><span data-stu-id="b19cd-121">Kind</span></span> | <span data-ttu-id="b19cd-122">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="b19cd-122">Supported dimension counts</span></span> | <span data-ttu-id="b19cd-123">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="b19cd-123">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b19cd-124">InputTensor</span><span class="sxs-lookup"><span data-stu-id="b19cd-124">InputTensor</span></span> | <span data-ttu-id="b19cd-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b19cd-125">Input</span></span> | <span data-ttu-id="b19cd-126">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="b19cd-126">1 to 8</span></span> | <span data-ttu-id="b19cd-127">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b19cd-127">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b19cd-128">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b19cd-128">OutputTensor</span></span> | <span data-ttu-id="b19cd-129">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="b19cd-129">Output</span></span> | <span data-ttu-id="b19cd-130">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="b19cd-130">1 to 8</span></span> | <span data-ttu-id="b19cd-131">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="b19cd-131">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="b19cd-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b19cd-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b19cd-133">**Header**</span><span class="sxs-lookup"><span data-stu-id="b19cd-133">**Header**</span></span> | <span data-ttu-id="b19cd-134">directml.h</span><span class="sxs-lookup"><span data-stu-id="b19cd-134">directml.h</span></span> |