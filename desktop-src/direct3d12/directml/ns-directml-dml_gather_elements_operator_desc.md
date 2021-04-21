---
UID: NS:directml.DML_GATHER_ELEMENTS_OPERATOR_DESC
title: DML_GATHER_ELEMENTS_OPERATOR_DESC
description: Erfasst Elemente aus dem Eingabe-Tensor entlang der angegebenen Achse mithilfe des Index-Tensors, um die Eingabe neu zuzuordnen.
helpviewer_keywords:
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- DML_GATHER_ELEMENTS_OPERATOR_DESC structure
- direct3d12.dml_gather_elements_operator_desc
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.openlocfilehash: 89a4f2017f6adec8cce206e9261eb0fa6563e94c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803021"
---
# <a name="dml_gather_elements_operator_desc-structure-directmlh"></a><span data-ttu-id="a673d-103">DML_GATHER_ELEMENTS_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="a673d-103">DML_GATHER_ELEMENTS_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a673d-104">Erfasst Elemente aus dem Eingabe-Tensor entlang der angegebenen Achse mithilfe des Index-Tensors, um die Eingabe neu zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a673d-104">Gathers elements from the input tensor along the given axis using the indices tensor to remap into the input.</span></span> <span data-ttu-id="a673d-105">Dieser Operator führt den folgenden Pseudocode aus, wobei das genaue Verhalten von der Achse, der Anzahl der Eingabedimensionen und der Indexdimensionsanzahl abhängt.</span><span class="sxs-lookup"><span data-stu-id="a673d-105">This operator performs the following pseudocode, with the exact behavior dependent on the axis, input dimension count, and indices dimension count.</span></span>

```
output[i, j, k, ...] = input[index[i, j, k, ...], j, k, ...] // if axis == 0
output[i, j, k, ...] = input[i, index[i, j, k, ...], k, ...] // if axis == 1
output[i, j, k, ...] = input[i, j, index[i, j, k, ...], ...] // if axis == 2
...
```

> [!IMPORTANT]
> <span data-ttu-id="a673d-106">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="a673d-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a673d-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="a673d-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a673d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a673d-108">Syntax</span></span>
```cpp
struct DML_GATHER_ELEMENTS_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="a673d-109">Member</span><span class="sxs-lookup"><span data-stu-id="a673d-109">Members</span></span>

`InputTensor`

<span data-ttu-id="a673d-110">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a673d-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a673d-111">Der Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a673d-111">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="a673d-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a673d-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a673d-113">Die Indizes in den Eingabe-Tensor entlang der aktiven Achse.</span><span class="sxs-lookup"><span data-stu-id="a673d-113">The indices into the input tensor along the active axis.</span></span> <span data-ttu-id="a673d-114">Die *Größen* müssen mit *InputTensor.Sizes* für jede Dimension mit Ausnahme *von Achse* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a673d-114">The *Sizes* must match *InputTensor.Sizes* for every dimension except *Axis*.</span></span>

<span data-ttu-id="a673d-115">Ab `DML_FEATURE_LEVEL_3_0` unterstützt dieser Operator negative Indexwerte, wenn ein ganzzahligen Typ mit Vorzeichen mit diesem Tensor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a673d-115">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="a673d-116">Negative Indizes werden als relativ zum Ende der Achsendimension interpretiert.</span><span class="sxs-lookup"><span data-stu-id="a673d-116">Negative indices are interpreted as being relative to the end of the axis dimension.</span></span> <span data-ttu-id="a673d-117">Beispielsweise bezieht sich ein Index von -1 auf das letzte Element entlang dieser Dimension.</span><span class="sxs-lookup"><span data-stu-id="a673d-117">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="a673d-118">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a673d-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a673d-119">Der Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a673d-119">The tensor to write the results to.</span></span> <span data-ttu-id="a673d-120">Die *Größen* müssen *mit IndizesTensor.Sizes* übereinstimmen, und *DataType* muss mit *InputTensor.DataType* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a673d-120">The *Sizes* must match *IndicesTensor.Sizes*, and *DataType* must match *InputTensor.DataType*.</span></span>


`Axis`

<span data-ttu-id="a673d-121">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a673d-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="a673d-122">Die Achsendimension von *InputTensor,* die mit erfasst werden soll, im Bereich `[0, *InputTensor.DimensionCount*)` von .</span><span class="sxs-lookup"><span data-stu-id="a673d-122">The axis dimension of *InputTensor* to gather along, ranging `[0, *InputTensor.DimensionCount*)`.</span></span>

## <a name="examples"></a><span data-ttu-id="a673d-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a673d-123">Examples</span></span>

```
Axis = 0

InputTensor: (Sizes:{3,3}, DataType:FLOAT32)
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]

IndicesTensor: (Sizes:{2,3}, DataType:UINT32)
    [[1, 2, 0],
     [2, 0, 0]]

// output[y, x] = input[indices[y, x], x]
OutputTensor: (Sizes:{2,3}, DataType:UINT32)
    [[4, 8, 3], // select elements vertically from data
     [7, 2, 3]]
```

## <a name="availability"></a><span data-ttu-id="a673d-124">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="a673d-124">Availability</span></span>
<span data-ttu-id="a673d-125">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a673d-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a673d-126">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="a673d-126">Tensor constraints</span></span>
* <span data-ttu-id="a673d-127">`IndicesTensor`, *InputTensor* und *OutputTensor* müssen denselben *DimensionCount aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="a673d-127">`IndicesTensor`, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="a673d-128">*InputTensor und* *OutputTensor* müssen denselben *Datentyp haben.*</span><span class="sxs-lookup"><span data-stu-id="a673d-128">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a673d-129">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a673d-129">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="a673d-130">DML_FEATURE_LEVEL_3_0 und höher</span><span class="sxs-lookup"><span data-stu-id="a673d-130">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="a673d-131">Tensor</span><span class="sxs-lookup"><span data-stu-id="a673d-131">Tensor</span></span> | <span data-ttu-id="a673d-132">Typ</span><span class="sxs-lookup"><span data-stu-id="a673d-132">Kind</span></span> | <span data-ttu-id="a673d-133">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="a673d-133">Supported dimension counts</span></span> | <span data-ttu-id="a673d-134">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="a673d-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a673d-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a673d-135">InputTensor</span></span> | <span data-ttu-id="a673d-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a673d-136">Input</span></span> | <span data-ttu-id="a673d-137">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a673d-137">1 to 8</span></span> | <span data-ttu-id="a673d-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a673d-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a673d-139">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="a673d-139">IndicesTensor</span></span> | <span data-ttu-id="a673d-140">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a673d-140">Input</span></span> | <span data-ttu-id="a673d-141">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a673d-141">1 to 8</span></span> | <span data-ttu-id="a673d-142">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="a673d-142">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="a673d-143">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a673d-143">OutputTensor</span></span> | <span data-ttu-id="a673d-144">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a673d-144">Output</span></span> | <span data-ttu-id="a673d-145">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="a673d-145">1 to 8</span></span> | <span data-ttu-id="a673d-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a673d-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="a673d-147">DML_FEATURE_LEVEL_2_1 und höher</span><span class="sxs-lookup"><span data-stu-id="a673d-147">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="a673d-148">Tensor</span><span class="sxs-lookup"><span data-stu-id="a673d-148">Tensor</span></span> | <span data-ttu-id="a673d-149">Typ</span><span class="sxs-lookup"><span data-stu-id="a673d-149">Kind</span></span> | <span data-ttu-id="a673d-150">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="a673d-150">Supported dimension counts</span></span> | <span data-ttu-id="a673d-151">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="a673d-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a673d-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a673d-152">InputTensor</span></span> | <span data-ttu-id="a673d-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a673d-153">Input</span></span> | <span data-ttu-id="a673d-154">4</span><span class="sxs-lookup"><span data-stu-id="a673d-154">4</span></span> | <span data-ttu-id="a673d-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a673d-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a673d-156">IndizesTensor</span><span class="sxs-lookup"><span data-stu-id="a673d-156">IndicesTensor</span></span> | <span data-ttu-id="a673d-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a673d-157">Input</span></span> | <span data-ttu-id="a673d-158">4</span><span class="sxs-lookup"><span data-stu-id="a673d-158">4</span></span> | <span data-ttu-id="a673d-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="a673d-159">UINT32</span></span> |
| <span data-ttu-id="a673d-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a673d-160">OutputTensor</span></span> | <span data-ttu-id="a673d-161">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a673d-161">Output</span></span> | <span data-ttu-id="a673d-162">4</span><span class="sxs-lookup"><span data-stu-id="a673d-162">4</span></span> | <span data-ttu-id="a673d-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a673d-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="a673d-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a673d-164">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a673d-165">**Header**</span><span class="sxs-lookup"><span data-stu-id="a673d-165">**Header**</span></span> | <span data-ttu-id="a673d-166">directml.h</span><span class="sxs-lookup"><span data-stu-id="a673d-166">directml.h</span></span> |