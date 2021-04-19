---
UID: NS:directml.DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
description: Berechnet die bitweise auffüllungs Anzahl (die Anzahl der Bits, die auf 1 festgelegt ist) für jedes Element des Eingabe Mandanten und schreibt das Ergebnis in den Ausgabe Mandanten.
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
ms.openlocfilehash: 4b292b1b6e12f4643e928022f59603fd75e080fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106363874"
---
# <a name="dml_element_wise_bit_count_operator_desc-structure-directmlh"></a><span data-ttu-id="bccdd-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="bccdd-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="bccdd-104">Berechnet die bitweise auffüllungs Anzahl (die Anzahl der Bits, die auf 1 festgelegt ist) für jedes Element des Eingabe Mandanten und schreibt das Ergebnis in den Ausgabe Mandanten.</span><span class="sxs-lookup"><span data-stu-id="bccdd-104">Computes the bitwise population count (the number of bits set to 1) for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="bccdd-105">Der Eingabe-und der Ausgabe Mandanten müssen die gleiche *DimensionCount* und *Größe* aufweisen, auch wenn Sie sich in *DataType* unterscheiden können.</span><span class="sxs-lookup"><span data-stu-id="bccdd-105">The input and output tensor must have the same *DimensionCount* and *Sizes*, although they may differ in *DataType*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bccdd-106">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="bccdd-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="bccdd-107">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="bccdd-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bccdd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bccdd-108">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="bccdd-109">Member</span><span class="sxs-lookup"><span data-stu-id="bccdd-109">Members</span></span>

`InputTensor`

<span data-ttu-id="bccdd-110">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bccdd-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bccdd-111">Der eingabetensor, aus dem gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="bccdd-111">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="bccdd-112">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bccdd-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bccdd-113">Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bccdd-113">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="bccdd-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bccdd-114">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0,   123], // 0b0000000000, 0b0001111011
 [456, 789]] // 0b0111001000, 0b1100010101

OutputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0, 6],
 [4, 5]]
```

## <a name="availability"></a><span data-ttu-id="bccdd-115">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="bccdd-115">Availability</span></span>
<span data-ttu-id="bccdd-116">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="bccdd-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="bccdd-117">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="bccdd-117">Tensor constraints</span></span>
<span data-ttu-id="bccdd-118">*Inputtensor* und *outputtensor* müssen die gleiche *DimensionCount* und *Größe* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bccdd-118">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="bccdd-119">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="bccdd-119">Tensor support</span></span>
| <span data-ttu-id="bccdd-120">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="bccdd-120">Tensor</span></span> | <span data-ttu-id="bccdd-121">Typ</span><span class="sxs-lookup"><span data-stu-id="bccdd-121">Kind</span></span> | <span data-ttu-id="bccdd-122">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="bccdd-122">Supported dimension counts</span></span> | <span data-ttu-id="bccdd-123">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="bccdd-123">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bccdd-124">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="bccdd-124">InputTensor</span></span> | <span data-ttu-id="bccdd-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bccdd-125">Input</span></span> | <span data-ttu-id="bccdd-126">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="bccdd-126">1 to 8</span></span> | <span data-ttu-id="bccdd-127">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="bccdd-127">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bccdd-128">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="bccdd-128">OutputTensor</span></span> | <span data-ttu-id="bccdd-129">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="bccdd-129">Output</span></span> | <span data-ttu-id="bccdd-130">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="bccdd-130">1 to 8</span></span> | <span data-ttu-id="bccdd-131">UInt32, Uint8</span><span class="sxs-lookup"><span data-stu-id="bccdd-131">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="bccdd-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bccdd-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bccdd-133">**Header**</span><span class="sxs-lookup"><span data-stu-id="bccdd-133">**Header**</span></span> | <span data-ttu-id="bccdd-134">directml. h</span><span class="sxs-lookup"><span data-stu-id="bccdd-134">directml.h</span></span> |