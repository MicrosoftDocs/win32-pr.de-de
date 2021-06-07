---
UID: NS:directml.DML_DEPTH_TO_SPACE1_OPERATOR_DESC
title: DML_DEPTH_TO_SPACE1_OPERATOR_DESC
description: Ordnet (permutiert) Daten aus der Tiefe in Blöcke räumlicher Daten neu. Der Operator gibt eine Kopie des Eingabe-Tensors aus, bei dem Werte aus der Tiefendimension in räumliche Blöcke in die Höhe und Breite verschoben werden.
helpviewer_keywords:
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure
- direct3d12.dml_depth_to_space1_operator_desc
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.openlocfilehash: 89b62a9916ee77dd6907d01710624d6e9a40a20a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417863"
---
# <a name="dml_depth_to_space1_operator_desc-structure-directmlh"></a><span data-ttu-id="c4a49-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="c4a49-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="c4a49-105">Ordnet (permutiert) Daten aus der Tiefe in Blöcke räumlicher Daten neu.</span><span class="sxs-lookup"><span data-stu-id="c4a49-105">Rearranges (permutes) data from depth into blocks of spatial data.</span></span> <span data-ttu-id="c4a49-106">Der Operator gibt eine Kopie des Eingabe-Tensors aus, bei dem Werte aus der Tiefendimension in räumliche Blöcke in die Höhe und Breite verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="c4a49-106">The operator outputs a copy of the input tensor where values from the depth dimension are moved in spatial blocks to the height and width dimensions.</span></span>

<span data-ttu-id="c4a49-107">Dies ist die umgekehrte Transformation von [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="c4a49-107">This is the inverse transformation of [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4a49-108">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="c4a49-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="c4a49-109">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="c4a49-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a49-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4a49-110">Syntax</span></span>
```cpp
struct DML_DEPTH_TO_SPACE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="c4a49-111">Member</span><span class="sxs-lookup"><span data-stu-id="c4a49-111">Members</span></span>

`InputTensor`

<span data-ttu-id="c4a49-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c4a49-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c4a49-113">Der Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4a49-113">The tensor to read from.</span></span> <span data-ttu-id="c4a49-114">Die Dimensionen des Eingabe-Tensors sind `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="c4a49-114">The input tensor's dimensions are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`OutputTensor`

<span data-ttu-id="c4a49-115">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c4a49-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c4a49-116">Der Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c4a49-116">The tensor to write the results to.</span></span> <span data-ttu-id="c4a49-117">Die Dimensionen des Ausgabe-Tensors sind `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` , wobei:</span><span class="sxs-lookup"><span data-stu-id="c4a49-117">The output tensor's dimensions are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`, where:</span></span>

* <span data-ttu-id="c4a49-118">OutputChannelCount wird als InputChannelCount /( ) berechnet. `BlockSize`  \*  `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="c4a49-118">OutputChannelCount is computed as InputChannelCount / (`BlockSize` \* `BlockSize`)</span></span>
* <span data-ttu-id="c4a49-119">OutputHeight wird als InputHeight \* berechnet. `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="c4a49-119">OutputHeight is computed as InputHeight \* `BlockSize`</span></span>
* <span data-ttu-id="c4a49-120">OutputWidth wird als InputWidth \* berechnet. `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="c4a49-120">OutputWidth is computed as InputWidth \* `BlockSize`</span></span>


`BlockSize`

<span data-ttu-id="c4a49-121">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c4a49-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c4a49-122">Die Breite und Höhe der Blöcke, die verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="c4a49-122">The width and height of the blocks that are moved.</span></span>


`Order`

<span data-ttu-id="c4a49-123">Typ: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="c4a49-123">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="c4a49-124">Weitere Informationen finden Sie [unter DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="c4a49-124">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c4a49-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4a49-125">Examples</span></span>

<span data-ttu-id="c4a49-126">In den Beispielen in diesem Abschnitt wird die folgende Eingabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4a49-126">The examples in this section all use the input below.</span></span>

```
InputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
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

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="c4a49-127">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="c4a49-127">Example 1.</span></span> <span data-ttu-id="c4a49-128">Reihenfolge der Tiefenspaltenzeilen</span><span class="sxs-lookup"><span data-stu-id="c4a49-128">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="c4a49-129">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="c4a49-129">Example 2.</span></span> <span data-ttu-id="c4a49-130">Reihenfolge der Spaltenzeilentiefe</span><span class="sxs-lookup"><span data-stu-id="c4a49-130">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
```


## <a name="remarks"></a><span data-ttu-id="c4a49-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4a49-131">Remarks</span></span>
<span data-ttu-id="c4a49-132">Wenn *Order* auf [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md)festgelegt **ist,** entspricht DML_DEPTH_TO_SPACE1_OPERATOR_DESC [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span><span class="sxs-lookup"><span data-stu-id="c4a49-132">When *Order* is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** is equivalent to [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span></span>

## <a name="availability"></a><span data-ttu-id="c4a49-133">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="c4a49-133">Availability</span></span>
<span data-ttu-id="c4a49-134">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c4a49-134">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c4a49-135">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="c4a49-135">Tensor constraints</span></span>
<span data-ttu-id="c4a49-136">*InputTensor* und *OutputTensor* müssen den gleichen *Datentyp aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="c4a49-136">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c4a49-137">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="c4a49-137">Tensor support</span></span>
| <span data-ttu-id="c4a49-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="c4a49-138">Tensor</span></span> | <span data-ttu-id="c4a49-139">Typ</span><span class="sxs-lookup"><span data-stu-id="c4a49-139">Kind</span></span> | <span data-ttu-id="c4a49-140">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="c4a49-140">Dimensions</span></span> | <span data-ttu-id="c4a49-141">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="c4a49-141">Supported dimension counts</span></span> | <span data-ttu-id="c4a49-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="c4a49-142">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="c4a49-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c4a49-143">InputTensor</span></span> | <span data-ttu-id="c4a49-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4a49-144">Input</span></span> | <span data-ttu-id="c4a49-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="c4a49-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="c4a49-146">4</span><span class="sxs-lookup"><span data-stu-id="c4a49-146">4</span></span> | <span data-ttu-id="c4a49-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c4a49-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c4a49-148">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c4a49-148">OutputTensor</span></span> | <span data-ttu-id="c4a49-149">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c4a49-149">Output</span></span> | <span data-ttu-id="c4a49-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="c4a49-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="c4a49-151">4</span><span class="sxs-lookup"><span data-stu-id="c4a49-151">4</span></span> | <span data-ttu-id="c4a49-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c4a49-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="c4a49-153">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c4a49-153">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c4a49-154">**Header**</span><span class="sxs-lookup"><span data-stu-id="c4a49-154">**Header**</span></span> | <span data-ttu-id="c4a49-155">directml.h</span><span class="sxs-lookup"><span data-stu-id="c4a49-155">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="c4a49-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4a49-156">See also</span></span>

* [<span data-ttu-id="c4a49-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="c4a49-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc)
* [<span data-ttu-id="c4a49-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="c4a49-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)