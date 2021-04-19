---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Fasst die Elemente eines Mandanten auf einer Achse zusammen, wobei der laufende Zähler der Summierungs-in den Ausgabe Mandanten geschrieben wird.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106355095"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="933c5-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="933c5-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="933c5-104">Fasst die Elemente eines Mandanten auf einer Achse zusammen, wobei der laufende Zähler der Summierungs-in den Ausgabe Mandanten geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="933c5-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="933c5-105">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="933c5-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="933c5-106">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="933c5-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="933c5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="933c5-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a><span data-ttu-id="933c5-108">Member</span><span class="sxs-lookup"><span data-stu-id="933c5-108">Members</span></span>

`InputTensor`

<span data-ttu-id="933c5-109">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="933c5-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="933c5-110">Der eingabensor, der die zu summierenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="933c5-110">The input tensor containing elements to be summed.</span></span>


`OutputTensor`

<span data-ttu-id="933c5-111">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="933c5-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="933c5-112">Der Ausgabe Mandanten, in den die resultierenden kumulativen Summen geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="933c5-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="933c5-113">Dieser Mandanten muss dieselbe Größe und denselben Datentyp aufweisen wie der *inputtensor*.</span><span class="sxs-lookup"><span data-stu-id="933c5-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="933c5-114">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="933c5-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="933c5-115">Der Index der Dimension, über die Elemente zusammengefasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="933c5-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="933c5-116">Dieser Wert muss kleiner als die *DimensionCount* von " *inputtensor*" sein.</span><span class="sxs-lookup"><span data-stu-id="933c5-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`AxisDirection`

<span data-ttu-id="933c5-117">Typ: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="933c5-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="933c5-118">Einer der Werte der [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="933c5-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="933c5-119">Wenn der Wert auf **DML_AXIS_DIRECTION_INCREASING** festgelegt ist, erfolgt die Summe, indem der tensorflow entlang der angegebenen Achse durch den aufsteigenden Element Index durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="933c5-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="933c5-120">Wenn **DML_AXIS_DIRECTION_DECREASING** auf festgelegt ist, ist der umgekehrte Wert true, und die Summe erfolgt durch das Durchlaufen von Elementen nach absteigender Index.</span><span class="sxs-lookup"><span data-stu-id="933c5-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>


`HasExclusiveSum`




## <a name="remarks"></a><span data-ttu-id="933c5-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="933c5-121">Remarks</span></span>
<span data-ttu-id="933c5-122">Dieser Operator unterstützt die direkte Ausführung, d. h., der *outputtensor* ist berechtigt, den *inputtensor* während der Bindung zu Alias.</span><span class="sxs-lookup"><span data-stu-id="933c5-122">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="933c5-123">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="933c5-123">Availability</span></span>
<span data-ttu-id="933c5-124">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="933c5-124">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="933c5-125">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="933c5-125">Tensor constraints</span></span>
<span data-ttu-id="933c5-126">*Inputtensor* und *outputtensor* müssen über denselben *Datentyp* und dieselben *Größen* verfügen.</span><span class="sxs-lookup"><span data-stu-id="933c5-126">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="933c5-127">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="933c5-127">Tensor support</span></span>
| <span data-ttu-id="933c5-128">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="933c5-128">Tensor</span></span> | <span data-ttu-id="933c5-129">Typ</span><span class="sxs-lookup"><span data-stu-id="933c5-129">Kind</span></span> | <span data-ttu-id="933c5-130">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="933c5-130">Supported dimension counts</span></span> | <span data-ttu-id="933c5-131">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="933c5-131">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="933c5-132">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="933c5-132">InputTensor</span></span> | <span data-ttu-id="933c5-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="933c5-133">Input</span></span> | <span data-ttu-id="933c5-134">4</span><span class="sxs-lookup"><span data-stu-id="933c5-134">4</span></span> | <span data-ttu-id="933c5-135">Float32, FLOAT16, UInt32, UInt16</span><span class="sxs-lookup"><span data-stu-id="933c5-135">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="933c5-136">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="933c5-136">OutputTensor</span></span> | <span data-ttu-id="933c5-137">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="933c5-137">Output</span></span> | <span data-ttu-id="933c5-138">4</span><span class="sxs-lookup"><span data-stu-id="933c5-138">4</span></span> | <span data-ttu-id="933c5-139">Float32, FLOAT16, UInt32, UInt16</span><span class="sxs-lookup"><span data-stu-id="933c5-139">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="933c5-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="933c5-140">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="933c5-141">**Header**</span><span class="sxs-lookup"><span data-stu-id="933c5-141">**Header**</span></span> | <span data-ttu-id="933c5-142">directml. h</span><span class="sxs-lookup"><span data-stu-id="933c5-142">directml.h</span></span> |