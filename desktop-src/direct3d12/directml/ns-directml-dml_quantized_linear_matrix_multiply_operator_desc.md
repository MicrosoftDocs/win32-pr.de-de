---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Führt eine Matrix Multiplikations Funktion für quantifizierte Daten aus. Dieser Operator entspricht mathematisch der dequantifizierung der Eingaben, der anschließende Durchführung der Matrix Multiplikation und der anschließenden Quantifizierung der Ausgabe.
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
ms.openlocfilehash: d0b20a37bca6ddf6083b116b53290a6b6b2084f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106366358"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="277f9-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="277f9-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="277f9-105">Führt eine Matrix Multiplikations Funktion für quantifizierte Daten aus.</span><span class="sxs-lookup"><span data-stu-id="277f9-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="277f9-106">Dieser Operator entspricht mathematisch der dequantifizierung der Eingaben, der anschließende Durchführung der Matrix Multiplikation und der anschließenden Quantifizierung der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="277f9-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="277f9-107">Für diesen Operator ist es erforderlich, dass die Eingabe-Tensoren der Matrix als 4D-Format multipliziert werden `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="277f9-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="277f9-108">Der Matrix Multiplikations Operator führt die BatchCount \* ChannelCount-Anzahl unabhängiger Matrix Multiplikationen durch.</span><span class="sxs-lookup"><span data-stu-id="277f9-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="277f9-109">Wenn *atensor* z. b. *Größen* von hat `{ BatchCount, ChannelCount, M, K }` und *btensor* die *Größe* hat `{ BatchCount, ChannelCount, K, N }` und *outputtensor* über *Größen* von verfügt `{ BatchCount, ChannelCount, M, N }` , führt der Matrix Multiplikations Operator BatchCount \* ChannelCount unabhängige Matrix Multiplikationen der Dimensionen {m, K} x {K, n} = {M, n} aus.</span><span class="sxs-lookup"><span data-stu-id="277f9-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="277f9-110">Funktion "Debug"</span><span class="sxs-lookup"><span data-stu-id="277f9-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="277f9-111">Quantize-Funktion</span><span class="sxs-lookup"><span data-stu-id="277f9-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="277f9-112">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="277f9-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="277f9-113">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="277f9-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="277f9-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="277f9-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="277f9-115">Member</span><span class="sxs-lookup"><span data-stu-id="277f9-115">Members</span></span>

`ATensor`

<span data-ttu-id="277f9-116">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="277f9-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="277f9-117">Ein tensorflow, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="277f9-117">A tensor containing the A data.</span></span> <span data-ttu-id="277f9-118">Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="277f9-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="277f9-119">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="277f9-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="277f9-120">Ein tensorflow, der die Daten der atensor-Skala enthält.</span><span class="sxs-lookup"><span data-stu-id="277f9-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="277f9-121">Die erwarteten Dimensionen von `AScaleTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, M, 1 }` Wenn die pro-Zeilen-Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="277f9-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="277f9-122">Diese Skalierungs Werte werden zum dequantifialisieren der Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="277f9-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="277f9-123">Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="277f9-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="277f9-124">Ein optionaler tensorflow, der die Daten des *atensor* -NULL-Punkts enthält.</span><span class="sxs-lookup"><span data-stu-id="277f9-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="277f9-125">Die erwarteten Dimensionen von azeropointtensor sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist oder `{ 1, 1, M, 1 }` Wenn pro Zeilen-Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="277f9-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="277f9-126">Diese nullpunktwerte werden zum decomieren der atensor-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="277f9-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="277f9-127">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="277f9-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="277f9-128">Ein tensorflow, der die B-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="277f9-128">A tensor containing the B data.</span></span> <span data-ttu-id="277f9-129">Diese Tensor-Dimensionen sollten lauten `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="277f9-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="277f9-130">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="277f9-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="277f9-131">Ein tensorflow, der die Daten der *btensor* -Skalierung enthält.</span><span class="sxs-lookup"><span data-stu-id="277f9-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="277f9-132">Die erwarteten Dimensionen von `BScaleTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, 1, N }` Wenn pro Spalten Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="277f9-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="277f9-133">Diese Skalierungs Werte werden zum dequantifialisieren der *btensor* -Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="277f9-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="277f9-134">Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="277f9-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="277f9-135">Ein optionaler tensorflow, der die Daten des *btensor* -NULL-Punkts enthält.</span><span class="sxs-lookup"><span data-stu-id="277f9-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="277f9-136">Die erwarteten Dimensionen von `BZeroPointTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, 1, N }` Wenn pro Spalten Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="277f9-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="277f9-137">Diese nullpunktwerte werden zum decomieren der *btensor* -Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="277f9-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="277f9-138">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="277f9-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="277f9-139">Ein tensorflow, der die Filter Skalierungs Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="277f9-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="277f9-140">Die erwarteten Dimensionen von `OutputScaleTensor` sind `{ 1, 1, 1, 1 }` , wenn pro tensorflow-Quantifizierung erforderlich ist, oder, `{ 1, 1, M, 1 }` Wenn die pro-Zeilen-Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="277f9-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="277f9-141">Dieser Skalierungs Wert wird zum dequantifialisieren der Filter Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="277f9-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="277f9-142">Typ: _Maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="277f9-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="277f9-143">Ein optionaler tensorflow, der die Filter-NULL-Punktdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="277f9-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="277f9-144">Die erwarteten Dimensionen von `OutputZeroPointTensor` sind, `{ 1, 1, 1, 1 }` Wenn pro tensorflow-Quantifizierung erforderlich ist oder `{ 1, 1, M, 1 }` Wenn pro Zeilen-Quantifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="277f9-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="277f9-145">Dieser Nullpunktwert wird zum decomieren der Filter Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="277f9-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="277f9-146">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="277f9-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="277f9-147">Ein tensorflow, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="277f9-147">A tensor to write the results to.</span></span> <span data-ttu-id="277f9-148">Die Dimensionen dieses Mandanten sind `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="277f9-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="277f9-149">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="277f9-149">Availability</span></span>
<span data-ttu-id="277f9-150">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="277f9-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="277f9-151">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="277f9-151">Tensor constraints</span></span>
* <span data-ttu-id="277f9-152">*Atensor* und `AZeroPointTensor` muss denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="277f9-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="277f9-153">*Btensor* und `BZeroPointTensor` muss denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="277f9-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="277f9-154">*Outputtensor* und `OutputZeroPointTensor` muss denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="277f9-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="277f9-155">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="277f9-155">Tensor support</span></span>
| <span data-ttu-id="277f9-156">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="277f9-156">Tensor</span></span> | <span data-ttu-id="277f9-157">Typ</span><span class="sxs-lookup"><span data-stu-id="277f9-157">Kind</span></span> | <span data-ttu-id="277f9-158">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="277f9-158">Supported dimension counts</span></span> | <span data-ttu-id="277f9-159">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="277f9-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="277f9-160">Atensor</span><span class="sxs-lookup"><span data-stu-id="277f9-160">ATensor</span></span> | <span data-ttu-id="277f9-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="277f9-161">Input</span></span> | <span data-ttu-id="277f9-162">4</span><span class="sxs-lookup"><span data-stu-id="277f9-162">4</span></span> | <span data-ttu-id="277f9-163">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="277f9-163">INT8, UINT8</span></span> |
| <span data-ttu-id="277f9-164">Ascaletensor</span><span class="sxs-lookup"><span data-stu-id="277f9-164">AScaleTensor</span></span> | <span data-ttu-id="277f9-165">Eingabe</span><span class="sxs-lookup"><span data-stu-id="277f9-165">Input</span></span> | <span data-ttu-id="277f9-166">4</span><span class="sxs-lookup"><span data-stu-id="277f9-166">4</span></span> | <span data-ttu-id="277f9-167">Float32</span><span class="sxs-lookup"><span data-stu-id="277f9-167">FLOAT32</span></span> |
| <span data-ttu-id="277f9-168">Azeropointtensor</span><span class="sxs-lookup"><span data-stu-id="277f9-168">AZeroPointTensor</span></span> | <span data-ttu-id="277f9-169">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="277f9-169">Optional input</span></span> | <span data-ttu-id="277f9-170">4</span><span class="sxs-lookup"><span data-stu-id="277f9-170">4</span></span> | <span data-ttu-id="277f9-171">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="277f9-171">INT8, UINT8</span></span> |
| <span data-ttu-id="277f9-172">Btensor</span><span class="sxs-lookup"><span data-stu-id="277f9-172">BTensor</span></span> | <span data-ttu-id="277f9-173">Eingabe</span><span class="sxs-lookup"><span data-stu-id="277f9-173">Input</span></span> | <span data-ttu-id="277f9-174">4</span><span class="sxs-lookup"><span data-stu-id="277f9-174">4</span></span> | <span data-ttu-id="277f9-175">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="277f9-175">INT8, UINT8</span></span> |
| <span data-ttu-id="277f9-176">Bscaletensor</span><span class="sxs-lookup"><span data-stu-id="277f9-176">BScaleTensor</span></span> | <span data-ttu-id="277f9-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="277f9-177">Input</span></span> | <span data-ttu-id="277f9-178">4</span><span class="sxs-lookup"><span data-stu-id="277f9-178">4</span></span> | <span data-ttu-id="277f9-179">Float32</span><span class="sxs-lookup"><span data-stu-id="277f9-179">FLOAT32</span></span> |
| <span data-ttu-id="277f9-180">Bzeropointtensor</span><span class="sxs-lookup"><span data-stu-id="277f9-180">BZeroPointTensor</span></span> | <span data-ttu-id="277f9-181">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="277f9-181">Optional input</span></span> | <span data-ttu-id="277f9-182">4</span><span class="sxs-lookup"><span data-stu-id="277f9-182">4</span></span> | <span data-ttu-id="277f9-183">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="277f9-183">INT8, UINT8</span></span> |
| <span data-ttu-id="277f9-184">Outputscaletensor</span><span class="sxs-lookup"><span data-stu-id="277f9-184">OutputScaleTensor</span></span> | <span data-ttu-id="277f9-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="277f9-185">Input</span></span> | <span data-ttu-id="277f9-186">4</span><span class="sxs-lookup"><span data-stu-id="277f9-186">4</span></span> | <span data-ttu-id="277f9-187">Float32</span><span class="sxs-lookup"><span data-stu-id="277f9-187">FLOAT32</span></span> |
| <span data-ttu-id="277f9-188">Outputzeropointtensor</span><span class="sxs-lookup"><span data-stu-id="277f9-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="277f9-189">Optionale Eingabe</span><span class="sxs-lookup"><span data-stu-id="277f9-189">Optional input</span></span> | <span data-ttu-id="277f9-190">4</span><span class="sxs-lookup"><span data-stu-id="277f9-190">4</span></span> | <span data-ttu-id="277f9-191">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="277f9-191">INT8, UINT8</span></span> |
| <span data-ttu-id="277f9-192">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="277f9-192">OutputTensor</span></span> | <span data-ttu-id="277f9-193">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="277f9-193">Output</span></span> | <span data-ttu-id="277f9-194">4</span><span class="sxs-lookup"><span data-stu-id="277f9-194">4</span></span> | <span data-ttu-id="277f9-195">Int8, Uint8</span><span class="sxs-lookup"><span data-stu-id="277f9-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="277f9-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="277f9-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="277f9-197">**Header**</span><span class="sxs-lookup"><span data-stu-id="277f9-197">**Header**</span></span> | <span data-ttu-id="277f9-198">directml. h</span><span class="sxs-lookup"><span data-stu-id="277f9-198">directml.h</span></span> |