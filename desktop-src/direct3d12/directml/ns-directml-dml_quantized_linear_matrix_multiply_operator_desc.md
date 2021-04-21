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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803571"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="49a5c-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="49a5c-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="49a5c-105">Führt eine Matrixmultiplikationsfunktion für quantisierte Daten aus.</span><span class="sxs-lookup"><span data-stu-id="49a5c-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="49a5c-106">Dieser Operator entspricht mathematisch der Dequantisierung der Eingaben, der anschließenden Matrixmultiplikation und der anschließenden Quantisierung der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="49a5c-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="49a5c-107">Dieser Operator erfordert, dass die Matrix-Multiplikationseingabe-Tensoren 4D sind, die als formatiert `{ BatchCount, ChannelCount, Height, Width }` sind.</span><span class="sxs-lookup"><span data-stu-id="49a5c-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="49a5c-108">Der Matrixmultiplikationsoperator führt BatchCount \* ChannelCount anzahl unabhängiger Matrixmultiplikationen aus.</span><span class="sxs-lookup"><span data-stu-id="49a5c-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="49a5c-109">Wenn *ATensor* z. *B. Größen* von `{ BatchCount, ChannelCount, M, K }` und *BTensor* *größen* von `{ BatchCount, ChannelCount, K, N }` und *OutputTensor* *Größen* von aufweist, führt `{ BatchCount, ChannelCount, M, N }` der Multiplikationsoperator der Matrix BatchCount \* ChannelCount unabhängige Matrixmultiplikationen der Dimensionen {M,K} x {K,N} = {M,N} aus.</span><span class="sxs-lookup"><span data-stu-id="49a5c-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="49a5c-110">Dequantize-Funktion</span><span class="sxs-lookup"><span data-stu-id="49a5c-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="49a5c-111">Quantize-Funktion</span><span class="sxs-lookup"><span data-stu-id="49a5c-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="49a5c-112">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="49a5c-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="49a5c-113">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="49a5c-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="49a5c-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="49a5c-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="49a5c-115">Member</span><span class="sxs-lookup"><span data-stu-id="49a5c-115">Members</span></span>

`ATensor`

<span data-ttu-id="49a5c-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="49a5c-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="49a5c-117">Ein Tensor, der die A-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="49a5c-117">A tensor containing the A data.</span></span> <span data-ttu-id="49a5c-118">Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, M, K }` sein.</span><span class="sxs-lookup"><span data-stu-id="49a5c-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="49a5c-119">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="49a5c-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="49a5c-120">Ein Tensor, der die ATensor-Skalierungsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="49a5c-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="49a5c-121">Die erwarteten Dimensionen von `AScaleTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn die Quantisierung pro Zeile erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="49a5c-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="49a5c-122">Diese Skalierungswerte werden zum Dequantisieren der A-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="49a5c-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="49a5c-123">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="49a5c-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="49a5c-124">Ein optionaler Tensor, der die Nullpunktdaten von *ATensor* enthält.</span><span class="sxs-lookup"><span data-stu-id="49a5c-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="49a5c-125">Die erwarteten Dimensionen von AZeroPointTensor sind `{ 1, 1, 1, 1 }` , wenn eine Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn eine Quantisierung pro Zeile erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="49a5c-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="49a5c-126">Diese Nullpunktwerte werden zum Dequantisieren der ATensor-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="49a5c-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="49a5c-127">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="49a5c-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="49a5c-128">Ein Tensor, der die B-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="49a5c-128">A tensor containing the B data.</span></span> <span data-ttu-id="49a5c-129">Die Dimensionen dieses Tensors sollten `{ BatchCount, ChannelCount, K, N }` sein.</span><span class="sxs-lookup"><span data-stu-id="49a5c-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="49a5c-130">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="49a5c-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="49a5c-131">Ein Tensor, der die *BTensor-Skalierungsdaten* enthält.</span><span class="sxs-lookup"><span data-stu-id="49a5c-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="49a5c-132">Die erwarteten Dimensionen von `BScaleTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, 1, N }` wenn eine Spaltenquantisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="49a5c-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="49a5c-133">Diese Skalierungswerte werden zum Dequantisieren der *BTensor-Werte* verwendet.</span><span class="sxs-lookup"><span data-stu-id="49a5c-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="49a5c-134">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="49a5c-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="49a5c-135">Ein optionaler Tensor, der die Nullpunktdaten von *BTensor* enthält.</span><span class="sxs-lookup"><span data-stu-id="49a5c-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="49a5c-136">Die erwarteten Dimensionen von `BZeroPointTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, 1, N }` wenn eine Spaltenquantisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="49a5c-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="49a5c-137">Diese Nullpunktwerte werden zum Dequantisieren der *BTensor-Werte* verwendet.</span><span class="sxs-lookup"><span data-stu-id="49a5c-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="49a5c-138">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="49a5c-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="49a5c-139">Ein Tensor, der die Filterskalierdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="49a5c-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="49a5c-140">Die erwarteten Dimensionen von `OutputScaleTensor` sind , wenn eine `{ 1, 1, 1, 1 }` Tensorquantisierung erforderlich ist, oder `{ 1, 1, M, 1 }` wenn die Quantisierung pro Zeile erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="49a5c-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="49a5c-141">Dieser Skalierungswert wird zum Dequantisieren der Filterwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="49a5c-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="49a5c-142">Typ: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="49a5c-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="49a5c-143">Ein optionaler Tensor, der die Nullpunktdaten des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="49a5c-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="49a5c-144">Die erwarteten Dimensionen von sind `OutputZeroPointTensor` , wenn eine Tensorquantisierung erforderlich ist oder wenn eine `{ 1, 1, 1, 1 }` Quantisierung pro Zeile erforderlich `{ 1, 1, M, 1 }` ist.</span><span class="sxs-lookup"><span data-stu-id="49a5c-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="49a5c-145">Dieser Nullpunktwert wird zum Dequantisieren der Filterwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="49a5c-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="49a5c-146">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="49a5c-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="49a5c-147">Ein Tensor, in den die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="49a5c-147">A tensor to write the results to.</span></span> <span data-ttu-id="49a5c-148">Die Dimensionen dieses Tensors sind `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="49a5c-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="49a5c-149">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="49a5c-149">Availability</span></span>
<span data-ttu-id="49a5c-150">Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="49a5c-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="49a5c-151">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="49a5c-151">Tensor constraints</span></span>
* <span data-ttu-id="49a5c-152">*ATensor und* `AZeroPointTensor` müssen den gleichen Datentyp *haben.*</span><span class="sxs-lookup"><span data-stu-id="49a5c-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="49a5c-153">*BTensor und* `BZeroPointTensor` müssen den gleichen Datentyp *haben.*</span><span class="sxs-lookup"><span data-stu-id="49a5c-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="49a5c-154">*OutputTensor* und `OutputZeroPointTensor` müssen den gleichen Datentyp *haben.*</span><span class="sxs-lookup"><span data-stu-id="49a5c-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="49a5c-155">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="49a5c-155">Tensor support</span></span>
| <span data-ttu-id="49a5c-156">Tensor</span><span class="sxs-lookup"><span data-stu-id="49a5c-156">Tensor</span></span> | <span data-ttu-id="49a5c-157">Typ</span><span class="sxs-lookup"><span data-stu-id="49a5c-157">Kind</span></span> | <span data-ttu-id="49a5c-158">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="49a5c-158">Supported dimension counts</span></span> | <span data-ttu-id="49a5c-159">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="49a5c-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="49a5c-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="49a5c-160">ATensor</span></span> | <span data-ttu-id="49a5c-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="49a5c-161">Input</span></span> | <span data-ttu-id="49a5c-162">4</span><span class="sxs-lookup"><span data-stu-id="49a5c-162">4</span></span> | <span data-ttu-id="49a5c-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="49a5c-163">INT8, UINT8</span></span> |
| <span data-ttu-id="49a5c-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="49a5c-164">AScaleTensor</span></span> | <span data-ttu-id="49a5c-165">Eingabe</span><span class="sxs-lookup"><span data-stu-id="49a5c-165">Input</span></span> | <span data-ttu-id="49a5c-166">4</span><span class="sxs-lookup"><span data-stu-id="49a5c-166">4</span></span> | <span data-ttu-id="49a5c-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="49a5c-167">FLOAT32</span></span> |
| <span data-ttu-id="49a5c-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="49a5c-168">AZeroPointTensor</span></span> | <span data-ttu-id="49a5c-169">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="49a5c-169">Optional input</span></span> | <span data-ttu-id="49a5c-170">4</span><span class="sxs-lookup"><span data-stu-id="49a5c-170">4</span></span> | <span data-ttu-id="49a5c-171">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="49a5c-171">INT8, UINT8</span></span> |
| <span data-ttu-id="49a5c-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="49a5c-172">BTensor</span></span> | <span data-ttu-id="49a5c-173">Eingabe</span><span class="sxs-lookup"><span data-stu-id="49a5c-173">Input</span></span> | <span data-ttu-id="49a5c-174">4</span><span class="sxs-lookup"><span data-stu-id="49a5c-174">4</span></span> | <span data-ttu-id="49a5c-175">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="49a5c-175">INT8, UINT8</span></span> |
| <span data-ttu-id="49a5c-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="49a5c-176">BScaleTensor</span></span> | <span data-ttu-id="49a5c-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="49a5c-177">Input</span></span> | <span data-ttu-id="49a5c-178">4</span><span class="sxs-lookup"><span data-stu-id="49a5c-178">4</span></span> | <span data-ttu-id="49a5c-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="49a5c-179">FLOAT32</span></span> |
| <span data-ttu-id="49a5c-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="49a5c-180">BZeroPointTensor</span></span> | <span data-ttu-id="49a5c-181">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="49a5c-181">Optional input</span></span> | <span data-ttu-id="49a5c-182">4</span><span class="sxs-lookup"><span data-stu-id="49a5c-182">4</span></span> | <span data-ttu-id="49a5c-183">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="49a5c-183">INT8, UINT8</span></span> |
| <span data-ttu-id="49a5c-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="49a5c-184">OutputScaleTensor</span></span> | <span data-ttu-id="49a5c-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="49a5c-185">Input</span></span> | <span data-ttu-id="49a5c-186">4</span><span class="sxs-lookup"><span data-stu-id="49a5c-186">4</span></span> | <span data-ttu-id="49a5c-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="49a5c-187">FLOAT32</span></span> |
| <span data-ttu-id="49a5c-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="49a5c-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="49a5c-189">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="49a5c-189">Optional input</span></span> | <span data-ttu-id="49a5c-190">4</span><span class="sxs-lookup"><span data-stu-id="49a5c-190">4</span></span> | <span data-ttu-id="49a5c-191">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="49a5c-191">INT8, UINT8</span></span> |
| <span data-ttu-id="49a5c-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="49a5c-192">OutputTensor</span></span> | <span data-ttu-id="49a5c-193">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="49a5c-193">Output</span></span> | <span data-ttu-id="49a5c-194">4</span><span class="sxs-lookup"><span data-stu-id="49a5c-194">4</span></span> | <span data-ttu-id="49a5c-195">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="49a5c-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="49a5c-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49a5c-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="49a5c-197">**Header**</span><span class="sxs-lookup"><span data-stu-id="49a5c-197">**Header**</span></span> | <span data-ttu-id="49a5c-198">directml.h</span><span class="sxs-lookup"><span data-stu-id="49a5c-198">directml.h</span></span> |