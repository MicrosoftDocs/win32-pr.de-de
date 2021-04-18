---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Führt eine Matrix Multiplikations Funktion für ganzzahlige Daten aus.
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
ms.openlocfilehash: f6ecccf49b0d7123e6f41321c7ba1bf8e8d4ad87
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351188"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="e0082-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="e0082-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="e0082-104">Führt eine Matrix Multiplikations Funktion für ganzzahlige Daten aus.</span><span class="sxs-lookup"><span data-stu-id="e0082-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="e0082-105">Dieser Operator erfordert, dass die Eingabe-Tensoren der Matrix als 4D-Wert vorliegen, die als formatiert sind `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="e0082-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="e0082-106">Der Matrix Multiplikations Operator führt die BatchCount \* ChannelCount-Anzahl unabhängiger Matrix Multiplikationen durch.</span><span class="sxs-lookup"><span data-stu-id="e0082-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="e0082-107">Wenn *atensor* z. b. *Größen* von hat `{ BatchCount, ChannelCount, M, K }` und *btensor* die *Größe* hat `{ BatchCount, ChannelCount, K, N }` und *outputtensor* über *Größen* von verfügt `{ BatchCount, ChannelCount, M, N }` , führt der Matrix Multiplikations Operator BatchCount \* ChannelCount unabhängige Matrix Multiplikationen der Dimensionen {m, K} x {K, n} = {M, n} aus.</span><span class="sxs-lookup"><span data-stu-id="e0082-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0082-108">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="e0082-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e0082-109">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e0082-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0082-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0082-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="e0082-111">Member</span><span class="sxs-lookup"><span data-stu-id="e0082-111">Members</span></span>

`ATensor`

<span data-ttu-id="e0082-112">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e0082-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e0082-113">Ein tensorflow, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e0082-113">A tensor containing the A data.</span></span> <span data-ttu-id="e0082-114">Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="e0082-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="e0082-115">Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e0082-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e0082-116">Ein optionaler tensorflow, der die Daten des atensor-NULL-Punkts enthält.</span><span class="sxs-lookup"><span data-stu-id="e0082-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="e0082-117">Die erwarteten Dimensionen von `AZeroPointTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, M, 1 }` Wenn die pro-Zeilen-Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e0082-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="e0082-118">Diese nullpunktwerte werden zum decomieren der *atensor* -Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0082-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="e0082-119">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e0082-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e0082-120">Ein tensorflow, der die B-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e0082-120">A tensor containing the B data.</span></span> <span data-ttu-id="e0082-121">Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="e0082-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="e0082-122">Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e0082-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e0082-123">Ein optionaler tensorflow, der die Daten des *btensor* -NULL-Punkts enthält.</span><span class="sxs-lookup"><span data-stu-id="e0082-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="e0082-124">Die erwarteten Dimensionen von `BZeroPointTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, 1, N }` Wenn pro Spalten Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e0082-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="e0082-125">Diese nullpunktwerte werden zum decomieren der btensor-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0082-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="e0082-126">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e0082-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e0082-127">Ein tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e0082-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="e0082-128">Die Dimensionen dieses Mandanten sind `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="e0082-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="e0082-129">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="e0082-129">Availability</span></span>
<span data-ttu-id="e0082-130">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e0082-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e0082-131">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="e0082-131">Tensor constraints</span></span>
* <span data-ttu-id="e0082-132">*Atensor* und `AZeroPointTensor` muss denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e0082-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="e0082-133">*Btensor* und `BZeroPointTensor` muss denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e0082-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e0082-134">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="e0082-134">Tensor support</span></span>
| <span data-ttu-id="e0082-135">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="e0082-135">Tensor</span></span> | <span data-ttu-id="e0082-136">Typ</span><span class="sxs-lookup"><span data-stu-id="e0082-136">Kind</span></span> | <span data-ttu-id="e0082-137">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="e0082-137">Dimensions</span></span> | <span data-ttu-id="e0082-138">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="e0082-138">Supported dimension counts</span></span> | <span data-ttu-id="e0082-139">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="e0082-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="e0082-140">Atensor</span><span class="sxs-lookup"><span data-stu-id="e0082-140">ATensor</span></span> | <span data-ttu-id="e0082-141">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0082-141">Input</span></span> | <span data-ttu-id="e0082-142">{BatchCount, ChannelCount, M, K}</span><span class="sxs-lookup"><span data-stu-id="e0082-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="e0082-143">4</span><span class="sxs-lookup"><span data-stu-id="e0082-143">4</span></span> | <span data-ttu-id="e0082-144">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="e0082-144">INT8, UINT8</span></span> |
| <span data-ttu-id="e0082-145">Azeropointtensor</span><span class="sxs-lookup"><span data-stu-id="e0082-145">AZeroPointTensor</span></span> | <span data-ttu-id="e0082-146">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0082-146">Optional input</span></span> | <span data-ttu-id="e0082-147">{1, 1, azeropointcount, 1}</span><span class="sxs-lookup"><span data-stu-id="e0082-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="e0082-148">4</span><span class="sxs-lookup"><span data-stu-id="e0082-148">4</span></span> | <span data-ttu-id="e0082-149">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="e0082-149">INT8, UINT8</span></span> |
| <span data-ttu-id="e0082-150">Btensor</span><span class="sxs-lookup"><span data-stu-id="e0082-150">BTensor</span></span> | <span data-ttu-id="e0082-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0082-151">Input</span></span> | <span data-ttu-id="e0082-152">{BatchCount, ChannelCount, K, N}</span><span class="sxs-lookup"><span data-stu-id="e0082-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="e0082-153">4</span><span class="sxs-lookup"><span data-stu-id="e0082-153">4</span></span> | <span data-ttu-id="e0082-154">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="e0082-154">INT8, UINT8</span></span> |
| <span data-ttu-id="e0082-155">Bzeropointtensor</span><span class="sxs-lookup"><span data-stu-id="e0082-155">BZeroPointTensor</span></span> | <span data-ttu-id="e0082-156">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0082-156">Optional input</span></span> | <span data-ttu-id="e0082-157">{1, 1, 1, bzeropointcount}</span><span class="sxs-lookup"><span data-stu-id="e0082-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="e0082-158">4</span><span class="sxs-lookup"><span data-stu-id="e0082-158">4</span></span> | <span data-ttu-id="e0082-159">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="e0082-159">INT8, UINT8</span></span> |
| <span data-ttu-id="e0082-160">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="e0082-160">OutputTensor</span></span> | <span data-ttu-id="e0082-161">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e0082-161">Output</span></span> | <span data-ttu-id="e0082-162">{BatchCount, ChannelCount, M, N}</span><span class="sxs-lookup"><span data-stu-id="e0082-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="e0082-163">4</span><span class="sxs-lookup"><span data-stu-id="e0082-163">4</span></span> | <span data-ttu-id="e0082-164">INT32</span><span class="sxs-lookup"><span data-stu-id="e0082-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="e0082-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0082-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e0082-166">**Header**</span><span class="sxs-lookup"><span data-stu-id="e0082-166">**Header**</span></span> | <span data-ttu-id="e0082-167">directml. h</span><span class="sxs-lookup"><span data-stu-id="e0082-167">directml.h</span></span> |