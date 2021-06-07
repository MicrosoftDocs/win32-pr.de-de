---
title: DirectML-Enumerationen
description: Die folgenden Enumerationen werden in DirectML.h deklariert.
ms.localizationpriority: low
ms.topic: article
ms.date: 11/06/2020
ms.custom: 19H1
ms.openlocfilehash: 2a761dba639ece37eba347115a831d3c6803a618
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521215"
---
# <a name="directml-enumerations"></a>DirectML-Enumerationen

Die folgenden Enumerationen werden in DirectML.h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema und Beschreibung |
|-|
| [**DML_AXIS_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_axis_direction). Definiert Konstanten, die die Richtung eines Vorgangs entlang der angegebenen Achse für den Operator angeben (z. B. Summierung, Auswahl der top-k-Elemente, Auswahl des Minimalelements). |
| [**DML_BINDING_TYPE**](/windows/desktop/api/directml/ne-directml-dml_binding_type). Definiert Konstanten, die die Art der Ressourcen angeben, auf die durch eine Bindungsbeschreibung DML_BINDING_DESC [wird.](/windows/desktop/api/directml/ns-directml-dml_binding_desc) |
| [**DML_CONVOLUTION_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_convolution_direction). Definiert Konstanten, die eine Richtung für den DirectML-Konvolutionsoperator angeben (wie in der DML_CONVOLUTION_OPERATOR_DESC [beschrieben).](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc) |
| [**DML_CONVOLUTION_MODE**](/windows/desktop/api/directml/ne-directml-dml_convolution_mode). Definiert Konstanten, die einen Modus für den DirectML-Konvolutionsoperator angeben (wie in der DML_CONVOLUTION_OPERATOR_DESC [beschrieben).](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc) |
| [**DML_CREATE_DEVICE_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_create_device_flags). Stellt zusätzliche Optionen zum Erstellen von Geräten für [DMLCreateDevice zur Verfügung.](/windows/desktop/api/directml/nf-directml-dmlcreatedevice) |
| [**DML_DEPTH_SPACE_ORDER**](/windows/desktop/api/directml/ne-directml-dml_depth_space_order). Definiert Konstanten, die die Transformation steuern, die in den DirectML-Operatoren DML_OPERATOR_DEPTH_TO_SPACE1 **und** DML_OPERATOR_SPACE_TO_DEPTH1. [](/windows/win32/api/directml/ne-directml-dml_operator_type) |
| [**DML_EXECUTION_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_execution_flags). Stellt Optionen für DirectML zur Verfügung, um die Ausführung von Operatoren zu steuern. |
| [**DML_FEATURE**](/windows/desktop/api/directml/ne-directml-dml_feature). Definiert eine Reihe optionaler Features und Funktionen, die vom DirectML-Gerät abgefragt werden können. |
| [**DML_GRAPH_EDGE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_edge_type). Definiert Konstanten, die einen Typ des Graphenrands angeben. Informationen [zur DML_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_edge_desc) Enumeration finden Sie unter DML_GRAPH_EDGE_DESC. |
| [**DML_GRAPH_NODE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_node_type). Definiert Konstanten, die einen Graphknotentyp angeben. Informationen [zur DML_GRAPH_NODE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_node_desc) Enumeration finden Sie unter DML_GRAPH_NODE_DESC. |
| [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode). Definiert Konstanten, die einen Modus für den DirectML-Upsample-2D-Operator angeben (wie in der DML_UPSAMPLE_2D_OPERATOR_DESC [beschrieben).](/windows/desktop/api/directml/ns-directml-dml_upsample_2d_operator_desc) |
| [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform). Definiert Konstanten, die eine Matrixtransformation angeben, die auf einen DirectML-Tensor angewendet werden soll. |
| [**DML_OPERATOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_operator_type). Definiert den Typ einer Operatorbeschreibung. |
| [**DML_PADDING_MODE**](/windows/desktop/api/directml/ne-directml-dml_padding_mode). Definiert Konstanten, die einen Modus für den DirectML-Pad-Operator angeben (wie in der DML_PADDING_OPERATOR_DESC [beschrieben).](/windows/desktop/api/directml/ns-directml-dml_padding_operator_desc) |
| [**DML_RANDOM_GENERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_random_generator_type). Definiert Konstanten, die Typen des Zufallszahlengenerators angeben. |
| [**DML_RECURRENT_NETWORK_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction). Definiert Konstanten, die eine Richtung für einen wiederkehrenden DirectML-Operator angeben. |
| [**DML_REDUCE_FUNCTION**](/windows/desktop/api/directml/ne-directml-dml_reduce_function). Definiert Konstanten, die den spezifischen Reduzierungsalgorithmus angeben, der für den DirectML-Reduzierungsoperator verwendet werden soll (wie in der DML_REDUCE_OPERATOR_DESC [beschrieben).](/windows/desktop/api/directml/ns-directml-dml_reduce_operator_desc) |
| [**DML_TENSOR_DATA_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_data_type). Gibt den Datentyp der Werte in einem Tensor an. |
| [**DML_TENSOR_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags). Gibt zusätzliche Optionen in einer Tensorbeschreibung an. |
| [**DML_TENSOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_type). Identifiziert einen Tensorbeschreibungstyp. |

## <a name="related-topics"></a>Zugehörige Themen

* [DirectML-Referenz](direct3d-directml-reference.md)
* [Core-Referenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)