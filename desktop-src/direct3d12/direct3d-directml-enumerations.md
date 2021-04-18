---
title: DirectML-Enumerationen
description: Die folgenden Enumerationen werden in "directml. h" deklariert.
ms.localizationpriority: low
ms.topic: article
ms.date: 11/06/2020
ms.custom: 19H1
ms.openlocfilehash: 6479b1bfe4216a5bdbe8aaee78c258f6f4a64f94
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106354897"
---
# <a name="directml-enumerations"></a>DirectML-Enumerationen

Die folgenden Enumerationen werden in "directml. h" deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema und Beschreibung |
|-|
| [**DML_AXIS_DIRECTION**](/windows/desktop/direct3d12/directml/ne-directml-dml_axis_direction). Definiert Konstanten, die die Richtung eines Vorgangs entlang der angegebenen Achse für den Operator angeben (z. b. die Summe, das Auswählen der Top-k-Elemente, das Auswählen des minimalen Elements). |
| [**DML_BINDING_TYPE**](/windows/desktop/api/directml/ne-directml-dml_binding_type). Definiert Konstanten, die die Art der Ressource angeben, auf die durch eine Bindungs Beschreibung [DML_BINDING_DESC Struktur](/windows/desktop/api/directml/ns-directml-dml_binding_desc)verwiesen wird. |
| [**DML_CONVOLUTION_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_convolution_direction). Definiert Konstanten, die eine Richtung für den Operator "directml-Operator" angeben (wie von der [DML_CONVOLUTION_OPERATOR_DESC Struktur](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)beschrieben). |
| [**DML_CONVOLUTION_MODE**](/windows/desktop/api/directml/ne-directml-dml_convolution_mode). Definiert Konstanten, die einen Modus für den Operator "directml-Operator" angeben (wie von der [DML_CONVOLUTION_OPERATOR_DESC Struktur](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)beschrieben). |
| [**DML_CREATE_DEVICE_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_create_device_flags). Bietet zusätzliche Optionen zur Geräte Erstellung für [dmlkreatedevice](/windows/desktop/api/directml/nf-directml-dmlcreatedevice). |
| [**DML_DEPTH_SPACE_ORDER**](/windows/desktop/direct3d12/directml/ne-directml-dml_depth_space_order). Definiert Konstanten, die die in den directml-Operatoren angewendete Transformation [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) und **DML_OPERATOR_SPACE_TO_DEPTH1** steuern. |
| [**DML_EXECUTION_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_execution_flags). Gibt Optionen für die directml an, um die Ausführung von Operatoren zu steuern. |
| [**DML_FEATURE**](/windows/desktop/api/directml/ne-directml-dml_feature). Definiert eine Reihe optionaler Features und Funktionen, die vom directml-Gerät abgefragt werden können. |
| [**DML_GRAPH_EDGE_TYPE**](/windows/desktop/direct3d12/directml/ne-directml-dml_graph_edge_type). Definiert Konstanten, die einen Typ von Diagramm Rand angeben. Weitere Informationen finden Sie unter [DML_GRAPH_EDGE_DESC](./directml/ns-directml-dml_graph_edge_desc.md) für die Verwendung dieser Enumeration. |
| [**DML_GRAPH_NODE_TYPE**](/windows/desktop/direct3d12/directml/ne-directml-dml_graph_node_type). Definiert Konstanten, die einen Typ von Diagramm Knoten angeben. Weitere Informationen finden Sie unter [DML_GRAPH_NODE_DESC](./directml/ns-directml-dml_graph_node_desc.md) für die Verwendung dieser Enumeration. |
| [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode). Definiert Konstanten, die einen Modus für den Operator "directml Upsample 2-D" angeben (wie in der [DML_UPSAMPLE_2D_OPERATOR_DESC-Struktur](/windows/desktop/api/directml/ns-directml-dml_upsample_2d_operator_desc)beschrieben). |
| [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform). Definiert Konstanten, die eine Matrix Transformation angeben, die auf einen directml-Tensor angewendet werden soll. |
| [**DML_OPERATOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_operator_type). Definiert den Typ einer Operator Beschreibung. |
| [**DML_PADDING_MODE**](/windows/desktop/api/directml/ne-directml-dml_padding_mode). Definiert Konstanten, die einen Modus für den directml-Auffüll Operator angeben (wie in der [DML_PADDING_OPERATOR_DESC Struktur](/windows/desktop/api/directml/ns-directml-dml_padding_operator_desc)beschrieben). |
| [**DML_RANDOM_GENERATOR_TYPE**](./directml/ne-directml-dml_random_generator_type.md). Definiert Konstanten, die Typen von zufälligem Zufallszahlengenerator angeben. |
| [**DML_RECURRENT_NETWORK_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction). Definiert Konstanten, die eine Richtung für einen wiederkehrenden directml-Operator angeben. |
| [**DML_REDUCE_FUNCTION**](/windows/desktop/api/directml/ne-directml-dml_reduce_function). Definiert Konstanten, die den spezifischen Reduzierungs Algorithmus angeben, der für den directml-Reduzierungs Operator verwendet werden soll (wie von der [DML_REDUCE_OPERATOR_DESC Struktur](/windows/desktop/api/directml/ns-directml-dml_reduce_operator_desc)beschrieben). |
| [**DML_TENSOR_DATA_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_data_type). Gibt den Datentyp der Werte in einem Tensor an. |
| [**DML_TENSOR_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags). Gibt zusätzliche Optionen in einer tensorflow-Beschreibung an. |
| [**DML_TENSOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_type). Identifiziert einen Typ der tensorflow-Beschreibung. |

## <a name="related-topics"></a>Zugehörige Themen

* [DirectML-Referenz](direct3d-directml-reference.md)
* [Core-Referenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)