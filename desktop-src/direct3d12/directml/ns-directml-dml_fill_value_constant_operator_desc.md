---
UID: NS:directml.DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
title: DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
description: Füllt einen Tensor mit dem angegebenen konstanten *Wert* aus.
helpviewer_keywords:
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure
- direct3d12.dml_fill_value_constant_operator_desc
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.openlocfilehash: 4fe9f766fc48a4b1ca0d32082dcd8a5f67591195
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803035"
---
# <a name="dml_fill_value_constant_operator_desc-structure-directmlh"></a><span data-ttu-id="c6e5c-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="c6e5c-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="c6e5c-104">Füllt einen Tensor mit dem angegebenen konstanten *Wert* aus.</span><span class="sxs-lookup"><span data-stu-id="c6e5c-104">Fills a tensor with the given constant *Value*.</span></span> <span data-ttu-id="c6e5c-105">Dieser Operator führt den folgenden Pseudocode aus.</span><span class="sxs-lookup"><span data-stu-id="c6e5c-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="c6e5c-106">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="c6e5c-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="c6e5c-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="c6e5c-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e5c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6e5c-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_CONSTANT_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      Value;
};
```



## <a name="members"></a><span data-ttu-id="c6e5c-109">Member</span><span class="sxs-lookup"><span data-stu-id="c6e5c-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="c6e5c-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c6e5c-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c6e5c-111">Der Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6e5c-111">The tensor to write the results to.</span></span> <span data-ttu-id="c6e5c-112">Dieser Tensor kann eine beliebige Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c6e5c-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="c6e5c-113">Typ: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="c6e5c-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="c6e5c-114">Der Datentyp des *Felds Wert,* der *mit OutputTensor.DataType* übereinstimmen muss.</span><span class="sxs-lookup"><span data-stu-id="c6e5c-114">The data type of the *Value* field, which must match *OutputTensor.DataType*.</span></span>


`Value`

<span data-ttu-id="c6e5c-115">Typ: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="c6e5c-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="c6e5c-116">Ein konstanter Wert zum Füllen der Ausgabe, wobei *ValueDataType* bestimmt, wie das Feld interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6e5c-116">A constant value to fill the output, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="c6e5c-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6e5c-117">Examples</span></span>

```
Value = 13.0

OutputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
    [[[[13.0f, 13.0f, 13.0f, 13.0f],
       [13.0f, 13.0f, 13.0f, 13.0f]]]]
```

## <a name="availability"></a><span data-ttu-id="c6e5c-118">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="c6e5c-118">Availability</span></span>
<span data-ttu-id="c6e5c-119">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c6e5c-119">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c6e5c-120">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="c6e5c-120">Tensor support</span></span>
| <span data-ttu-id="c6e5c-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="c6e5c-121">Tensor</span></span> | <span data-ttu-id="c6e5c-122">Typ</span><span class="sxs-lookup"><span data-stu-id="c6e5c-122">Kind</span></span> | <span data-ttu-id="c6e5c-123">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="c6e5c-123">Supported dimension counts</span></span> | <span data-ttu-id="c6e5c-124">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="c6e5c-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c6e5c-125">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c6e5c-125">OutputTensor</span></span> | <span data-ttu-id="c6e5c-126">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c6e5c-126">Output</span></span> | <span data-ttu-id="c6e5c-127">4</span><span class="sxs-lookup"><span data-stu-id="c6e5c-127">4</span></span> | <span data-ttu-id="c6e5c-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c6e5c-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="c6e5c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6e5c-129">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c6e5c-130">**Header**</span><span class="sxs-lookup"><span data-stu-id="c6e5c-130">**Header**</span></span> | <span data-ttu-id="c6e5c-131">directml.h</span><span class="sxs-lookup"><span data-stu-id="c6e5c-131">directml.h</span></span> |