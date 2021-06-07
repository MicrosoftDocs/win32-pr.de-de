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
# <a name="directml-feature-level-history"></a>DirectML-Verlauf auf Featureebene

Den allgemeinen DirectML-Versionsverlauf finden Sie unter [DirectML-Versionsverlauf.](./dml-version-history.md)

## <a name="dml_feature_level_3_1"></a>DML_FEATURE_LEVEL_3_1

Eingeführt in DirectML Version 1.5.0.

Unterstützung für die folgenden Operatoren [wurde hinzugefügt.](/windows/win32/api/directml/ne-directml-dml_operator_type)

* **DML_OPERATOR_ELEMENT_WISE_ATAN_YX**
* **DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**
* **DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**
* **DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**
* **DML_OPERATOR_CUMULATIVE_PRODUCT**
* **DML_OPERATOR_BATCH_NORMALIZATION_GRAD**

Die maximale Anzahl unterstützter Dimensionen für die folgenden Operatoren wurde von 4 auf 8 erhöht.

* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_CAST**
* **DML_OPERATOR_JOIN**
* **DML_OPERATOR_LP_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_PADDING**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_TILE**
* **DML_OPERATOR_TOP_K**
* **DML_OPERATOR_TOP_K1**

## <a name="dml_feature_level_3_0"></a>DML_FEATURE_LEVEL_3_0

Eingeführt in DirectML Version 1.4.0.

Unterstützung für die folgenden Operatoren [wurde hinzugefügt.](/windows/win32/api/directml/ne-directml-dml_operator_type)

* **DML_OPERATOR_ELEMENT_WISE_BIT_AND**
* **DML_OPERATOR_ELEMENT_WISE_BIT_OR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_XOR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_NOT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**
* **DML_OPERATOR_ACTIVATION_CELU**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_AVERAGE_POOLING_GRAD**
* **DML_OPERATOR_MAX_POOLING_GRAD**
* **DML_OPERATOR_RANDOM_GENERATOR**
* **DML_OPERATOR_NONZERO_COORDINATES**
* **DML_OPERATOR_RESAMPLE_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_ADAM_OPTIMIZER**
* **DML_OPERATOR_ARGMIN**
* **DML_OPERATOR_ARGMAX**
* **DML_OPERATOR_ROI_ALIGN**
* **DML_OPERATOR_GATHER_ND1**

Die folgenden Erweiterungen wurden hinzugefügt.

* Die maximale Anzahl von Tensordimensionen wurde von 5 auf 8 erhöht. Siehe [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).
* Den folgenden Operatoren wurde zusätzliche Unterstützung für ganzzahlige Datentypen hinzugefügt.
  * **DML_OPERATOR_ELEMENT_WISE_POW**
  * **DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**
  * **DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** und **DML_OPERATOR_MAX_POOLING2**
  * **DML_OPERATOR_REDUCE** bei Verwendung **von** DML_REDUCE_FUNCTION_ARGMIN oder **DML_REDUCE_FUNCTION_ARGMAX**
* Die folgenden 64-Bit-Datentypen wurden hinzugefügt und werden von select-Operatoren unterstützt.
  * **DML_TENSOR_DATA_TYPE_FLOAT64**
  * **DML_TENSOR_DATA_TYPE_UINT64**
  * **DML_TENSOR_DATA_TYPE_INT64**

Veraltete Funktionalität.

* **DML_REDUCE_FUNCTION_ARGMAX** und **DML_REDUCE_FUNCTION_ARGMIN** sind veraltet. Sie sollten die eigenständigen DML_OPERATOR_ARGMIN **und** **DML_OPERATOR_ARGMAX** verwenden.

## <a name="dml_feature_level_2_1"></a>DML_FEATURE_LEVEL_2_1

Eingeführt in DirectML Version 1.2.0.

Die folgenden APIs wurden hinzugefügt.

* [IDMLDevice1-Schnittstelle](/windows/win32/api/directml/nn-directml-idmldevice1)
* Operatordiagrammunterstützung (siehe [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)

Unterstützung für die folgenden Operatoren hinzugefügt.

* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**
* **DML_OPERATOR_ELEMENT_WISE_ROUND**
* **DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**
* **DML_OPERATOR_FILL_VALUE_CONSTANT**
* **DML_OPERATOR_FILL_VALUE_SEQUENCE**
* **DML_OPERATOR_CUMULATIVE_SUMMATION**
* **DML_OPERATOR_REVERSE_SUBSEQUENCES**
* **DML_OPERATOR_GATHER_ELEMENTS**
* **DML_OPERATOR_GATHER_ND**
* **DML_OPERATOR_SCATTER_ND**
* **DML_OPERATOR_MAX_POOLING2**
* **DML_OPERATOR_SLICE1**
* **DML_OPERATOR_TOP_K1**
* **DML_OPERATOR_DEPTH_TO_SPACE1**
* **DML_OPERATOR_SPACE_TO_DEPTH1**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_RESAMPLE1**
* **DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**
* **DML_OPERATOR_CONVOLUTION_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**

Die folgenden Erweiterungen wurden hinzugefügt.

* Den folgenden Operatoren wurde zusätzliche Unterstützung für ganzzahlige Datentypen hinzugefügt.
  * **DML_OPERATOR_ELEMENT_WISE_IDENTITY**
  * **DML_OPERATOR_ELEMENT_WISE_ABS**
  * **DML_OPERATOR_ELEMENT_WISE_ADD**
  * **DML_OPERATOR_ELEMENT_WISE_CLIP**
  * **DML_OPERATOR_ELEMENT_WISE_DIVIDE**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_MAX**
  * **DML_OPERATOR_ELEMENT_WISE_MEAN**
  * **DML_OPERATOR_ELEMENT_WISE_MIN**
  * **DML_OPERATOR_ELEMENT_WISE_MULTIPLY**
  * **DML_OPERATOR_ELEMENT_WISE_SUBTRACT**
  * **DML_OPERATOR_ELEMENT_WISE_THRESHOLD**
  * **DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_SIGN**
  * **DML_OPERATOR_ELEMENT_WISE_IF**
  * **DML_OPERATOR_ACTIVATION_SHRINK**
  * **DML_OPERATOR_PADDING**
  * **DML_OPERATOR_GATHER**
  * **DML_OPERATOR_SCATTER**
  * **DML_OPERATOR_DEPTH_TO_SPACE**
  * **DML_OPERATOR_SPACE_TO_DEPTH**
  * **DML_OPERATOR_TILE**
  * **DML_OPERATOR_TOP_K** und **DML_OPERATOR_TOP_K1**
  * **DML_OPERATOR_ONE_HOT**
  * **DML_OPERATOR_REDUCE**, wenn Sie eine der folgenden Reduce-Funktionen verwenden.
    * **DML_REDUCE_FUNCTION_ARGMIN**
    * **DML_REDUCE_FUNCTION_ARGMAX**
    * **DML_REDUCE_FUNCTION_MAX**
    * **DML_REDUCE_FUNCTION_MIN**
    * **DML_REDUCE_FUNCTION_MULTIPLY**
    * **DML_REDUCE_FUNCTION_SUM**
* Gelockerte Tensorformeinschränkungen für **DML_OPERATOR_GATHER**

## <a name="dml_feature_level_2_0"></a>DML_FEATURE_LEVEL_2_0

Eingeführt in DirectML Version 1.1.0.

Die folgenden APIs wurden hinzugefügt.
* [DMLCreateDevice1-Funktion](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [DML_FEATURE_LEVEL-Enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
* Abfragen auf Featureebene (siehe [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))

Unterstützung für die folgenden Operatoren wurde hinzugefügt.

* **DML_OPERATOR_ELEMENT_WISE_SIGN**
* **DML_OPERATOR_ELEMENT_WISE_IS_NAN**
* **DML_OPERATOR_ELEMENT_WISE_ERF**
* **DML_OPERATOR_ELEMENT_WISE_SINH**
* **DML_OPERATOR_ELEMENT_WISE_COSH**
* **DML_OPERATOR_ELEMENT_WISE_TANH**
* **DML_OPERATOR_ELEMENT_WISE_ASINH**
* **DML_OPERATOR_ELEMENT_WISE_ACOSH**
* **DML_OPERATOR_ELEMENT_WISE_ATANH**
* **DML_OPERATOR_ELEMENT_WISE_IF**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_MAX_POOLING1**
* **DML_OPERATOR_MAX_UNPOOLING**
* **DML_OPERATOR_DIAGONAL_MATRIX**
* **DML_OPERATOR_SCATTER_ELEMENTS**
* **DML_OPERATOR_SCATTER**
* **DML_OPERATOR_ONE_HOT**
* **DML_OPERATOR_RESAMPLE**

Die folgenden Erweiterungen wurden hinzugefügt.

* Wenn Sie eine Eingaberessource für die Verteilung eines [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)binden, ist es jetzt zulässig, eine Ressource mit [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) bereitzustellen (zusätzlich zu **D3D12_HEAP_TYPE_DEFAULT**), solange auch die entsprechenden Heapeigenschaften festgelegt sind. Weitere Informationen finden Sie [unter Binden in DirectML.](./dml-binding.md)
* Die folgenden logischen booleschen Operatoren unterstützen jetzt **UINT8-Ausgabe** tensors zusätzlich zur vorhandenen Unterstützung für **UINT32.**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**
* 5D-Aktivierungsfunktionen unterstützen jetzt die Verwendung von Schritten bei ihren Eingabe- und Ausgabe-Tensoren.

## <a name="dml_feature_level_1_0"></a>DML_FEATURE_LEVEL_1_0

Die Funktionsebene, in der DirectML eingeführt wurde.

## <a name="see-also"></a>Siehe auch

* [DirectML-Versionsverlauf](./dml-version-history.md)
* [DML_FEATURE_LEVEL-Enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [DMLCreateDevice1-Funktion](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [DML_FEATURE_QUERY_FEATURE_LEVELS-Struktur](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
