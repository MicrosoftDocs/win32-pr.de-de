---
title: Verlauf der directml-Funktionsebene
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 92f5a004b73d608a3958ae0edfa8c6d6b6a523d6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548770"
---
# <a name="directml-feature-level-history"></a>Verlauf der directml-Funktionsebene

Allgemeine Informationen zur directml-Version finden Sie unter [directml-Versionsverlauf](./dml-version-history.md).

## <a name="dml_feature_level_3_0"></a>DML_FEATURE_LEVEL_3_0

Eingeführt in directml-Version 1.4.0.

Unterstützung für die folgenden Operatoren hinzugefügt.

* [DML_OPERATOR_ELEMENT_WISE_BIT_AND](/windows/win32/api/directml/ne-directml-dml_operator_type)
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

Folgende Verbesserungen wurden hinzugefügt.

* Die maximale Anzahl von tensorflow-Dimensionen wurde von 5 auf 8 erweitert. Siehe [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).
* Der folgenden Operatoren wurde zusätzliche Unterstützung für ganzzahlige Datentypen hinzugefügt.
  * **DML_OPERATOR_ELEMENT_WISE_POW**
  * **DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**
  * **DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** und **DML_OPERATOR_MAX_POOLING2**
  * **DML_OPERATOR_REDUCE**, wenn Sie **DML_REDUCE_FUNCTION_ARGMIN** oder **DML_REDUCE_FUNCTION_ARGMAX** verwenden
* Die folgenden 64-Bit-Datentypen wurden hinzugefügt und werden von SELECT-Operatoren unterstützt.
  * **DML_TENSOR_DATA_TYPE_FLOAT64**
  * **DML_TENSOR_DATA_TYPE_UINT64**
  * **DML_TENSOR_DATA_TYPE_INT64**

Als veraltet markierte Funktionen.

* **DML_REDUCE_FUNCTION_ARGMAX** und **DML_REDUCE_FUNCTION_ARGMIN** wurden als veraltet markiert. Es empfiehlt sich, die eigenständigen **DML_OPERATOR_ARGMIN** und **DML_OPERATOR_ARGMAX** Operatoren an ihrer Stelle zu verwenden.

## <a name="dml_feature_level_2_1"></a>DML_FEATURE_LEVEL_2_1

Eingeführt in der directml-Version 1.2.0.

Die folgenden APIs wurden hinzugefügt.

* [IDMLDevice1-Schnittstelle](./directml/nn-directml-idmldevice1.md)
* Operator Graph-Unterstützung (siehe [IDMLDevice1:: compilegraph](./directml/nf-directml-idmldevice1-compilegraph.md) )

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

Folgende Verbesserungen wurden hinzugefügt.

* Der folgenden Operatoren wurde zusätzliche Unterstützung für ganzzahlige Datentypen hinzugefügt.
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
  * **DML_OPERATOR_REDUCE**, wenn Sie eine der folgenden Reduzierungs Funktionen verwenden.
    * **DML_REDUCE_FUNCTION_ARGMIN**
    * **DML_REDUCE_FUNCTION_ARGMAX**
    * **DML_REDUCE_FUNCTION_MAX**
    * **DML_REDUCE_FUNCTION_MIN**
    * **DML_REDUCE_FUNCTION_MULTIPLY**
    * **DML_REDUCE_FUNCTION_SUM**
* Einschränkungen der tensorflow-Form für **DML_OPERATOR_GATHER**

## <a name="dml_feature_level_2_0"></a>DML_FEATURE_LEVEL_2_0

Eingeführt in directml, Version 1.1.0.

Die folgenden APIs wurden hinzugefügt.
* [DMLCreateDevice1-Funktion](./directml/nf-directml-dmlcreatedevice1.md)
* [DML_FEATURE_LEVEL-Enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
* Abfragen auf Funktionsebene (siehe [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))

Unterstützung für die folgenden Operatoren hinzugefügt.

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

Folgende Verbesserungen wurden hinzugefügt.

* Wenn eine Eingabe Ressource für die Verteilung eines [idmloperatorinitializers](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)gebunden wird, ist es jetzt zulässig, eine Ressource mit [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (zusätzlich zu **D3D12_HEAP_TYPE_DEFAULT**) bereitzustellen, solange geeignete Heap Eigenschaften festgelegt sind. Weitere Informationen finden Sie [Unterbindung in directml](./dml-binding.md).
* Die folgenden logischen booleschen Operatoren unterstützen nun neben der vorhandenen Unterstützung für **UInt32** auch **Uint8** -ausgabetensoren.
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**
* 5D-Aktivierungs Funktionen unterstützen jetzt die Verwendung von Fortschritten auf Ihren Eingabe-und Ausgabe Tensoren.

## <a name="dml_feature_level_1_0"></a>DML_FEATURE_LEVEL_1_0

Die Funktionsebene, in der directml eingeführt wurde.

## <a name="see-also"></a>Siehe auch

[Versionsverlauf](./dml-version-history.md) 
 der directml [DML_FEATURE_LEVEL-Enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level) 
 [DMLCreateDevice1-Funktion](./directml/nf-directml-dmlcreatedevice1.md) 
 [DML_FEATURE_QUERY_FEATURE_LEVELS Struktur](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)