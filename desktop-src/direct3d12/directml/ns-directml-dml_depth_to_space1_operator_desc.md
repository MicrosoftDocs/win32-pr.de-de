---
UID: NS:directml.DML_DEPTH_TO_SPACE1_OPERATOR_DESC
title: DML_DEPTH_TO_SPACE1_OPERATOR_DESC
description: Ordnet (permutes) Daten aus einer Tiefe in Blöcke räumlicher Daten an. Der-Operator gibt eine Kopie des Eingabe Mandanten aus, bei der Werte aus der tiefen Dimension in räumliche Blöcke in die Dimensionen Height und Width verschoben werden.
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
ms.openlocfilehash: 639bda0b8d398d24b01649635d3cfcbd2301a211
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106354264"
---
# <a name="dml_depth_to_space1_operator_desc-structure-directmlh"></a><span data-ttu-id="64351-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="64351-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="64351-105">Ordnet (permutes) Daten aus einer Tiefe in Blöcke räumlicher Daten an.</span><span class="sxs-lookup"><span data-stu-id="64351-105">Rearranges (permutes) data from depth into blocks of spatial data.</span></span> <span data-ttu-id="64351-106">Der-Operator gibt eine Kopie des Eingabe Mandanten aus, bei der Werte aus der tiefen Dimension in räumliche Blöcke in die Dimensionen Height und Width verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="64351-106">The operator outputs a copy of the input tensor where values from the depth dimension are moved in spatial blocks to the height and width dimensions.</span></span>

<span data-ttu-id="64351-107">Dies ist die umgekehrte Transformation von [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="64351-107">This is the inverse transformation of [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64351-108">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="64351-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="64351-109">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="64351-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="64351-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="64351-110">Syntax</span></span>
```cpp
struct DML_DEPTH_TO_SPACE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="64351-111">Member</span><span class="sxs-lookup"><span data-stu-id="64351-111">Members</span></span>

`InputTensor`

<span data-ttu-id="64351-112">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64351-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64351-113">Der zu lesende tensorflow.</span><span class="sxs-lookup"><span data-stu-id="64351-113">The tensor to read from.</span></span> <span data-ttu-id="64351-114">Die Dimensionen des eingabetensors sind `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="64351-114">The input tensor's dimensions are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`OutputTensor`

<span data-ttu-id="64351-115">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64351-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64351-116">Der tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64351-116">The tensor to write the results to.</span></span> <span data-ttu-id="64351-117">Die Dimensionen des Ausgabe Mandanten lauten `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` :</span><span class="sxs-lookup"><span data-stu-id="64351-117">The output tensor's dimensions are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`, where:</span></span>

* <span data-ttu-id="64351-118">Outputchannelcount wird als inputchannelcount/( `BlockSize`  \*  `BlockSize` ) berechnet.</span><span class="sxs-lookup"><span data-stu-id="64351-118">OutputChannelCount is computed as InputChannelCount / (`BlockSize` \* `BlockSize`)</span></span>
* <span data-ttu-id="64351-119">OutputHeight wird als inputheight berechnet \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="64351-119">OutputHeight is computed as InputHeight \* `BlockSize`</span></span>
* <span data-ttu-id="64351-120">OutputWidth wird als inputwidth berechnet \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="64351-120">OutputWidth is computed as InputWidth \* `BlockSize`</span></span>


`BlockSize`

<span data-ttu-id="64351-121">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="64351-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="64351-122">Die Breite und Höhe der Blöcke, die verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="64351-122">The width and height of the blocks that are moved.</span></span>


`Order`

<span data-ttu-id="64351-123">Typ: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="64351-123">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="64351-124">Siehe [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="64351-124">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="64351-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64351-125">Examples</span></span>

<span data-ttu-id="64351-126">In den Beispielen in diesem Abschnitt werden alle unten aufgeführten Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="64351-126">The examples in this section all use the input below.</span></span>

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

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="64351-127">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="64351-127">Example 1.</span></span> <span data-ttu-id="64351-128">Tiefen Spalten-Zeilen Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="64351-128">Depth-column-row order</span></span>

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

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="64351-129">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="64351-129">Example 2.</span></span> <span data-ttu-id="64351-130">Spalten zeilige Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="64351-130">Column-row-depth order</span></span>

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


## <a name="remarks"></a><span data-ttu-id="64351-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64351-131">Remarks</span></span>
<span data-ttu-id="64351-132">Wenn *Order* auf [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md)festgelegt ist, entspricht **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span><span class="sxs-lookup"><span data-stu-id="64351-132">When *Order* is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** is equivalent to [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span></span>

## <a name="availability"></a><span data-ttu-id="64351-133">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="64351-133">Availability</span></span>
<span data-ttu-id="64351-134">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="64351-134">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="64351-135">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="64351-135">Tensor constraints</span></span>
<span data-ttu-id="64351-136">*Inputtensor* und *outputtensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="64351-136">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="64351-137">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="64351-137">Tensor support</span></span>
| <span data-ttu-id="64351-138">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="64351-138">Tensor</span></span> | <span data-ttu-id="64351-139">Typ</span><span class="sxs-lookup"><span data-stu-id="64351-139">Kind</span></span> | <span data-ttu-id="64351-140">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="64351-140">Dimensions</span></span> | <span data-ttu-id="64351-141">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="64351-141">Supported dimension counts</span></span> | <span data-ttu-id="64351-142">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="64351-142">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="64351-143">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="64351-143">InputTensor</span></span> | <span data-ttu-id="64351-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64351-144">Input</span></span> | <span data-ttu-id="64351-145">{BatchCount, inputchannelcount, inputheight, inputwidth}</span><span class="sxs-lookup"><span data-stu-id="64351-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="64351-146">4</span><span class="sxs-lookup"><span data-stu-id="64351-146">4</span></span> | <span data-ttu-id="64351-147">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="64351-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="64351-148">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="64351-148">OutputTensor</span></span> | <span data-ttu-id="64351-149">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="64351-149">Output</span></span> | <span data-ttu-id="64351-150">{BatchCount, outputchannelcount, OutputHeight, OutputWidth}</span><span class="sxs-lookup"><span data-stu-id="64351-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="64351-151">4</span><span class="sxs-lookup"><span data-stu-id="64351-151">4</span></span> | <span data-ttu-id="64351-152">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="64351-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="64351-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64351-153">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="64351-154">**Header**</span><span class="sxs-lookup"><span data-stu-id="64351-154">**Header**</span></span> | <span data-ttu-id="64351-155">directml. h</span><span class="sxs-lookup"><span data-stu-id="64351-155">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="64351-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64351-156">See also</span></span>

* [<span data-ttu-id="64351-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="64351-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc)
* [<span data-ttu-id="64351-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="64351-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)