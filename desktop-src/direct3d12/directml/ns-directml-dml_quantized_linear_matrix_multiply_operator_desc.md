---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Führt eine Matrixmultiplikationsfunktion für quantisierte Daten aus. Dieser Operator entspricht mathematisch der Dequantisierung der Eingaben, der anschließenden Matrixmultiplikation und der anschließenden Quantisierung der Ausgabe.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417810"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="726a3-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="726a3-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="726a3-105">Führt eine Matrixmultiplikationsfunktion für quantisierte Daten aus.</span><span class="sxs-lookup"><span data-stu-id="726a3-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="726a3-106">Dieser Operator entspricht mathematisch der Dequantisierung der Eingaben, der anschließenden Matrixmultiplikation und der anschließenden Quantisierung der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="726a3-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="726a3-107">Dieser Operator erfordert, dass die Matrix-Multiplikationseingabe-Tensoren 4D sind, die als formatiert `{ BatchCount, ChannelCount, Height, Width }` sind.</span><span class="sxs-lookup"><span data-stu-id="726a3-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="726a3-108">Der Matrixmultiplikationsoperator führt BatchCount \* ChannelCount anzahl unabhängiger Matrixmultiplikationen aus.</span><span class="sxs-lookup"><span data-stu-id="726a3-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="726a3-109">Wenn *ATensor* z. *B. Größen* von und `{ BatchCount, ChannelCount, M, K }` *BTensor* *größen* von `{ BatchCount, ChannelCount, K, N }` und *OutputTensor* *Größen* von aufweist, führt `{ BatchCount, ChannelCount, M, N }` der Multiplikationsoperator der Matrix BatchCount \* ChannelCount unabhängige Matrixmultiplikationen der Dimensionen {M,K} x {K,N} = {M,N} aus.</span><span class="sxs-lookup"><span data-stu-id="726a3-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="726a3-110">Dequantize-Funktion</span><span class="sxs-lookup"><span data-stu-id="726a3-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="726a3-111">Quantize-Funktion</span><span class="sxs-lookup"><span data-stu-id="726a3-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="726a3-112">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="726a3-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="726a3-113">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="726a3-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="726a3-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="726a3-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="726a3-115">Member</span><span class="sxs-lookup"><span data-stu-id="726a3-115">Members</span></span>

`ATensor`

<span data-ttu-id="726a3-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="726a3-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="726a3-117">Ein Tensor, der die A-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="726a3-117">A tensor containing the A data.</span></span> <span data-ttu-id="726a3-118">Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, M, K }` sein.</span><span class="sxs-lookup"><span data-stu-id="726a3-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="726a3-119">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="726a3-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="726a3-120">Ein Tensor, der die ATensor-Skalierungsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="726a3-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="726a3-121">Die erwarteten Dimensionen von `AScaleTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn eine Quantisierung pro Zeile erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="726a3-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="726a3-122">Diese Skalierungswerte werden zum Dequantisieren der A-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="726a3-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="726a3-123">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="726a3-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="726a3-124">Ein optionaler Tensor, der die Nullpunktdaten von *ATensor* enthält.</span><span class="sxs-lookup"><span data-stu-id="726a3-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="726a3-125">Die erwarteten Dimensionen von AZeroPointTensor sind `{ 1, 1, 1, 1 }` , wenn eine Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn eine Quantisierung pro Zeile erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="726a3-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="726a3-126">Diese Nullpunktwerte werden zum Dequantisieren der ATensor-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="726a3-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="726a3-127">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="726a3-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="726a3-128">Ein Tensor, der die B-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="726a3-128">A tensor containing the B data.</span></span> <span data-ttu-id="726a3-129">Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, K, N }` sein.</span><span class="sxs-lookup"><span data-stu-id="726a3-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="726a3-130">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="726a3-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="726a3-131">Ein Tensor, der die *BTensor-Skalierungsdaten* enthält.</span><span class="sxs-lookup"><span data-stu-id="726a3-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="726a3-132">Die erwarteten Dimensionen von `BScaleTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, 1, N }` wenn eine Spaltenquantisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="726a3-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="726a3-133">Diese Skalierungswerte werden zum Dequantisieren der *BTensor-Werte* verwendet.</span><span class="sxs-lookup"><span data-stu-id="726a3-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="726a3-134">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="726a3-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="726a3-135">Ein optionaler Tensor, der die Nullpunktdaten von *BTensor* enthält.</span><span class="sxs-lookup"><span data-stu-id="726a3-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="726a3-136">Die erwarteten Dimensionen von `BZeroPointTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, 1, N }` wenn eine Spaltenquantisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="726a3-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="726a3-137">Diese Nullpunktwerte werden zum Dequantisieren der *BTensor-Werte* verwendet.</span><span class="sxs-lookup"><span data-stu-id="726a3-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="726a3-138">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="726a3-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="726a3-139">Ein Tensor, der die Filterskalierdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="726a3-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="726a3-140">Die erwarteten Dimensionen von `OutputScaleTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn eine Quantisierung pro Zeile erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="726a3-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="726a3-141">Dieser Skalierungswert wird zum Dequantisieren der Filterwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="726a3-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="726a3-142">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="726a3-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="726a3-143">Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="726a3-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="726a3-144">Die erwarteten Dimensionen von `OutputZeroPointTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn eine Quantisierung pro Zeile erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="726a3-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="726a3-145">Dieser Nullpunktwert wird zum Dequantisieren der Filterwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="726a3-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="726a3-146">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="726a3-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="726a3-147">Ein Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="726a3-147">A tensor to write the results to.</span></span> <span data-ttu-id="726a3-148">Die Dimensionen dieses Tensors sind `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="726a3-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="726a3-149">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="726a3-149">Availability</span></span>
<span data-ttu-id="726a3-150">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="726a3-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="726a3-151">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="726a3-151">Tensor constraints</span></span>
* <span data-ttu-id="726a3-152">*ATensor* und `AZeroPointTensor` müssen den gleichen *DataType aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="726a3-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="726a3-153">*BTensor* und `BZeroPointTensor` müssen den gleichen Datentyp *aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="726a3-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="726a3-154">*OutputTensor* und `OutputZeroPointTensor` müssen den gleichen Datentyp *aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="726a3-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="726a3-155">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="726a3-155">Tensor support</span></span>
| <span data-ttu-id="726a3-156">Tensor</span><span class="sxs-lookup"><span data-stu-id="726a3-156">Tensor</span></span> | <span data-ttu-id="726a3-157">Typ</span><span class="sxs-lookup"><span data-stu-id="726a3-157">Kind</span></span> | <span data-ttu-id="726a3-158">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="726a3-158">Supported dimension counts</span></span> | <span data-ttu-id="726a3-159">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="726a3-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="726a3-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="726a3-160">ATensor</span></span> | <span data-ttu-id="726a3-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="726a3-161">Input</span></span> | <span data-ttu-id="726a3-162">4</span><span class="sxs-lookup"><span data-stu-id="726a3-162">4</span></span> | <span data-ttu-id="726a3-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="726a3-163">INT8, UINT8</span></span> |
| <span data-ttu-id="726a3-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="726a3-164">AScaleTensor</span></span> | <span data-ttu-id="726a3-165">Eingabe</span><span class="sxs-lookup"><span data-stu-id="726a3-165">Input</span></span> | <span data-ttu-id="726a3-166">4</span><span class="sxs-lookup"><span data-stu-id="726a3-166">4</span></span> | <span data-ttu-id="726a3-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="726a3-167">FLOAT32</span></span> |
| <span data-ttu-id="726a3-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="726a3-168">AZeroPointTensor</span></span> | <span data-ttu-id="726a3-169">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="726a3-169">Optional input</span></span> | <span data-ttu-id="726a3-170">4</span><span class="sxs-lookup"><span data-stu-id="726a3-170">4</span></span> | <span data-ttu-id="726a3-171">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="726a3-171">INT8, UINT8</span></span> |
| <span data-ttu-id="726a3-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="726a3-172">BTensor</span></span> | <span data-ttu-id="726a3-173">Eingabe</span><span class="sxs-lookup"><span data-stu-id="726a3-173">Input</span></span> | <span data-ttu-id="726a3-174">4</span><span class="sxs-lookup"><span data-stu-id="726a3-174">4</span></span> | <span data-ttu-id="726a3-175">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="726a3-175">INT8, UINT8</span></span> |
| <span data-ttu-id="726a3-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="726a3-176">BScaleTensor</span></span> | <span data-ttu-id="726a3-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="726a3-177">Input</span></span> | <span data-ttu-id="726a3-178">4</span><span class="sxs-lookup"><span data-stu-id="726a3-178">4</span></span> | <span data-ttu-id="726a3-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="726a3-179">FLOAT32</span></span> |
| <span data-ttu-id="726a3-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="726a3-180">BZeroPointTensor</span></span> | <span data-ttu-id="726a3-181">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="726a3-181">Optional input</span></span> | <span data-ttu-id="726a3-182">4</span><span class="sxs-lookup"><span data-stu-id="726a3-182">4</span></span> | <span data-ttu-id="726a3-183">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="726a3-183">INT8, UINT8</span></span> |
| <span data-ttu-id="726a3-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="726a3-184">OutputScaleTensor</span></span> | <span data-ttu-id="726a3-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="726a3-185">Input</span></span> | <span data-ttu-id="726a3-186">4</span><span class="sxs-lookup"><span data-stu-id="726a3-186">4</span></span> | <span data-ttu-id="726a3-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="726a3-187">FLOAT32</span></span> |
| <span data-ttu-id="726a3-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="726a3-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="726a3-189">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="726a3-189">Optional input</span></span> | <span data-ttu-id="726a3-190">4</span><span class="sxs-lookup"><span data-stu-id="726a3-190">4</span></span> | <span data-ttu-id="726a3-191">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="726a3-191">INT8, UINT8</span></span> |
| <span data-ttu-id="726a3-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="726a3-192">OutputTensor</span></span> | <span data-ttu-id="726a3-193">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="726a3-193">Output</span></span> | <span data-ttu-id="726a3-194">4</span><span class="sxs-lookup"><span data-stu-id="726a3-194">4</span></span> | <span data-ttu-id="726a3-195">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="726a3-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="726a3-196">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="726a3-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="726a3-197">**Header**</span><span class="sxs-lookup"><span data-stu-id="726a3-197">**Header**</span></span> | <span data-ttu-id="726a3-198">directml.h</span><span class="sxs-lookup"><span data-stu-id="726a3-198">directml.h</span></span> |