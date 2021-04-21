---
UID: NS:directml.DML_SPACE_TO_DEPTH1_OPERATOR_DESC
title: DML_SPACE_TO_DEPTH1_OPERATOR_DESC
description: Ordnet Blöcke räumlicher Daten in die Tiefe neu an. Der -Operator gibt eine Kopie des Eingabe-Tensors aus, in dem Werte aus der Höhe und Breite in die Tiefendimension verschoben werden.
helpviewer_keywords:
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure
- direct3d12.dml_space_to_depth1_operator_desc
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
ms.openlocfilehash: 35e64d83fa6b8df42428869f72249e9846e50596
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802871"
---
# <a name="dml_space_to_depth1_operator_desc-structure-directmlh"></a><span data-ttu-id="dd1bf-104">DML_SPACE_TO_DEPTH1_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="dd1bf-104">DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="dd1bf-105">Ordnet Blöcke räumlicher Daten in die Tiefe neu an.</span><span class="sxs-lookup"><span data-stu-id="dd1bf-105">Rearranges blocks of spatial data into depth.</span></span> <span data-ttu-id="dd1bf-106">Der -Operator gibt eine Kopie des Eingabe-Tensors aus, in dem Werte aus der Höhe und Breite in die Tiefendimension verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="dd1bf-106">The operator outputs a copy of the input tensor where values from the height and width dimensions are moved to the depth dimension.</span></span>

<span data-ttu-id="dd1bf-107">Dies ist die umgekehrte Transformation von [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="dd1bf-107">This is the inverse transformation of [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd1bf-108">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="dd1bf-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="dd1bf-109">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="dd1bf-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1bf-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd1bf-110">Syntax</span></span>
```cpp
struct DML_SPACE_TO_DEPTH1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="dd1bf-111">Member</span><span class="sxs-lookup"><span data-stu-id="dd1bf-111">Members</span></span>

`InputTensor`

<span data-ttu-id="dd1bf-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dd1bf-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dd1bf-113">Der Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd1bf-113">The tensor to read from.</span></span> <span data-ttu-id="dd1bf-114">Die Dimensionen des Eingabe-Tensors sind `{ Batch, Channels, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="dd1bf-114">The input tensor's dimensions are `{ Batch, Channels, Height, Width }`.</span></span>


`OutputTensor`

<span data-ttu-id="dd1bf-115">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dd1bf-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dd1bf-116">Der Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd1bf-116">The tensor to write the results to.</span></span> <span data-ttu-id="dd1bf-117">Die Abmessungen des Ausgabe-Tensors sind `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }` .</span><span class="sxs-lookup"><span data-stu-id="dd1bf-117">The output tensor's dimensions are `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }`.</span></span>


`BlockSize`

<span data-ttu-id="dd1bf-118">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="dd1bf-118">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="dd1bf-119">Die Breite und Höhe der verschobenen Blöcke.</span><span class="sxs-lookup"><span data-stu-id="dd1bf-119">The width and height of the Blocks that are moved.</span></span>


`Order`

<span data-ttu-id="dd1bf-120">Typ: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="dd1bf-120">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="dd1bf-121">Weitere Informationen finden Sie [unter DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="dd1bf-121">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dd1bf-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd1bf-122">Examples</span></span>

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="dd1bf-123">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="dd1bf-123">Example 1.</span></span> <span data-ttu-id="dd1bf-124">Reihenfolge der Tiefenspaltenzeilen</span><span class="sxs-lookup"><span data-stu-id="dd1bf-124">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]

OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="dd1bf-125">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="dd1bf-125">Example 2.</span></span> <span data-ttu-id="dd1bf-126">Reihenfolge der Spaltenzeilentiefe</span><span class="sxs-lookup"><span data-stu-id="dd1bf-126">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```


## <a name="remarks"></a><span data-ttu-id="dd1bf-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd1bf-127">Remarks</span></span>
<span data-ttu-id="dd1bf-128">Wenn der *Order-Parameter* auf [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md)ist, entspricht dieser Operator [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="dd1bf-128">When the *Order* parameter is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), this operator is equivalent to [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="dd1bf-129">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="dd1bf-129">Availability</span></span>
<span data-ttu-id="dd1bf-130">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dd1bf-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="dd1bf-131">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="dd1bf-131">Tensor constraints</span></span>
<span data-ttu-id="dd1bf-132">*InputTensor und* *OutputTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="dd1bf-132">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="dd1bf-133">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="dd1bf-133">Tensor support</span></span>
| <span data-ttu-id="dd1bf-134">Tensor</span><span class="sxs-lookup"><span data-stu-id="dd1bf-134">Tensor</span></span> | <span data-ttu-id="dd1bf-135">Typ</span><span class="sxs-lookup"><span data-stu-id="dd1bf-135">Kind</span></span> | <span data-ttu-id="dd1bf-136">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="dd1bf-136">Dimensions</span></span> | <span data-ttu-id="dd1bf-137">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="dd1bf-137">Supported dimension counts</span></span> | <span data-ttu-id="dd1bf-138">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="dd1bf-138">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="dd1bf-139">InputTensor</span><span class="sxs-lookup"><span data-stu-id="dd1bf-139">InputTensor</span></span> | <span data-ttu-id="dd1bf-140">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dd1bf-140">Input</span></span> | <span data-ttu-id="dd1bf-141">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="dd1bf-141">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="dd1bf-142">4</span><span class="sxs-lookup"><span data-stu-id="dd1bf-142">4</span></span> | <span data-ttu-id="dd1bf-143">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="dd1bf-143">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="dd1bf-144">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="dd1bf-144">OutputTensor</span></span> | <span data-ttu-id="dd1bf-145">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="dd1bf-145">Output</span></span> | <span data-ttu-id="dd1bf-146">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="dd1bf-146">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="dd1bf-147">4</span><span class="sxs-lookup"><span data-stu-id="dd1bf-147">4</span></span> | <span data-ttu-id="dd1bf-148">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="dd1bf-148">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="dd1bf-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd1bf-149">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="dd1bf-150">**Header**</span><span class="sxs-lookup"><span data-stu-id="dd1bf-150">**Header**</span></span> | <span data-ttu-id="dd1bf-151">directml.h</span><span class="sxs-lookup"><span data-stu-id="dd1bf-151">directml.h</span></span> |