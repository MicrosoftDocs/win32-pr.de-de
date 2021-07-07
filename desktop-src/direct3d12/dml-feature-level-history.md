---
title: DirectML-Verlauf auf Featureebene
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 3ddb2eec80448b8119bf2d990afbb998f212db26
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282549"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="1131c-103">DirectML-Verlauf auf Featureebene</span><span class="sxs-lookup"><span data-stu-id="1131c-103">DirectML feature level history</span></span>

<span data-ttu-id="1131c-104">Informationen zum allgemeinen DirectML-Versionsverlauf finden Sie unter [DirectML-Versionsverlauf.](./dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="1131c-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_4_0"></a><span data-ttu-id="1131c-105">DML_FEATURE_LEVEL_4_0</span><span class="sxs-lookup"><span data-stu-id="1131c-105">DML_FEATURE_LEVEL_4_0</span></span>

<span data-ttu-id="1131c-106">Eingeführt in DirectML Version 1.6.0.</span><span class="sxs-lookup"><span data-stu-id="1131c-106">Introduced in DirectML version 1.6.0.</span></span>

<span data-ttu-id="1131c-107">Unterstützung für die folgenden Operatortypen wurde hinzugefügt, die in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="1131c-107">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1131c-108">Für jede Operatortypkonstante stellt dieses Thema einen Link zur entsprechenden -Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="1131c-108">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="1131c-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span><span class="sxs-lookup"><span data-stu-id="1131c-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span></span>
* <span data-ttu-id="1131c-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="1131c-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span></span>
* <span data-ttu-id="1131c-111">**DML_OPERATOR_ROI_ALIGN1**</span><span class="sxs-lookup"><span data-stu-id="1131c-111">**DML_OPERATOR_ROI_ALIGN1**</span></span>

<span data-ttu-id="1131c-112">Erweiterte Unterstützung für Datentyp und Dimensionsanzahl für die folgenden Operatoren, die in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="1131c-112">Extended data type and dimension count support for the following operators, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1131c-113">Ausführliche Informationen zur spezifischen Unterstützung, die in [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level)hinzugefügt wurde, finden Sie im Strukturthema der einzelnen Operatoren.</span><span class="sxs-lookup"><span data-stu-id="1131c-113">For details on the specific support added in [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), see each operator's structure topic.</span></span>

* <span data-ttu-id="1131c-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="1131c-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="1131c-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="1131c-116">**DML_OPERATOR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="1131c-116">**DML_OPERATOR_CONVOLUTION**</span></span>
* <span data-ttu-id="1131c-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="1131c-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="1131c-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="1131c-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="1131c-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="1131c-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="1131c-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="1131c-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="1131c-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="1131c-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="1131c-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="1131c-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="1131c-123">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="1131c-123">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="1131c-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="1131c-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="1131c-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="1131c-126">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="1131c-126">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="1131c-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="1131c-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>
* <span data-ttu-id="1131c-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1131c-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="1131c-129">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="1131c-129">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="1131c-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="1131c-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="1131c-131">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="1131c-131">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="1131c-132">Eingeführt in DirectML Version 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="1131c-132">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="1131c-133">Unterstützung für die folgenden Operatortypen wurde hinzugefügt, die in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="1131c-133">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1131c-134">Für jede Operatortypkonstante stellt dieses Thema einen Link zur entsprechenden -Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="1131c-134">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="1131c-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="1131c-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="1131c-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="1131c-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="1131c-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="1131c-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="1131c-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="1131c-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="1131c-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="1131c-141">Die maximale Anzahl unterstützter Dimensionen für die folgenden Operatoren wurde von 4 auf 8 erhöht.</span><span class="sxs-lookup"><span data-stu-id="1131c-141">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="1131c-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="1131c-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="1131c-143">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="1131c-143">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="1131c-144">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="1131c-144">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="1131c-145">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="1131c-145">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="1131c-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="1131c-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="1131c-147">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="1131c-147">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="1131c-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="1131c-149">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-149">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="1131c-150">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="1131c-150">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="1131c-151">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="1131c-151">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="1131c-152">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="1131c-152">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="1131c-153">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="1131c-153">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="1131c-154">Eingeführt in DirectML Version 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="1131c-154">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="1131c-155">Unterstützung für die folgenden Operatortypen wurde hinzugefügt, die in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="1131c-155">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1131c-156">Für jede Operatortypkonstante stellt dieses Thema einen Link zur entsprechenden -Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="1131c-156">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="1131c-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="1131c-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="1131c-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="1131c-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="1131c-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="1131c-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="1131c-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="1131c-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="1131c-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="1131c-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="1131c-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="1131c-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="1131c-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="1131c-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="1131c-164">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="1131c-164">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="1131c-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="1131c-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="1131c-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="1131c-168">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="1131c-168">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="1131c-169">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="1131c-169">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="1131c-170">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-170">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="1131c-171">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1131c-171">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="1131c-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="1131c-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="1131c-173">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="1131c-173">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="1131c-174">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="1131c-174">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="1131c-175">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="1131c-175">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="1131c-176">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="1131c-176">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="1131c-177">Die folgenden Erweiterungen wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1131c-177">Added the following enhancements.</span></span>

* <span data-ttu-id="1131c-178">Die maximale Anzahl von Tensordimensionen wurde von 5 auf 8 erhöht.</span><span class="sxs-lookup"><span data-stu-id="1131c-178">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="1131c-179">Weitere Informationen finden Sie [unter DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1131c-179">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="1131c-180">Den folgenden Operatoren wurde zusätzliche Unterstützung für integer-Datentypen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1131c-180">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="1131c-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="1131c-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="1131c-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="1131c-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="1131c-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** und **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="1131c-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="1131c-184">**DML_OPERATOR_REDUCE** bei Verwendung von **DML_REDUCE_FUNCTION_ARGMIN** oder **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="1131c-184">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="1131c-185">Die folgenden 64-Bit-Datentypen wurden hinzugefügt und werden von Select-Operatoren unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1131c-185">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="1131c-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="1131c-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="1131c-187">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="1131c-187">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="1131c-188">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="1131c-188">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="1131c-189">Veraltete Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="1131c-189">Deprecated functionality.</span></span>

* <span data-ttu-id="1131c-190">**DML_REDUCE_FUNCTION_ARGMAX** und **DML_REDUCE_FUNCTION_ARGMIN** sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="1131c-190">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="1131c-191">Sie sollten die eigenständigen **operatoren DML_OPERATOR_ARGMIN** und **DML_OPERATOR_ARGMAX** an ihrer Stelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="1131c-191">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="1131c-192">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="1131c-192">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="1131c-193">Eingeführt in DirectML Version 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="1131c-193">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="1131c-194">Die folgenden APIs wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1131c-194">Added the following APIs.</span></span>

* [<span data-ttu-id="1131c-195">IDMLDevice1-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1131c-195">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="1131c-196">Operatordiagrammunterstützung (siehe [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="1131c-196">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="1131c-197">Unterstützung für die folgenden Operatortypen wurde hinzugefügt, die in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="1131c-197">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1131c-198">Für jede Operatortypkonstante stellt dieses Thema einen Link zur entsprechenden -Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="1131c-198">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="1131c-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="1131c-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="1131c-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="1131c-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="1131c-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="1131c-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="1131c-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="1131c-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="1131c-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="1131c-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="1131c-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="1131c-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="1131c-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="1131c-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="1131c-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="1131c-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="1131c-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="1131c-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="1131c-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="1131c-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="1131c-209">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="1131c-209">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="1131c-210">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="1131c-210">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="1131c-211">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="1131c-211">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="1131c-212">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="1131c-212">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="1131c-213">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="1131c-213">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="1131c-214">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="1131c-214">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="1131c-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="1131c-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="1131c-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="1131c-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="1131c-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="1131c-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="1131c-218">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="1131c-218">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="1131c-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="1131c-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="1131c-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1131c-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="1131c-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="1131c-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="1131c-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="1131c-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="1131c-223">Die folgenden Erweiterungen wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1131c-223">Added the following enhancements.</span></span>

* <span data-ttu-id="1131c-224">Den folgenden Operatoren wurde zusätzliche Unterstützung für integer-Datentypen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1131c-224">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="1131c-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="1131c-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="1131c-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="1131c-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="1131c-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="1131c-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="1131c-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="1131c-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="1131c-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="1131c-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="1131c-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="1131c-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="1131c-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="1131c-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="1131c-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="1131c-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="1131c-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="1131c-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="1131c-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="1131c-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="1131c-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="1131c-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="1131c-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1131c-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="1131c-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="1131c-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="1131c-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="1131c-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="1131c-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="1131c-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="1131c-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="1131c-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="1131c-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="1131c-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="1131c-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="1131c-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="1131c-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="1131c-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="1131c-244">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="1131c-244">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="1131c-245">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="1131c-245">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="1131c-246">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="1131c-246">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="1131c-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="1131c-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="1131c-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="1131c-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="1131c-249">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="1131c-249">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="1131c-250">**DML_OPERATOR_TOP_K** und **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="1131c-250">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="1131c-251">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="1131c-251">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="1131c-252">**DML_OPERATOR_REDUCE**, wenn Sie eine der folgenden Reduce-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1131c-252">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="1131c-253">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="1131c-253">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="1131c-254">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="1131c-254">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="1131c-255">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="1131c-255">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="1131c-256">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="1131c-256">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="1131c-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1131c-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="1131c-258">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="1131c-258">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="1131c-259">Gelockerte Tensorformeinschränkungen für **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="1131c-259">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="1131c-260">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="1131c-260">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="1131c-261">Eingeführt in DirectML Version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="1131c-261">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="1131c-262">Die folgenden APIs wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1131c-262">Added the following APIs.</span></span>
* [<span data-ttu-id="1131c-263">DMLCreateDevice1-Funktion</span><span class="sxs-lookup"><span data-stu-id="1131c-263">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="1131c-264">DML_FEATURE_LEVEL-Enumeration</span><span class="sxs-lookup"><span data-stu-id="1131c-264">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="1131c-265">Abfragen auf Featureebene (siehe [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="1131c-265">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="1131c-266">Unterstützung für die folgenden Operatortypen wurde hinzugefügt, die in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="1131c-266">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1131c-267">Für jede Operatortypkonstante stellt dieses Thema einen Link zur entsprechenden -Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="1131c-267">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="1131c-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="1131c-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="1131c-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="1131c-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="1131c-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="1131c-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="1131c-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="1131c-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="1131c-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="1131c-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="1131c-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="1131c-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="1131c-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="1131c-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="1131c-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="1131c-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="1131c-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="1131c-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="1131c-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="1131c-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="1131c-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="1131c-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="1131c-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="1131c-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="1131c-280">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="1131c-280">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="1131c-281">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="1131c-281">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="1131c-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="1131c-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="1131c-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="1131c-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="1131c-284">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="1131c-284">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="1131c-285">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="1131c-285">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="1131c-286">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="1131c-286">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="1131c-287">Die folgenden Erweiterungen wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1131c-287">Added the following enhancements.</span></span>

* <span data-ttu-id="1131c-288">Wenn Sie eine Eingaberessource für die Verteilung eines [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)binden, ist es jetzt zulässig, eine Ressource mit [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) bereitzustellen (zusätzlich zu **D3D12_HEAP_TYPE_DEFAULT**), solange auch die entsprechenden Heapeigenschaften festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="1131c-288">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="1131c-289">Weitere Informationen finden Sie [unter Binden in DirectML.](./dml-binding.md)</span><span class="sxs-lookup"><span data-stu-id="1131c-289">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="1131c-290">Die folgenden logischen booleschen Operatoren unterstützen jetzt **UINT8-Ausgabe** tensors zusätzlich zur vorhandenen Unterstützung für **UINT32.**</span><span class="sxs-lookup"><span data-stu-id="1131c-290">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="1131c-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="1131c-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="1131c-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="1131c-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="1131c-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="1131c-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="1131c-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="1131c-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="1131c-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="1131c-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="1131c-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="1131c-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="1131c-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="1131c-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="1131c-298">5D-Aktivierungsfunktionen unterstützen jetzt die Verwendung von Schritten bei ihren Eingabe- und Ausgabe-Tensoren.</span><span class="sxs-lookup"><span data-stu-id="1131c-298">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="1131c-299">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="1131c-299">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="1131c-300">Die Funktionsebene, in der DirectML eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1131c-300">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="1131c-301">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1131c-301">See also</span></span>

* [<span data-ttu-id="1131c-302">DirectML-Versionsverlauf</span><span class="sxs-lookup"><span data-stu-id="1131c-302">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="1131c-303">DML_FEATURE_LEVEL Enumeration</span><span class="sxs-lookup"><span data-stu-id="1131c-303">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="1131c-304">DMLCreateDevice1-Funktion</span><span class="sxs-lookup"><span data-stu-id="1131c-304">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="1131c-305">DML_FEATURE_QUERY_FEATURE_LEVELS-Struktur</span><span class="sxs-lookup"><span data-stu-id="1131c-305">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
