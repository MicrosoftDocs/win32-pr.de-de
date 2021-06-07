---
UID: NS:directml.DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
description: Berechnet die bitweise Auffüllungsanzahl (die Anzahl der Bits, die auf 1 festgelegt sind) für jedes Element des Eingabe-Tensors und schreibt das Ergebnis in den Ausgabe-Tensor.
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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417703"
---
# <a name="dml_element_wise_bit_count_operator_desc-structure-directmlh"></a><span data-ttu-id="bba19-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="bba19-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="bba19-104">Berechnet die bitweise Auffüllungsanzahl (die Anzahl der Bits, die auf 1 festgelegt sind) für jedes Element des Eingabe-Tensors und schreibt das Ergebnis in den Ausgabe-Tensor.</span><span class="sxs-lookup"><span data-stu-id="bba19-104">Computes the bitwise population count (the number of bits set to 1) for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="bba19-105">Der Eingabe- und Ausgabe-Tensor muss über die gleichen *DimensionCount-* und *Größen* verfügen, obwohl sie sich in *DataType* unterscheiden können.</span><span class="sxs-lookup"><span data-stu-id="bba19-105">The input and output tensor must have the same *DimensionCount* and *Sizes*, although they may differ in *DataType*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bba19-106">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="bba19-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="bba19-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="bba19-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bba19-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bba19-108">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="bba19-109">Member</span><span class="sxs-lookup"><span data-stu-id="bba19-109">Members</span></span>

`InputTensor`

<span data-ttu-id="bba19-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bba19-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bba19-111">Der Eingabe-Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bba19-111">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="bba19-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bba19-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bba19-113">Der Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bba19-113">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="bba19-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bba19-114">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0,   123], // 0b0000000000, 0b0001111011
 [456, 789]] // 0b0111001000, 0b1100010101

OutputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0, 6],
 [4, 5]]
```

## <a name="availability"></a><span data-ttu-id="bba19-115">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="bba19-115">Availability</span></span>
<span data-ttu-id="bba19-116">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bba19-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="bba19-117">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="bba19-117">Tensor constraints</span></span>
<span data-ttu-id="bba19-118">*InputTensor* und *OutputTensor* müssen über die gleichen *DimensionCount-* und *Größen verfügen.*</span><span class="sxs-lookup"><span data-stu-id="bba19-118">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="bba19-119">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="bba19-119">Tensor support</span></span>
| <span data-ttu-id="bba19-120">Tensor</span><span class="sxs-lookup"><span data-stu-id="bba19-120">Tensor</span></span> | <span data-ttu-id="bba19-121">Typ</span><span class="sxs-lookup"><span data-stu-id="bba19-121">Kind</span></span> | <span data-ttu-id="bba19-122">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="bba19-122">Supported dimension counts</span></span> | <span data-ttu-id="bba19-123">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="bba19-123">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bba19-124">InputTensor</span><span class="sxs-lookup"><span data-stu-id="bba19-124">InputTensor</span></span> | <span data-ttu-id="bba19-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bba19-125">Input</span></span> | <span data-ttu-id="bba19-126">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="bba19-126">1 to 8</span></span> | <span data-ttu-id="bba19-127">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bba19-127">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bba19-128">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="bba19-128">OutputTensor</span></span> | <span data-ttu-id="bba19-129">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="bba19-129">Output</span></span> | <span data-ttu-id="bba19-130">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="bba19-130">1 to 8</span></span> | <span data-ttu-id="bba19-131">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="bba19-131">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="bba19-132">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bba19-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bba19-133">**Header**</span><span class="sxs-lookup"><span data-stu-id="bba19-133">**Header**</span></span> | <span data-ttu-id="bba19-134">directml.h</span><span class="sxs-lookup"><span data-stu-id="bba19-134">directml.h</span></span> |