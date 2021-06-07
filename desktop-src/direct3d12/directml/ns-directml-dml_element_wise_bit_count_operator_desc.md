---
UID: NS:directml.DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
description: Berechnet das bitweise NOT für jedes Element des Eingabetensors und schreibt das Ergebnis in den Ausgabetensor.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.openlocfilehash: 070fc901c006ce1f18429e79eab635a5360c4af7
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417633"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a><span data-ttu-id="a38f8-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="a38f8-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a38f8-104">Berechnet das bitweise NOT für jedes Element des Eingabetensors und schreibt das Ergebnis in den Ausgabetensor.</span><span class="sxs-lookup"><span data-stu-id="a38f8-104">Computes the bitwise NOT for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="a38f8-105">Der Eingabe- und Ausgabe-Tensor muss denselben *DimensionCount-,* *Sizes-* und *DataType-Wert aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="a38f8-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="a38f8-106">Dieser Operator unterstützt die in-place-Ausführung, was bedeutet, dass der Ausgabetensor während der Bindung einen Alias für den Eingabetensor verwenden darf.</span><span class="sxs-lookup"><span data-stu-id="a38f8-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias the input tensor during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a38f8-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="a38f8-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a38f8-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="a38f8-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a38f8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a38f8-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="a38f8-110">Member</span><span class="sxs-lookup"><span data-stu-id="a38f8-110">Members</span></span>

`InputTensor`

<span data-ttu-id="a38f8-111">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a38f8-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a38f8-112">Der Eingabetensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a38f8-112">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="a38f8-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a38f8-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a38f8-114">Der Ausgabe tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a38f8-114">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="a38f8-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a38f8-115">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="a38f8-116">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="a38f8-116">Availability</span></span>
<span data-ttu-id="a38f8-117">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a38f8-117">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a38f8-118">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="a38f8-118">Tensor constraints</span></span>
<span data-ttu-id="a38f8-119">*InputTensor und* *OutputTensor* müssen denselben *DataType,* *DimensionCount* und *die gleichen Größen aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="a38f8-119">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a38f8-120">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a38f8-120">Tensor support</span></span>
| <span data-ttu-id="a38f8-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="a38f8-121">Tensor</span></span> | <span data-ttu-id="a38f8-122">Typ</span><span class="sxs-lookup"><span data-stu-id="a38f8-122">Kind</span></span> | <span data-ttu-id="a38f8-123">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="a38f8-123">Supported dimension counts</span></span> | <span data-ttu-id="a38f8-124">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="a38f8-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a38f8-125">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a38f8-125">InputTensor</span></span> | <span data-ttu-id="a38f8-126">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a38f8-126">Input</span></span> | <span data-ttu-id="a38f8-127">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a38f8-127">1 to 8</span></span> | <span data-ttu-id="a38f8-128">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a38f8-128">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a38f8-129">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a38f8-129">OutputTensor</span></span> | <span data-ttu-id="a38f8-130">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a38f8-130">Output</span></span> | <span data-ttu-id="a38f8-131">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a38f8-131">1 to 8</span></span> | <span data-ttu-id="a38f8-132">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a38f8-132">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="a38f8-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a38f8-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a38f8-134">**Header**</span><span class="sxs-lookup"><span data-stu-id="a38f8-134">**Header**</span></span> | <span data-ttu-id="a38f8-135">directml.h</span><span class="sxs-lookup"><span data-stu-id="a38f8-135">directml.h</span></span> |