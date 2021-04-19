---
UID: NS:directml.DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
description: Berechnet das bitweise NOT für jedes Element des Eingabe Mandanten und schreibt das Ergebnis in den Ausgabe Mandanten.
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
ms.openlocfilehash: bb42be1e1f00fcf749ed271d55a7958b43464f1a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106353247"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a><span data-ttu-id="e4f36-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="e4f36-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e4f36-104">Berechnet das bitweise NOT für jedes Element des Eingabe Mandanten und schreibt das Ergebnis in den Ausgabe Mandanten.</span><span class="sxs-lookup"><span data-stu-id="e4f36-104">Computes the bitwise NOT for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="e4f36-105">Der Eingabe-und Ausgabe Mandanten muss dieselbe *DimensionCount*, *Größe* und denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e4f36-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="e4f36-106">Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass der ausgabetensor während der Bindung den Eingabe Mandanten als Alias zulässt.</span><span class="sxs-lookup"><span data-stu-id="e4f36-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias the input tensor during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4f36-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="e4f36-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e4f36-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e4f36-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f36-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4f36-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="e4f36-110">Member</span><span class="sxs-lookup"><span data-stu-id="e4f36-110">Members</span></span>

`InputTensor`

<span data-ttu-id="e4f36-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e4f36-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e4f36-112">Der eingabetensor, aus dem gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="e4f36-112">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="e4f36-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e4f36-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e4f36-114">Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4f36-114">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="e4f36-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e4f36-115">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="e4f36-116">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="e4f36-116">Availability</span></span>
<span data-ttu-id="e4f36-117">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="e4f36-117">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e4f36-118">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="e4f36-118">Tensor constraints</span></span>
<span data-ttu-id="e4f36-119">*Inputtensor* und *outputtensor* müssen denselben *Datentyp*, jede *DimensionCount* und jede *Größe* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e4f36-119">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e4f36-120">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="e4f36-120">Tensor support</span></span>
| <span data-ttu-id="e4f36-121">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="e4f36-121">Tensor</span></span> | <span data-ttu-id="e4f36-122">Typ</span><span class="sxs-lookup"><span data-stu-id="e4f36-122">Kind</span></span> | <span data-ttu-id="e4f36-123">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="e4f36-123">Supported dimension counts</span></span> | <span data-ttu-id="e4f36-124">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="e4f36-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e4f36-125">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="e4f36-125">InputTensor</span></span> | <span data-ttu-id="e4f36-126">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e4f36-126">Input</span></span> | <span data-ttu-id="e4f36-127">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="e4f36-127">1 to 8</span></span> | <span data-ttu-id="e4f36-128">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="e4f36-128">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e4f36-129">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="e4f36-129">OutputTensor</span></span> | <span data-ttu-id="e4f36-130">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e4f36-130">Output</span></span> | <span data-ttu-id="e4f36-131">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="e4f36-131">1 to 8</span></span> | <span data-ttu-id="e4f36-132">UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="e4f36-132">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="e4f36-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4f36-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e4f36-134">**Header**</span><span class="sxs-lookup"><span data-stu-id="e4f36-134">**Header**</span></span> | <span data-ttu-id="e4f36-135">directml. h</span><span class="sxs-lookup"><span data-stu-id="e4f36-135">directml.h</span></span> |