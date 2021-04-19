---
UID: NS:directml.DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
title: DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
description: Füllt einen tensorflow mit dem angegebenen Konstanten *Wert*.
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
ms.openlocfilehash: d2b69f1f6b1c9768c24cab9a58bba3c3cadb04bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106362806"
---
# <a name="dml_fill_value_constant_operator_desc-structure-directmlh"></a><span data-ttu-id="8f772-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="8f772-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8f772-104">Füllt einen tensorflow mit dem angegebenen Konstanten *Wert*.</span><span class="sxs-lookup"><span data-stu-id="8f772-104">Fills a tensor with the given constant *Value*.</span></span> <span data-ttu-id="8f772-105">Dieser Operator führt den folgenden Pseudocode aus.</span><span class="sxs-lookup"><span data-stu-id="8f772-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="8f772-106">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="8f772-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="8f772-107">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8f772-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f772-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f772-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_CONSTANT_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      Value;
};
```



## <a name="members"></a><span data-ttu-id="8f772-109">Member</span><span class="sxs-lookup"><span data-stu-id="8f772-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="8f772-110">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8f772-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8f772-111">Der tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8f772-111">The tensor to write the results to.</span></span> <span data-ttu-id="8f772-112">Dieser Mandanten kann eine beliebige Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8f772-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="8f772-113">Typ: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="8f772-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="8f772-114">Der Datentyp des *Wertfelds* , das " *outputtensor. DataType*" entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="8f772-114">The data type of the *Value* field, which must match *OutputTensor.DataType*.</span></span>


`Value`

<span data-ttu-id="8f772-115">Typ: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="8f772-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="8f772-116">Ein konstanter Wert zum Auffüllen der Ausgabe mit *valuedatatype* , der bestimmt, wie das Feld interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f772-116">A constant value to fill the output, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="8f772-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f772-117">Examples</span></span>

```
Value = 13.0

OutputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
    [[[[13.0f, 13.0f, 13.0f, 13.0f],
       [13.0f, 13.0f, 13.0f, 13.0f]]]]
```

## <a name="availability"></a><span data-ttu-id="8f772-118">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="8f772-118">Availability</span></span>
<span data-ttu-id="8f772-119">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8f772-119">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8f772-120">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="8f772-120">Tensor support</span></span>
| <span data-ttu-id="8f772-121">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="8f772-121">Tensor</span></span> | <span data-ttu-id="8f772-122">Typ</span><span class="sxs-lookup"><span data-stu-id="8f772-122">Kind</span></span> | <span data-ttu-id="8f772-123">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="8f772-123">Supported dimension counts</span></span> | <span data-ttu-id="8f772-124">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="8f772-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8f772-125">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="8f772-125">OutputTensor</span></span> | <span data-ttu-id="8f772-126">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8f772-126">Output</span></span> | <span data-ttu-id="8f772-127">4</span><span class="sxs-lookup"><span data-stu-id="8f772-127">4</span></span> | <span data-ttu-id="8f772-128">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="8f772-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="8f772-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f772-129">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8f772-130">**Header**</span><span class="sxs-lookup"><span data-stu-id="8f772-130">**Header**</span></span> | <span data-ttu-id="8f772-131">directml. h</span><span class="sxs-lookup"><span data-stu-id="8f772-131">directml.h</span></span> |