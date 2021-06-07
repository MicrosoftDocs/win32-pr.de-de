---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Berechnet die N-dimensionalen Koordinaten aller Nicht-Null-Elemente des Eingabetensors.
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
ms.openlocfilehash: 39463ba57bc90b35d5ac5dc7fc43993169137221
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417236"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a><span data-ttu-id="467fd-103">DML_NONZERO_COORDINATES_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="467fd-103">DML_NONZERO_COORDINATES_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="467fd-104">Berechnet die N-dimensionalen Koordinaten aller Nicht-Null-Elemente des Eingabetensors.</span><span class="sxs-lookup"><span data-stu-id="467fd-104">Computes the N-dimensional coordinates of all non-zero elements of the input tensor.</span></span>

<span data-ttu-id="467fd-105">Dieser Operator erzeugt eine MxN-Matrix von Werten, wobei jede Zeile M eine N-dimensionale Koordinate eines Werts enthält, der nicht 0 (null) aus der Eingabe ist.</span><span class="sxs-lookup"><span data-stu-id="467fd-105">This operator produces an MxN matrix of values, where each row M contains an N-dimensional coordinate of a non-zero value from the input.</span></span> <span data-ttu-id="467fd-106">Bei Verwendung **von FLOAT32-** oder **FLOAT16-Eingaben** werden sowohl negative als auch positive 0 (0,0f und -0,0f) im Rahmen dieses Operators als 0 (null) behandelt.</span><span class="sxs-lookup"><span data-stu-id="467fd-106">When using **FLOAT32** or **FLOAT16** inputs, both negative and positive 0 (0.0f and -0.0f) are treated as zero for the purposes of this operator.</span></span>

<span data-ttu-id="467fd-107">Der -Operator erfordert, dass *der OutputCoordinatesTensor* groß genug ist, um ein ungünstigstes Szenario zu bieten, bei dem jedes Element der Eingabe nicht 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="467fd-107">The operator requires that the *OutputCoordinatesTensor* has a size large enough to accommodate a worst-case scenario where every element of the input is non-zero.</span></span> <span data-ttu-id="467fd-108">Dieser Operator gibt die Anzahl der Elemente, die nicht null sind, über den *OutputCountTensor* zurück, den Aufrufer überprüfen können, um die Anzahl der Koordinaten zu bestimmen, die in den *OutputCoordinatesTensor* geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="467fd-108">This operator returns the count of of non-zero elements via the *OutputCountTensor*, which callers can inspect to determine the number of coordinates written to the *OutputCoordinatesTensor*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="467fd-109">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="467fd-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="467fd-110">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="467fd-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="467fd-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="467fd-111">Syntax</span></span>

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a><span data-ttu-id="467fd-112">Member</span><span class="sxs-lookup"><span data-stu-id="467fd-112">Members</span></span>

`InputTensor`

<span data-ttu-id="467fd-113">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="467fd-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="467fd-114">Ein Eingabe tensor.</span><span class="sxs-lookup"><span data-stu-id="467fd-114">An input tensor.</span></span>

`OutputCountTensor`

<span data-ttu-id="467fd-115">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="467fd-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="467fd-116">Ein Ausgabe-Tensor, der die Anzahl von Elementen enthält, die nicht 0 (null) im Eingabetensor sind.</span><span class="sxs-lookup"><span data-stu-id="467fd-116">An output tensor that holds the count of non-zero elements in the input tensor.</span></span> <span data-ttu-id="467fd-117">This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1.</span><span class="sxs-lookup"><span data-stu-id="467fd-117">This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1.</span></span> <span data-ttu-id="467fd-118">Der Typ dieses Tensors muss **UINT32 sein.**</span><span class="sxs-lookup"><span data-stu-id="467fd-118">The type of this tensor must be **UINT32**.</span></span>

`OutputCoordinatesTensor`

<span data-ttu-id="467fd-119">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="467fd-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="467fd-120">Ein Ausgabe-Tensor, der die n-dimensionalen Koordinaten der Eingabeelemente enthält, die nicht 0 (null) sind.</span><span class="sxs-lookup"><span data-stu-id="467fd-120">An output tensor that holds the N-dimensional coordinates of the input elements which are non-zero.</span></span> 

<span data-ttu-id="467fd-121">Dieser Tensor  muss größen von `{1,1,M,N}` (wenn *DimensionCount* gleich 4 ist) oder `{1,1,1,M,N}` (wenn *DimensionCount* 5  ist), wobei M die Gesamtzahl der Elemente im *InputTensor* und N größer oder gleich dem effektiven Rang von *InputTensor* bis zum *DimensionCount-Wert* der Eingabe ist.</span><span class="sxs-lookup"><span data-stu-id="467fd-121">This tensor must have *Sizes* of `{1,1,M,N}` (if *DimensionCount* is 4), or `{1,1,1,M,N}` (if *DimensionCount* is 5), where M is the total number of elements in the *InputTensor*, and N is greater or equal to the *effective rank* of *InputTensor*, up to the *DimensionCount* of the input.</span></span>

<span data-ttu-id="467fd-122">Der effektive Rang eines Tensors wird durch *DimensionCount* dieses Tensors ohne führende Dimensionen der Größe 1 bestimmt.</span><span class="sxs-lookup"><span data-stu-id="467fd-122">The effective rank of a tensor is determined by the *DimensionCount* of that tensor excluding leading dimensions of size 1.</span></span> <span data-ttu-id="467fd-123">Beispielsweise hat ein Tensor mit größen von den effektiven Rang 3, ebenso wie ein `{1,2,3,4}` Tensor mit größen von `{1,1,5,5,5}` .</span><span class="sxs-lookup"><span data-stu-id="467fd-123">For example a tensor with sizes of `{1,2,3,4}` has effective rank 3, as does a tensor with sizes of `{1,1,5,5,5}`.</span></span> <span data-ttu-id="467fd-124">Ein Tensor mit Größen hat `{1,1,1,1}` den effektiven Rang 0.</span><span class="sxs-lookup"><span data-stu-id="467fd-124">A tensor with sizes `{1,1,1,1}` has effective rank 0.</span></span>

<span data-ttu-id="467fd-125">Stellen Sie sich *einen InputTensor mit* *größen von* `{1,1,12,5}` vor.</span><span class="sxs-lookup"><span data-stu-id="467fd-125">Consider an *InputTensor* with *Sizes* of `{1,1,12,5}`.</span></span> <span data-ttu-id="467fd-126">Dieser Eingabetensor enthält 60 Elemente und hat einen effektiven Rang von 2.</span><span class="sxs-lookup"><span data-stu-id="467fd-126">This input tensor contains 60 elements, and has an effective rank of 2.</span></span> <span data-ttu-id="467fd-127">In diesem Beispiel haben alle gültigen Größen von *OutputCoordinatesTensor* das Format , wobei N >= 2, aber nicht größer als `{1,1,60,N}` *DimensionCount* (in diesem Beispiel 4) ist.</span><span class="sxs-lookup"><span data-stu-id="467fd-127">In this example all valid sizes of *OutputCoordinatesTensor* are of the form `{1,1,60,N}`, where N >= 2 but no greater than the *DimensionCount* (4 in this example).</span></span>

<span data-ttu-id="467fd-128">Die in diesen Tensor geschriebenen Koordinaten werden garantiert nach dem aufsteigenden Elementindex geordnet.</span><span class="sxs-lookup"><span data-stu-id="467fd-128">The coordinates written into this tensor are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="467fd-129">Wenn der Eingabetensor z. B. drei Werte an den Koordinaten , und hat, sind die werte, die in {1,0} {1,2} den {0,5} *OutputCoordinatesTensor* geschrieben werden, `[[0,5], [1,0], [1,2]]` .</span><span class="sxs-lookup"><span data-stu-id="467fd-129">For example if the input tensor has 3 non-zero values at coordinates {1,0}, {1,2}, and {0,5}, the values written to the *OutputCoordinatesTensor* will be `[[0,5], [1,0], [1,2]]`.</span></span>

<span data-ttu-id="467fd-130">Während für diesen Tensor die Dimension M der Anzahl der Elemente im Eingabetensor entspricht, schreibt dieser Operator nur maximal OutputCount-Elemente in diesen Tensor.</span><span class="sxs-lookup"><span data-stu-id="467fd-130">While this tensor requires its dimension M to equal the number of elements in the input tensor, this operator will only write a maximum of OutputCount elements to this tensor.</span></span> <span data-ttu-id="467fd-131">OutputCount wird über den skalaren *OutputCountTensor zurückgegeben.*</span><span class="sxs-lookup"><span data-stu-id="467fd-131">The OutputCount is returned through the scalar *OutputCountTensor*.</span></span>

> [!NOTE]
> <span data-ttu-id="467fd-132">Die verbleibenden Elemente dieses Tensors außerhalb von OutputCount sind nach Abschluss dieses Operators nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="467fd-132">The remaining elements of this tensor beyond the OutputCount are undefined once this operator completes.</span></span> <span data-ttu-id="467fd-133">Sie sollten sich nicht auf die Werte dieser Elemente verlassen.</span><span class="sxs-lookup"><span data-stu-id="467fd-133">You shouldn't rely on the values of these elements.</span></span>

## <a name="example"></a><span data-ttu-id="467fd-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="467fd-134">Example</span></span>

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

## <a name="availability"></a><span data-ttu-id="467fd-135">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="467fd-135">Availability</span></span>
<span data-ttu-id="467fd-136">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="467fd-136">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="467fd-137">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="467fd-137">Tensor constraints</span></span>
<span data-ttu-id="467fd-138">*InputTensor*, *OutputCoordinatesTensor* und müssen `OutputCountTensor` denselben *DimensionCount aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="467fd-138">*InputTensor*, *OutputCoordinatesTensor*, and `OutputCountTensor` must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="467fd-139">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="467fd-139">Tensor support</span></span>
| <span data-ttu-id="467fd-140">Tensor</span><span class="sxs-lookup"><span data-stu-id="467fd-140">Tensor</span></span> | <span data-ttu-id="467fd-141">Typ</span><span class="sxs-lookup"><span data-stu-id="467fd-141">Kind</span></span> | <span data-ttu-id="467fd-142">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="467fd-142">Dimensions</span></span> | <span data-ttu-id="467fd-143">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="467fd-143">Supported dimension counts</span></span> | <span data-ttu-id="467fd-144">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="467fd-144">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="467fd-145">InputTensor</span><span class="sxs-lookup"><span data-stu-id="467fd-145">InputTensor</span></span> | <span data-ttu-id="467fd-146">Eingabe</span><span class="sxs-lookup"><span data-stu-id="467fd-146">Input</span></span> | <span data-ttu-id="467fd-147">{ [D0], D1, D2, D3, D4 }</span><span class="sxs-lookup"><span data-stu-id="467fd-147">{ [D0], D1, D2, D3, D4 }</span></span> | <span data-ttu-id="467fd-148">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="467fd-148">4 to 5</span></span> | <span data-ttu-id="467fd-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="467fd-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="467fd-150">OutputCountTensor</span><span class="sxs-lookup"><span data-stu-id="467fd-150">OutputCountTensor</span></span> | <span data-ttu-id="467fd-151">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="467fd-151">Output</span></span> | <span data-ttu-id="467fd-152">{ [1], 1, 1, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="467fd-152">{ [1], 1, 1, 1, 1 }</span></span> | <span data-ttu-id="467fd-153">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="467fd-153">4 to 5</span></span> | <span data-ttu-id="467fd-154">UINT32</span><span class="sxs-lookup"><span data-stu-id="467fd-154">UINT32</span></span> |
| <span data-ttu-id="467fd-155">OutputCoordinatesTensor</span><span class="sxs-lookup"><span data-stu-id="467fd-155">OutputCoordinatesTensor</span></span> | <span data-ttu-id="467fd-156">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="467fd-156">Output</span></span> | <span data-ttu-id="467fd-157">{ [1], 1, 1, M, N }</span><span class="sxs-lookup"><span data-stu-id="467fd-157">{ [1], 1, 1, M, N }</span></span> | <span data-ttu-id="467fd-158">4 bis 5</span><span class="sxs-lookup"><span data-stu-id="467fd-158">4 to 5</span></span> | <span data-ttu-id="467fd-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="467fd-159">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="467fd-160">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="467fd-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="467fd-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="467fd-161">**Header**</span></span> | <span data-ttu-id="467fd-162">directml.h</span><span class="sxs-lookup"><span data-stu-id="467fd-162">directml.h</span></span> |