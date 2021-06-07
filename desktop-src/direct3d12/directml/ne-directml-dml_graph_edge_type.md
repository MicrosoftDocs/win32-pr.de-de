---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Definiert Konstanten, die einen Typ des Graphenrands angeben. Informationen [zur DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) Enumeration finden Sie unter DML_GRAPH_EDGE_DESC.
helpviewer_keywords:
- DML_GRAPH_EDGE_TYPE
- DML_GRAPH_EDGE_TYPE structure
- direct3d12.dml_graph_edge_type
- directml/DML_GRAPH_EDGE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
- directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
ms.openlocfilehash: d65649fcd2115cc7cdcc1b01da20ef44b0436e6f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417919"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a>DML_GRAPH_EDGE_TYPE -Enumeration (directml.h)

Definiert Konstanten, die einen Typ des Graphenrands angeben. Informationen [zur DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) Enumeration finden Sie unter DML_GRAPH_EDGE_DESC.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a>Konstanten

| Name | BESCHREIBUNG |
| ---- |:---- |
| DML_GRAPH_EDGE_TYPE_INVALID | Gibt einen unbekannten Graphenrandtyp an und ist nie gültig. Die Verwendung dieses Werts führt zu einem Fehler. |
| DML_GRAPH_EDGE_TYPE_INPUT | Gibt an, dass der Graphrand von der -Struktur [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) wird. |
| DML_GRAPH_EDGE_TYPE_OUTPUT | Gibt an, dass der Graphrand von der -Struktur [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) wird. |
| DML_GRAPH_EDGE_TYPE_INTERMEDIATE | Gibt an, dass der Graphrand von der -Struktur [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) wird.<br><br>##-Verfügbarkeit<br><br>Diese API wurde in der DirectML-Version `1.1.0` eingeführt. |


## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Siehe auch

* [IDMLDevice1::CompileGraph-Methode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC-Struktur](./ns-directml-dml_graph_desc.md)     
* [DML_GRAPH_EDGE_DESC-Struktur](./ns-directml-dml_graph_edge_desc.md)
* [DML_INPUT_GRAPH_EDGE_DESC-Struktur](./ns-directml-dml_input_graph_edge_desc.md)
* [DML_OUTPUT_GRAPH_EDGE_DESC-Struktur](./ns-directml-dml_output_graph_edge_desc.md)
* [DML_INTERMEDIATE_GRAPH_EDGE_DESC-Struktur](./ns-directml-dml_intermediate_graph_edge_desc.md)