---
UID: NS:directml.DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
description: Berechnet das bitweise XOR (exklusiv or) zwischen jedem entsprechenden Element der Eingabe-Tensoren und schreibt das Ergebnis in den Ausgabe Mandanten.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.openlocfilehash: 73a811448b7c2b7839afd6e926acb0bf04a2ff44
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106362808"
---
# <a name="dml_element_wise_bit_xor_operator_desc-structure-directmlh"></a><span data-ttu-id="20373-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="20373-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="20373-104">Berechnet das bitweise XOR (exklusiv or) zwischen jedem entsprechenden Element der Eingabe-Tensoren und schreibt das Ergebnis in den Ausgabe Mandanten.</span><span class="sxs-lookup"><span data-stu-id="20373-104">Computes the bitwise XOR (eXclusive OR) between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="20373-105">Der Eingabe-und Ausgabe Mandanten muss dieselbe *DimensionCount*, *Größe* und denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="20373-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="20373-106">Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass der ausgabetensor bei der Bindung eine oder mehrere Eingabe-Tensoren als Alias zulässt.</span><span class="sxs-lookup"><span data-stu-id="20373-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20373-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="20373-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="20373-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="20373-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="20373-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="20373-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="20373-110">Member</span><span class="sxs-lookup"><span data-stu-id="20373-110">Members</span></span>

`ATensor`

<span data-ttu-id="20373-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="20373-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="20373-112">Ein tensorflow, der die Links neben Eingaben enthält.</span><span class="sxs-lookup"><span data-stu-id="20373-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="20373-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="20373-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="20373-114">Ein tensorflow, der die Eingaben auf der rechten Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="20373-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="20373-115">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="20373-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="20373-116">Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20373-116">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="20373-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="20373-117">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="20373-118">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="20373-118">Availability</span></span>
<span data-ttu-id="20373-119">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="20373-119">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="20373-120">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="20373-120">Tensor constraints</span></span>
<span data-ttu-id="20373-121">*Atensor*, *btensor* und *outputtensor* müssen denselben *Datentyp*, jede *DimensionCount* und jede *Größe* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="20373-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="20373-122">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="20373-122">Tensor support</span></span>
| <span data-ttu-id="20373-123">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="20373-123">Tensor</span></span> | <span data-ttu-id="20373-124">Typ</span><span class="sxs-lookup"><span data-stu-id="20373-124">Kind</span></span> | <span data-ttu-id="20373-125">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="20373-125">Supported dimension counts</span></span> | <span data-ttu-id="20373-126">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="20373-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="20373-127">Atensor</span><span class="sxs-lookup"><span data-stu-id="20373-127">ATensor</span></span> | <span data-ttu-id="20373-128">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20373-128">Input</span></span> | <span data-ttu-id="20373-129">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="20373-129">1 to 8</span></span> | <span data-ttu-id="20373-130">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="20373-130">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="20373-131">Btensor</span><span class="sxs-lookup"><span data-stu-id="20373-131">BTensor</span></span> | <span data-ttu-id="20373-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20373-132">Input</span></span> | <span data-ttu-id="20373-133">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="20373-133">1 to 8</span></span> | <span data-ttu-id="20373-134">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="20373-134">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="20373-135">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="20373-135">OutputTensor</span></span> | <span data-ttu-id="20373-136">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="20373-136">Output</span></span> | <span data-ttu-id="20373-137">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="20373-137">1 to 8</span></span> | <span data-ttu-id="20373-138">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="20373-138">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="20373-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20373-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="20373-140">**Header**</span><span class="sxs-lookup"><span data-stu-id="20373-140">**Header**</span></span> | <span data-ttu-id="20373-141">directml. h</span><span class="sxs-lookup"><span data-stu-id="20373-141">directml.h</span></span> |