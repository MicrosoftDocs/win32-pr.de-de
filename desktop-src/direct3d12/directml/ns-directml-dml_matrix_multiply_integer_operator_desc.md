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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802841"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="5543f-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="5543f-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="5543f-104">Führt eine Matrixmultiplikationsfunktion für ganzzahlige Daten aus.</span><span class="sxs-lookup"><span data-stu-id="5543f-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="5543f-105">Dieser Operator erfordert, dass die Matrix-Multiplikationseingabe-Tensoren 4D sind, die als formatiert `{ BatchCount, ChannelCount, Height, Width }` sind.</span><span class="sxs-lookup"><span data-stu-id="5543f-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="5543f-106">Der Matrixmultiplikationsoperator führt BatchCount \* ChannelCount anzahl unabhängiger Matrixmultiplikationen aus.</span><span class="sxs-lookup"><span data-stu-id="5543f-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="5543f-107">Wenn *ATensor* z. *B. Größen* von `{ BatchCount, ChannelCount, M, K }` und *BTensor* *größen* von `{ BatchCount, ChannelCount, K, N }` und *OutputTensor* *Größen* von aufweist, führt `{ BatchCount, ChannelCount, M, N }` der Multiplikationsoperator der Matrix BatchCount \* ChannelCount unabhängige Matrixmultiplikationen der Dimensionen {M,K} x {K,N} = {M,N} aus.</span><span class="sxs-lookup"><span data-stu-id="5543f-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5543f-108">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="5543f-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5543f-109">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="5543f-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5543f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5543f-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="5543f-111">Member</span><span class="sxs-lookup"><span data-stu-id="5543f-111">Members</span></span>

`ATensor`

<span data-ttu-id="5543f-112">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5543f-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5543f-113">Ein Tensor, der die A-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5543f-113">A tensor containing the A data.</span></span> <span data-ttu-id="5543f-114">Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, M, K }` sein.</span><span class="sxs-lookup"><span data-stu-id="5543f-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="5543f-115">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5543f-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5543f-116">Ein optionaler Tensor, der die Nullpunktdaten von ATensor enthält.</span><span class="sxs-lookup"><span data-stu-id="5543f-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="5543f-117">Die erwarteten Dimensionen von `AZeroPointTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder wenn eine `{ 1, 1, M, 1 }` Zeilen-Quantisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5543f-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="5543f-118">Diese Nullpunktwerte werden zum Dequantisieren der *ATensor-Werte* verwendet.</span><span class="sxs-lookup"><span data-stu-id="5543f-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="5543f-119">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5543f-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5543f-120">Ein Tensor, der die B-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5543f-120">A tensor containing the B data.</span></span> <span data-ttu-id="5543f-121">Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, K, N }` sein.</span><span class="sxs-lookup"><span data-stu-id="5543f-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="5543f-122">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5543f-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5543f-123">Ein optionaler Tensor, der die Nullpunktdaten von *BTensor* enthält.</span><span class="sxs-lookup"><span data-stu-id="5543f-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="5543f-124">Die erwarteten Dimensionen von sind `BZeroPointTensor` , wenn eine Tensorquantisierung erforderlich ist, oder , wenn eine `{ 1, 1, 1, 1 }` Quantisierung pro Spalte erforderlich `{ 1, 1, 1, N }` ist.</span><span class="sxs-lookup"><span data-stu-id="5543f-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="5543f-125">Diese Nullpunktwerte werden zum Dequantisieren der BTensor-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="5543f-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="5543f-126">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5543f-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5543f-127">Ein Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5543f-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="5543f-128">Die Dimensionen dieses Tensors sind `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="5543f-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="5543f-129">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="5543f-129">Availability</span></span>
<span data-ttu-id="5543f-130">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5543f-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5543f-131">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="5543f-131">Tensor constraints</span></span>
* <span data-ttu-id="5543f-132">*ATensor und* `AZeroPointTensor` müssen den gleichen Datentyp *haben.*</span><span class="sxs-lookup"><span data-stu-id="5543f-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="5543f-133">*BTensor und* `BZeroPointTensor` müssen den gleichen Datentyp *haben.*</span><span class="sxs-lookup"><span data-stu-id="5543f-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5543f-134">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="5543f-134">Tensor support</span></span>
| <span data-ttu-id="5543f-135">Tensor</span><span class="sxs-lookup"><span data-stu-id="5543f-135">Tensor</span></span> | <span data-ttu-id="5543f-136">Typ</span><span class="sxs-lookup"><span data-stu-id="5543f-136">Kind</span></span> | <span data-ttu-id="5543f-137">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="5543f-137">Dimensions</span></span> | <span data-ttu-id="5543f-138">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="5543f-138">Supported dimension counts</span></span> | <span data-ttu-id="5543f-139">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="5543f-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="5543f-140">ATensor</span><span class="sxs-lookup"><span data-stu-id="5543f-140">ATensor</span></span> | <span data-ttu-id="5543f-141">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5543f-141">Input</span></span> | <span data-ttu-id="5543f-142">{ BatchCount, ChannelCount, M, K }</span><span class="sxs-lookup"><span data-stu-id="5543f-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="5543f-143">4</span><span class="sxs-lookup"><span data-stu-id="5543f-143">4</span></span> | <span data-ttu-id="5543f-144">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="5543f-144">INT8, UINT8</span></span> |
| <span data-ttu-id="5543f-145">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="5543f-145">AZeroPointTensor</span></span> | <span data-ttu-id="5543f-146">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="5543f-146">Optional input</span></span> | <span data-ttu-id="5543f-147">{ 1, 1, AZeroPointCount, 1 }</span><span class="sxs-lookup"><span data-stu-id="5543f-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="5543f-148">4</span><span class="sxs-lookup"><span data-stu-id="5543f-148">4</span></span> | <span data-ttu-id="5543f-149">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="5543f-149">INT8, UINT8</span></span> |
| <span data-ttu-id="5543f-150">BTensor</span><span class="sxs-lookup"><span data-stu-id="5543f-150">BTensor</span></span> | <span data-ttu-id="5543f-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5543f-151">Input</span></span> | <span data-ttu-id="5543f-152">{ BatchCount, ChannelCount, K, N }</span><span class="sxs-lookup"><span data-stu-id="5543f-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="5543f-153">4</span><span class="sxs-lookup"><span data-stu-id="5543f-153">4</span></span> | <span data-ttu-id="5543f-154">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="5543f-154">INT8, UINT8</span></span> |
| <span data-ttu-id="5543f-155">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="5543f-155">BZeroPointTensor</span></span> | <span data-ttu-id="5543f-156">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="5543f-156">Optional input</span></span> | <span data-ttu-id="5543f-157">{ 1, 1, 1, BZeroPointCount }</span><span class="sxs-lookup"><span data-stu-id="5543f-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="5543f-158">4</span><span class="sxs-lookup"><span data-stu-id="5543f-158">4</span></span> | <span data-ttu-id="5543f-159">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="5543f-159">INT8, UINT8</span></span> |
| <span data-ttu-id="5543f-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5543f-160">OutputTensor</span></span> | <span data-ttu-id="5543f-161">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5543f-161">Output</span></span> | <span data-ttu-id="5543f-162">{ BatchCount, ChannelCount, M, N }</span><span class="sxs-lookup"><span data-stu-id="5543f-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="5543f-163">4</span><span class="sxs-lookup"><span data-stu-id="5543f-163">4</span></span> | <span data-ttu-id="5543f-164">INT32</span><span class="sxs-lookup"><span data-stu-id="5543f-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="5543f-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5543f-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5543f-166">**Header**</span><span class="sxs-lookup"><span data-stu-id="5543f-166">**Header**</span></span> | <span data-ttu-id="5543f-167">directml.h</span><span class="sxs-lookup"><span data-stu-id="5543f-167">directml.h</span></span> |