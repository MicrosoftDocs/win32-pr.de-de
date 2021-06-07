---
title: DirectML-Verlauf auf Featureebene
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 1e5d9f8b0532b809bab617655694af68ba530430
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521205"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="c1289-103">DirectML-Verlauf auf Featureebene</span><span class="sxs-lookup"><span data-stu-id="c1289-103">DirectML feature level history</span></span>

<span data-ttu-id="c1289-104">Den allgemeinen DirectML-Versionsverlauf finden Sie unter [DirectML-Versionsverlauf.](./dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="c1289-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="c1289-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="c1289-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="c1289-106">Eingeführt in DirectML Version 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="c1289-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="c1289-107">Unterstützung für die folgenden Operatoren [wurde hinzugefügt.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="c1289-107">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="c1289-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="c1289-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="c1289-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c1289-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="c1289-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="c1289-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="c1289-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c1289-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="c1289-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="c1289-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="c1289-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c1289-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="c1289-114">Die maximale Anzahl unterstützter Dimensionen für die folgenden Operatoren wurde von 4 auf 8 erhöht.</span><span class="sxs-lookup"><span data-stu-id="c1289-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="c1289-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="c1289-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="c1289-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="c1289-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="c1289-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="c1289-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="c1289-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="c1289-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="c1289-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="c1289-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="c1289-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="c1289-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="c1289-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c1289-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="c1289-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c1289-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="c1289-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="c1289-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="c1289-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="c1289-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="c1289-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="c1289-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="c1289-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="c1289-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="c1289-127">Eingeführt in DirectML Version 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="c1289-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="c1289-128">Unterstützung für die folgenden Operatoren [wurde hinzugefügt.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="c1289-128">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="c1289-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="c1289-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="c1289-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="c1289-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="c1289-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="c1289-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="c1289-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="c1289-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="c1289-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="c1289-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="c1289-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="c1289-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="c1289-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="c1289-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="c1289-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="c1289-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="c1289-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c1289-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="c1289-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c1289-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="c1289-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c1289-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="c1289-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="c1289-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="c1289-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="c1289-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="c1289-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c1289-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="c1289-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c1289-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="c1289-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="c1289-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="c1289-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="c1289-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="c1289-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="c1289-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="c1289-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="c1289-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="c1289-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="c1289-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="c1289-149">Die folgenden Erweiterungen wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1289-149">Added the following enhancements.</span></span>

* <span data-ttu-id="c1289-150">Die maximale Anzahl von Tensordimensionen wurde von 5 auf 8 erhöht.</span><span class="sxs-lookup"><span data-stu-id="c1289-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="c1289-151">Siehe [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c1289-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="c1289-152">Den folgenden Operatoren wurde zusätzliche Unterstützung für ganzzahlige Datentypen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1289-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="c1289-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="c1289-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="c1289-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="c1289-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="c1289-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** und **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="c1289-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="c1289-156">**DML_OPERATOR_REDUCE** bei Verwendung **von** DML_REDUCE_FUNCTION_ARGMIN oder **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="c1289-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="c1289-157">Die folgenden 64-Bit-Datentypen wurden hinzugefügt und werden von select-Operatoren unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c1289-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="c1289-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="c1289-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="c1289-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="c1289-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="c1289-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="c1289-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="c1289-161">Veraltete Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="c1289-161">Deprecated functionality.</span></span>

* <span data-ttu-id="c1289-162">**DML_REDUCE_FUNCTION_ARGMAX** und **DML_REDUCE_FUNCTION_ARGMIN** sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="c1289-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="c1289-163">Sie sollten die eigenständigen DML_OPERATOR_ARGMIN **und** **DML_OPERATOR_ARGMAX** verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1289-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="c1289-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="c1289-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="c1289-165">Eingeführt in DirectML Version 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="c1289-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="c1289-166">Die folgenden APIs wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1289-166">Added the following APIs.</span></span>

* [<span data-ttu-id="c1289-167">IDMLDevice1-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c1289-167">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="c1289-168">Operatordiagrammunterstützung (siehe [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="c1289-168">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="c1289-169">Unterstützung für die folgenden Operatoren hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1289-169">Added support for the following operators.</span></span>

* <span data-ttu-id="c1289-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="c1289-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="c1289-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="c1289-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="c1289-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="c1289-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="c1289-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="c1289-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="c1289-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="c1289-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="c1289-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="c1289-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="c1289-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="c1289-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="c1289-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="c1289-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="c1289-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="c1289-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="c1289-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="c1289-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="c1289-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="c1289-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="c1289-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="c1289-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="c1289-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="c1289-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="c1289-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="c1289-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="c1289-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="c1289-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="c1289-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="c1289-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="c1289-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="c1289-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="c1289-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="c1289-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="c1289-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="c1289-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="c1289-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="c1289-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="c1289-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="c1289-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="c1289-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="c1289-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="c1289-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="c1289-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="c1289-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="c1289-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="c1289-194">Die folgenden Erweiterungen wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1289-194">Added the following enhancements.</span></span>

* <span data-ttu-id="c1289-195">Den folgenden Operatoren wurde zusätzliche Unterstützung für ganzzahlige Datentypen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1289-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="c1289-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="c1289-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="c1289-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="c1289-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="c1289-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="c1289-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="c1289-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="c1289-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="c1289-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="c1289-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="c1289-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="c1289-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="c1289-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="c1289-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="c1289-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="c1289-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="c1289-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="c1289-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="c1289-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="c1289-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="c1289-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="c1289-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="c1289-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="c1289-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="c1289-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="c1289-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="c1289-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="c1289-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="c1289-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="c1289-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="c1289-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="c1289-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="c1289-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="c1289-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="c1289-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="c1289-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="c1289-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="c1289-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="c1289-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="c1289-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="c1289-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="c1289-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="c1289-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="c1289-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="c1289-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="c1289-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="c1289-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="c1289-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="c1289-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="c1289-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="c1289-221">**DML_OPERATOR_TOP_K** und **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="c1289-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="c1289-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="c1289-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="c1289-223">**DML_OPERATOR_REDUCE**, wenn Sie eine der folgenden Reduce-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1289-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="c1289-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="c1289-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="c1289-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="c1289-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="c1289-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="c1289-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="c1289-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="c1289-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="c1289-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="c1289-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="c1289-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="c1289-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="c1289-230">Gelockerte Tensorformeinschränkungen für **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="c1289-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="c1289-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="c1289-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="c1289-232">Eingeführt in DirectML Version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="c1289-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="c1289-233">Die folgenden APIs wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1289-233">Added the following APIs.</span></span>
* [<span data-ttu-id="c1289-234">DMLCreateDevice1-Funktion</span><span class="sxs-lookup"><span data-stu-id="c1289-234">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="c1289-235">DML_FEATURE_LEVEL-Enumeration</span><span class="sxs-lookup"><span data-stu-id="c1289-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="c1289-236">Abfragen auf Featureebene (siehe [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="c1289-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="c1289-237">Unterstützung für die folgenden Operatoren wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1289-237">Added support for the following operators.</span></span>

* <span data-ttu-id="c1289-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="c1289-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="c1289-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="c1289-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="c1289-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="c1289-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="c1289-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="c1289-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="c1289-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="c1289-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="c1289-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="c1289-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="c1289-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="c1289-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="c1289-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="c1289-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="c1289-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="c1289-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="c1289-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="c1289-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="c1289-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="c1289-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="c1289-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="c1289-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="c1289-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="c1289-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="c1289-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="c1289-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="c1289-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="c1289-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="c1289-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="c1289-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="c1289-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="c1289-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="c1289-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="c1289-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="c1289-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="c1289-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="c1289-257">Die folgenden Erweiterungen wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1289-257">Added the following enhancements.</span></span>

* <span data-ttu-id="c1289-258">Wenn Sie eine Eingaberessource für die Verteilung eines [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)binden, ist es jetzt zulässig, eine Ressource mit [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) bereitzustellen (zusätzlich zu **D3D12_HEAP_TYPE_DEFAULT**), solange auch die entsprechenden Heapeigenschaften festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c1289-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="c1289-259">Weitere Informationen finden Sie [unter Binden in DirectML.](./dml-binding.md)</span><span class="sxs-lookup"><span data-stu-id="c1289-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="c1289-260">Die folgenden logischen booleschen Operatoren unterstützen jetzt **UINT8-Ausgabe** tensors zusätzlich zur vorhandenen Unterstützung für **UINT32.**</span><span class="sxs-lookup"><span data-stu-id="c1289-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="c1289-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="c1289-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="c1289-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="c1289-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="c1289-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="c1289-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="c1289-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="c1289-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="c1289-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="c1289-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="c1289-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="c1289-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="c1289-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="c1289-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="c1289-268">5D-Aktivierungsfunktionen unterstützen jetzt die Verwendung von Schritten bei ihren Eingabe- und Ausgabe-Tensoren.</span><span class="sxs-lookup"><span data-stu-id="c1289-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="c1289-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="c1289-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="c1289-270">Die Funktionsebene, in der DirectML eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="c1289-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1289-271">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1289-271">See also</span></span>

* [<span data-ttu-id="c1289-272">DirectML-Versionsverlauf</span><span class="sxs-lookup"><span data-stu-id="c1289-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="c1289-273">DML_FEATURE_LEVEL-Enumeration</span><span class="sxs-lookup"><span data-stu-id="c1289-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="c1289-274">DMLCreateDevice1-Funktion</span><span class="sxs-lookup"><span data-stu-id="c1289-274">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="c1289-275">DML_FEATURE_QUERY_FEATURE_LEVELS-Struktur</span><span class="sxs-lookup"><span data-stu-id="c1289-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
