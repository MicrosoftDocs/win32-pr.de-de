---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Führt eine Matrixmultiplikationsfunktion für ganzzahlige Daten aus.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417603"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="55497-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="55497-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="55497-104">Führt eine Matrixmultiplikationsfunktion für ganzzahlige Daten aus.</span><span class="sxs-lookup"><span data-stu-id="55497-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="55497-105">Für diesen Operator müssen die Matrix-Multiplikationseingabetensoren 4D sein, die als formatiert `{ BatchCount, ChannelCount, Height, Width }` sind.</span><span class="sxs-lookup"><span data-stu-id="55497-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="55497-106">Der Matrixmultiplikationsoperator führt BatchCount \* ChannelCount number of independent matrix multiplications (Anzahl unabhängiger Matrixmultiplikationen) aus.</span><span class="sxs-lookup"><span data-stu-id="55497-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="55497-107">Wenn *ATensor* beispielsweise  über Größen von verfügt und BTensor über Größen von verfügt und OutputTensor größen von hat, führt der Matrixmultiplikationsoperator batchCount \* ChannelCount unabhängige Matrixmultiplikationen von Dimensionen `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N} aus.</span><span class="sxs-lookup"><span data-stu-id="55497-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55497-108">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="55497-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="55497-109">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="55497-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="55497-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="55497-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="55497-111">Member</span><span class="sxs-lookup"><span data-stu-id="55497-111">Members</span></span>

`ATensor`

<span data-ttu-id="55497-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="55497-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="55497-113">Ein Tensor, der die A-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="55497-113">A tensor containing the A data.</span></span> <span data-ttu-id="55497-114">Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, M, K }` sein.</span><span class="sxs-lookup"><span data-stu-id="55497-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="55497-115">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="55497-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="55497-116">Ein optionaler Tensor, der die ATensor-Nullpunktdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="55497-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="55497-117">Die erwarteten Dimensionen von sind `AZeroPointTensor` , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine Quantisierung pro Zeile `{ 1, 1, 1, 1 }` `{ 1, 1, M, 1 }` erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="55497-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="55497-118">Diese Nullpunktwerte werden zum Dequantisieren der *ATensor-Werte* verwendet.</span><span class="sxs-lookup"><span data-stu-id="55497-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="55497-119">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="55497-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="55497-120">Ein Tensor, der die B-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="55497-120">A tensor containing the B data.</span></span> <span data-ttu-id="55497-121">Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, K, N }` sein.</span><span class="sxs-lookup"><span data-stu-id="55497-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="55497-122">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="55497-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="55497-123">Ein optionaler Tensor, der die *BTensor-Nullpunktdaten* enthält.</span><span class="sxs-lookup"><span data-stu-id="55497-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="55497-124">Die erwarteten Dimensionen von sind `BZeroPointTensor` , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine `{ 1, 1, 1, 1 }` Quantisierung pro Spalte erforderlich `{ 1, 1, 1, N }` ist.</span><span class="sxs-lookup"><span data-stu-id="55497-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="55497-125">Diese Nullpunktwerte werden zum Dequantisieren der BTensor-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="55497-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="55497-126">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="55497-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="55497-127">Ein Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="55497-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="55497-128">Die Dimensionen dieses Tensors sind `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="55497-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="55497-129">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="55497-129">Availability</span></span>
<span data-ttu-id="55497-130">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="55497-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="55497-131">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="55497-131">Tensor constraints</span></span>
* <span data-ttu-id="55497-132">*ATensor und* `AZeroPointTensor` müssen den gleichen Datentyp *haben.*</span><span class="sxs-lookup"><span data-stu-id="55497-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="55497-133">*BTensor* und `BZeroPointTensor` müssen den gleichen Datentyp *haben.*</span><span class="sxs-lookup"><span data-stu-id="55497-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="55497-134">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="55497-134">Tensor support</span></span>
| <span data-ttu-id="55497-135">Tensor</span><span class="sxs-lookup"><span data-stu-id="55497-135">Tensor</span></span> | <span data-ttu-id="55497-136">Typ</span><span class="sxs-lookup"><span data-stu-id="55497-136">Kind</span></span> | <span data-ttu-id="55497-137">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="55497-137">Dimensions</span></span> | <span data-ttu-id="55497-138">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="55497-138">Supported dimension counts</span></span> | <span data-ttu-id="55497-139">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="55497-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="55497-140">ATensor</span><span class="sxs-lookup"><span data-stu-id="55497-140">ATensor</span></span> | <span data-ttu-id="55497-141">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55497-141">Input</span></span> | <span data-ttu-id="55497-142">{ BatchCount, ChannelCount, M, K }</span><span class="sxs-lookup"><span data-stu-id="55497-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="55497-143">4</span><span class="sxs-lookup"><span data-stu-id="55497-143">4</span></span> | <span data-ttu-id="55497-144">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="55497-144">INT8, UINT8</span></span> |
| <span data-ttu-id="55497-145">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="55497-145">AZeroPointTensor</span></span> | <span data-ttu-id="55497-146">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="55497-146">Optional input</span></span> | <span data-ttu-id="55497-147">{ 1, 1, AZeroPointCount, 1 }</span><span class="sxs-lookup"><span data-stu-id="55497-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="55497-148">4</span><span class="sxs-lookup"><span data-stu-id="55497-148">4</span></span> | <span data-ttu-id="55497-149">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="55497-149">INT8, UINT8</span></span> |
| <span data-ttu-id="55497-150">BTensor</span><span class="sxs-lookup"><span data-stu-id="55497-150">BTensor</span></span> | <span data-ttu-id="55497-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55497-151">Input</span></span> | <span data-ttu-id="55497-152">{ BatchCount, ChannelCount, K, N }</span><span class="sxs-lookup"><span data-stu-id="55497-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="55497-153">4</span><span class="sxs-lookup"><span data-stu-id="55497-153">4</span></span> | <span data-ttu-id="55497-154">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="55497-154">INT8, UINT8</span></span> |
| <span data-ttu-id="55497-155">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="55497-155">BZeroPointTensor</span></span> | <span data-ttu-id="55497-156">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="55497-156">Optional input</span></span> | <span data-ttu-id="55497-157">{ 1, 1, 1, BZeroPointCount }</span><span class="sxs-lookup"><span data-stu-id="55497-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="55497-158">4</span><span class="sxs-lookup"><span data-stu-id="55497-158">4</span></span> | <span data-ttu-id="55497-159">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="55497-159">INT8, UINT8</span></span> |
| <span data-ttu-id="55497-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="55497-160">OutputTensor</span></span> | <span data-ttu-id="55497-161">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="55497-161">Output</span></span> | <span data-ttu-id="55497-162">{ BatchCount, ChannelCount, M, N }</span><span class="sxs-lookup"><span data-stu-id="55497-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="55497-163">4</span><span class="sxs-lookup"><span data-stu-id="55497-163">4</span></span> | <span data-ttu-id="55497-164">INT32</span><span class="sxs-lookup"><span data-stu-id="55497-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="55497-165">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="55497-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="55497-166">**Header**</span><span class="sxs-lookup"><span data-stu-id="55497-166">**Header**</span></span> | <span data-ttu-id="55497-167">directml.h</span><span class="sxs-lookup"><span data-stu-id="55497-167">directml.h</span></span> |