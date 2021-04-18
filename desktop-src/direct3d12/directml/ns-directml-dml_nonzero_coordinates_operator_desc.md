---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Berechnet die N-dimensionalen Koordinaten aller Elemente ungleich 0 (null) des eingabetensors.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: a662ac3b341c07e512e11dcc15cbc9b11ec5f405
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106354896"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a><span data-ttu-id="0ae32-103">DML_NONZERO_COORDINATES_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="0ae32-103">DML_NONZERO_COORDINATES_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="0ae32-104">Berechnet die N-dimensionalen Koordinaten aller Elemente ungleich 0 (null) des eingabetensors.</span><span class="sxs-lookup"><span data-stu-id="0ae32-104">Computes the N-dimensional coordinates of all non-zero elements of the input tensor.</span></span>

<span data-ttu-id="0ae32-105">Dieser Operator erzeugt eine MXN-Matrix mit Werten, wobei jede Zeile M eine N-dimensionale Koordinate eines Werts ungleich 0 (null) aus der Eingabe enthält.</span><span class="sxs-lookup"><span data-stu-id="0ae32-105">This operator produces an MxN matrix of values, where each row M contains an N-dimensional coordinate of a non-zero value from the input.</span></span> <span data-ttu-id="0ae32-106">Bei Verwendung von **float32** -oder **FLOAT16** -Eingaben werden sowohl negative als auch positive 0 (0,0 f und-0,0 f) für die Zwecke dieses Operators als 0 (null) behandelt.</span><span class="sxs-lookup"><span data-stu-id="0ae32-106">When using **FLOAT32** or **FLOAT16** inputs, both negative and positive 0 (0.0f and -0.0f) are treated as zero for the purposes of this operator.</span></span>

<span data-ttu-id="0ae32-107">Der Operator erfordert, dass der *outputcoordinatestensor* eine Größe hat, die groß genug ist, um einem Worst-Case-Szenario Rechnung zu tragen, bei dem jedes Element der Eingabe ungleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="0ae32-107">The operator requires that the *OutputCoordinatesTensor* has a size large enough to accommodate a worst-case scenario where every element of the input is non-zero.</span></span> <span data-ttu-id="0ae32-108">Dieser Operator gibt die Anzahl von Elementen ungleich 0 (null) über den *outputzählensor* zurück, die Aufrufer überprüfen können, um die Anzahl der Koordinaten zu ermitteln, die in *outputcoordinatestensor* geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0ae32-108">This operator returns the count of of non-zero elements via the *OutputCountTensor*, which callers can inspect to determine the number of coordinates written to the *OutputCoordinatesTensor*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0ae32-109">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="0ae32-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="0ae32-110">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="0ae32-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ae32-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ae32-111">Syntax</span></span>

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a><span data-ttu-id="0ae32-112">Member</span><span class="sxs-lookup"><span data-stu-id="0ae32-112">Members</span></span>

`InputTensor`

<span data-ttu-id="0ae32-113">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0ae32-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0ae32-114">Ein eingabetensor.</span><span class="sxs-lookup"><span data-stu-id="0ae32-114">An input tensor.</span></span>

`OutputCountTensor`

<span data-ttu-id="0ae32-115">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0ae32-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0ae32-116">Ein Ausgabe Mandanten, der die Anzahl der Elemente ungleich 0 (null) im Eingabe Mandanten enthält.</span><span class="sxs-lookup"><span data-stu-id="0ae32-116">An output tensor that holds the count of non-zero elements in the input tensor.</span></span> <span data-ttu-id="0ae32-117">Dieser Mandanten muss ein Skalar sein, d &mdash; . h. die Größe dieses Mandanten muss 1 sein.</span><span class="sxs-lookup"><span data-stu-id="0ae32-117">This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1.</span></span> <span data-ttu-id="0ae32-118">Der Typ dieses Mandanten muss **UInt32** lauten.</span><span class="sxs-lookup"><span data-stu-id="0ae32-118">The type of this tensor must be **UINT32**.</span></span>

`OutputCoordinatesTensor`

<span data-ttu-id="0ae32-119">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0ae32-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0ae32-120">Ein Ausgabe-tensorflow, der die N-dimensionalen Koordinaten der Eingabeelemente enthält, die ungleich 0 (null) sind.</span><span class="sxs-lookup"><span data-stu-id="0ae32-120">An output tensor that holds the N-dimensional coordinates of the input elements which are non-zero.</span></span> 

<span data-ttu-id="0ae32-121">Dieser tensorflow muss über *Größen* von `{1,1,M,N}` verfügen ( *Wenn DimensionCount* gleich 4 ist), oder `{1,1,1,M,N}` (wenn *DimensionCount* gleich 5 ist), wobei M die Gesamtzahl der Elemente in *inputtensor* ist, und N größer oder gleich dem *effektiven Rang* von *inputtensor* ist, bis zur *DimensionCount* der Eingabe.</span><span class="sxs-lookup"><span data-stu-id="0ae32-121">This tensor must have *Sizes* of `{1,1,M,N}` (if *DimensionCount* is 4), or `{1,1,1,M,N}` (if *DimensionCount* is 5), where M is the total number of elements in the *InputTensor*, and N is greater or equal to the *effective rank* of *InputTensor*, up to the *DimensionCount* of the input.</span></span>

<span data-ttu-id="0ae32-122">Der effektive Rang eines Mandanten wird durch die *DimensionCount* dieses Mandanten mit Ausnahme der führenden Dimensionen der Größe 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0ae32-122">The effective rank of a tensor is determined by the *DimensionCount* of that tensor excluding leading dimensions of size 1.</span></span> <span data-ttu-id="0ae32-123">Ein tensorflow mit Größen von hat beispielsweise `{1,2,3,4}` einen effektiven Rang 3, ebenso wie ein tensorflow mit den Größen von `{1,1,5,5,5}` .</span><span class="sxs-lookup"><span data-stu-id="0ae32-123">For example a tensor with sizes of `{1,2,3,4}` has effective rank 3, as does a tensor with sizes of `{1,1,5,5,5}`.</span></span> <span data-ttu-id="0ae32-124">Ein tensorflow mit Größen `{1,1,1,1}` hat den gültigen Rang 0.</span><span class="sxs-lookup"><span data-stu-id="0ae32-124">A tensor with sizes `{1,1,1,1}` has effective rank 0.</span></span>

<span data-ttu-id="0ae32-125">Stellen Sie sich einen *inputtensor* mit *Größen* von vor `{1,1,12,5}` .</span><span class="sxs-lookup"><span data-stu-id="0ae32-125">Consider an *InputTensor* with *Sizes* of `{1,1,12,5}`.</span></span> <span data-ttu-id="0ae32-126">Dieser eingabetensor enthält 60 Elemente und hat einen effektiven Rang von 2.</span><span class="sxs-lookup"><span data-stu-id="0ae32-126">This input tensor contains 60 elements, and has an effective rank of 2.</span></span> <span data-ttu-id="0ae32-127">In diesem Beispiel weisen alle gültigen Größen von *outputcoordinatestensor* das Format auf `{1,1,60,N}` , wobei N >= 2, aber nicht größer als die *DimensionCount* (in diesem Beispiel 4) ist.</span><span class="sxs-lookup"><span data-stu-id="0ae32-127">In this example all valid sizes of *OutputCoordinatesTensor* are of the form `{1,1,60,N}`, where N >= 2 but no greater than the *DimensionCount* (4 in this example).</span></span>

<span data-ttu-id="0ae32-128">Die in diesen Mandanten geschriebenen Koordinaten werden garantiert nach dem aufsteigenden Element Index sortiert.</span><span class="sxs-lookup"><span data-stu-id="0ae32-128">The coordinates written into this tensor are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="0ae32-129">Wenn der Eingabe-tensorflow z. b. drei Werte ungleich NULL bei den Koordinaten {1,0} , {1,2} und enthält {0,5} , werden die Werte, die in den *outputcoordinatestensor* geschrieben werden, gleich sein `[[0,5], [1,0], [1,2]]` .</span><span class="sxs-lookup"><span data-stu-id="0ae32-129">For example if the input tensor has 3 non-zero values at coordinates {1,0}, {1,2}, and {0,5}, the values written to the *OutputCoordinatesTensor* will be `[[0,5], [1,0], [1,2]]`.</span></span>

<span data-ttu-id="0ae32-130">Während dieser Mandanten erfordert, dass die Dimension M mit der Anzahl der Elemente im eingabetensor identisch ist, schreibt dieser Operator nur maximal die outputcount-Elemente in diesen Mandanten.</span><span class="sxs-lookup"><span data-stu-id="0ae32-130">While this tensor requires its dimension M to equal the number of elements in the input tensor, this operator will only write a maximum of OutputCount elements to this tensor.</span></span> <span data-ttu-id="0ae32-131">Outputcount wird durch den skalaren *outputzählensor* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0ae32-131">The OutputCount is returned through the scalar *OutputCountTensor*.</span></span>

> [!NOTE]
> <span data-ttu-id="0ae32-132">Die übrigen Elemente dieses Mandanten außerhalb von outputcount sind nach Abschluss dieses Operators nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="0ae32-132">The remaining elements of this tensor beyond the OutputCount are undefined once this operator completes.</span></span> <span data-ttu-id="0ae32-133">Sie sollten sich nicht auf die Werte dieser Elemente verlassen.</span><span class="sxs-lookup"><span data-stu-id="0ae32-133">You shouldn't rely on the values of these elements.</span></span>

## <a name="example"></a><span data-ttu-id="0ae32-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0ae32-134">Example</span></span>

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a><span data-ttu-id="0ae32-135">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="0ae32-135">Availability</span></span>
<span data-ttu-id="0ae32-136">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="0ae32-136">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="0ae32-137">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="0ae32-137">Tensor constraints</span></span>
<span data-ttu-id="0ae32-138">" *Inputtensor*", " *outputcoordinatestensor*" und "" `OutputCountTensor` müssen dieselbe *DimensionCount* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0ae32-138">*InputTensor*, *OutputCoordinatesTensor*, and `OutputCountTensor` must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="0ae32-139">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0ae32-139">Tensor support</span></span>
| <span data-ttu-id="0ae32-140">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="0ae32-140">Tensor</span></span> | <span data-ttu-id="0ae32-141">Typ</span><span class="sxs-lookup"><span data-stu-id="0ae32-141">Kind</span></span> | <span data-ttu-id="0ae32-142">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="0ae32-142">Dimensions</span></span> | <span data-ttu-id="0ae32-143">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="0ae32-143">Supported dimension counts</span></span> | <span data-ttu-id="0ae32-144">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="0ae32-144">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="0ae32-145">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="0ae32-145">InputTensor</span></span> | <span data-ttu-id="0ae32-146">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0ae32-146">Input</span></span> | <span data-ttu-id="0ae32-147">{[D0], D1, D2, D3, D4}</span><span class="sxs-lookup"><span data-stu-id="0ae32-147">{ [D0], D1, D2, D3, D4 }</span></span> | <span data-ttu-id="0ae32-148">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="0ae32-148">4 to 5</span></span> | <span data-ttu-id="0ae32-149">Float32, FLOAT16, Int32, INT16, int8, UInt32, UInt16, Uint8</span><span class="sxs-lookup"><span data-stu-id="0ae32-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="0ae32-150">Outputzählensor</span><span class="sxs-lookup"><span data-stu-id="0ae32-150">OutputCountTensor</span></span> | <span data-ttu-id="0ae32-151">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="0ae32-151">Output</span></span> | <span data-ttu-id="0ae32-152">{[1], 1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="0ae32-152">{ [1], 1, 1, 1, 1 }</span></span> | <span data-ttu-id="0ae32-153">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="0ae32-153">4 to 5</span></span> | <span data-ttu-id="0ae32-154">UINT32</span><span class="sxs-lookup"><span data-stu-id="0ae32-154">UINT32</span></span> |
| <span data-ttu-id="0ae32-155">Outputcoordinatestensor</span><span class="sxs-lookup"><span data-stu-id="0ae32-155">OutputCoordinatesTensor</span></span> | <span data-ttu-id="0ae32-156">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="0ae32-156">Output</span></span> | <span data-ttu-id="0ae32-157">{[1], 1, 1, M, N}</span><span class="sxs-lookup"><span data-stu-id="0ae32-157">{ [1], 1, 1, M, N }</span></span> | <span data-ttu-id="0ae32-158">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="0ae32-158">4 to 5</span></span> | <span data-ttu-id="0ae32-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="0ae32-159">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="0ae32-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ae32-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0ae32-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="0ae32-161">**Header**</span></span> | <span data-ttu-id="0ae32-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="0ae32-162">directml.h</span></span> |