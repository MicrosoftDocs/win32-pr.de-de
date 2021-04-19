---
UID: NS:directml.DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
title: DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
description: Füllt einen tensorflow mit einer Sequenz.
helpviewer_keywords:
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure
- direct3d12.dml_fill_value_sequence_operator_desc
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
ms.openlocfilehash: ec356568c0860d330234cd990e8cf42ff4ccd120
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106357139"
---
# <a name="dml_fill_value_sequence_operator_desc-structure-directmlh"></a><span data-ttu-id="fe79b-103">DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="fe79b-103">DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="fe79b-104">Füllt einen tensorflow mit einer Sequenz.</span><span class="sxs-lookup"><span data-stu-id="fe79b-104">Fills a tensor with a sequence.</span></span> <span data-ttu-id="fe79b-105">Dieser Operator führt den folgenden Pseudocode aus.</span><span class="sxs-lookup"><span data-stu-id="fe79b-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
    Value += Delta
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="fe79b-106">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="fe79b-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="fe79b-107">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fe79b-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe79b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe79b-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      ValueStart;
  DML_SCALAR_UNION      ValueDelta;
};
```



## <a name="members"></a><span data-ttu-id="fe79b-109">Member</span><span class="sxs-lookup"><span data-stu-id="fe79b-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="fe79b-110">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe79b-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe79b-111">Der tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fe79b-111">The tensor to write the results to.</span></span> <span data-ttu-id="fe79b-112">Dieser Mandanten kann eine beliebige Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fe79b-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="fe79b-113">Typ: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="fe79b-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="fe79b-114">Der Datentyp des *Wertfelds* , das " *outputtensor. DataType*" entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="fe79b-114">The data type of *Value* field, which must match *OutputTensor.DataType*.</span></span>


`ValueStart`

<span data-ttu-id="fe79b-115">Typ: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="fe79b-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="fe79b-116">Der Anfangswert zum Auffüllen des ersten Elements in der Ausgabe mit *valuedatatype* , das festlegt, wie das Feld interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe79b-116">The initial value to fill the first element in the output, with *ValueDataType* determining how to interpret the field.</span></span>


`ValueDelta`

<span data-ttu-id="fe79b-117">Typ: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="fe79b-117">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="fe79b-118">Ein Schritt, der dem Wert für jedes geschriebene Element hinzugefügt werden soll, wobei *valuedatatype* festlegt, wie das Feld interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe79b-118">A step to add to the value for each element written, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="fe79b-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe79b-119">Examples</span></span>

### <a name="example-1-1d-ascending-step"></a><span data-ttu-id="fe79b-120">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="fe79b-120">Example 1.</span></span> <span data-ttu-id="fe79b-121">1D aufsteigender Schritt</span><span class="sxs-lookup"><span data-stu-id="fe79b-121">1D ascending step</span></span>

```
ValueStart = 3
ValueDelta = 2
ValueDataType = DML_TENSOR_DATA_TYPE_FLOAT32

OutputTensor: (Sizes:{1,1,1,3}, DataType:FLOAT32)
    [[[[3, 5, 7]]]]
```

### <a name="example-2-2d-ascending-step"></a><span data-ttu-id="fe79b-122">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="fe79b-122">Example 2.</span></span> <span data-ttu-id="fe79b-123">2D-aufsteigender Schritt</span><span class="sxs-lookup"><span data-stu-id="fe79b-123">2D ascending step</span></span>

```
ValueStart = 10
ValueDelta = -2
ValueDataType = DML_TENSOR_DATA_TYPE_UINT8

OutputTensor: (Sizes:{1,1,2,2}, DataType:UINT8)
    [[[[10, 8],
       [ 6, 4]]]]
```

## <a name="availability"></a><span data-ttu-id="fe79b-124">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="fe79b-124">Availability</span></span>
<span data-ttu-id="fe79b-125">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="fe79b-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fe79b-126">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="fe79b-126">Tensor support</span></span>
| <span data-ttu-id="fe79b-127">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="fe79b-127">Tensor</span></span> | <span data-ttu-id="fe79b-128">Typ</span><span class="sxs-lookup"><span data-stu-id="fe79b-128">Kind</span></span> | <span data-ttu-id="fe79b-129">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="fe79b-129">Supported dimension counts</span></span> | <span data-ttu-id="fe79b-130">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="fe79b-130">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fe79b-131">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="fe79b-131">OutputTensor</span></span> | <span data-ttu-id="fe79b-132">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fe79b-132">Output</span></span> | <span data-ttu-id="fe79b-133">4</span><span class="sxs-lookup"><span data-stu-id="fe79b-133">4</span></span> | <span data-ttu-id="fe79b-134">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="fe79b-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="fe79b-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe79b-135">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fe79b-136">**Header**</span><span class="sxs-lookup"><span data-stu-id="fe79b-136">**Header**</span></span> | <span data-ttu-id="fe79b-137">directml. h</span><span class="sxs-lookup"><span data-stu-id="fe79b-137">directml.h</span></span> |