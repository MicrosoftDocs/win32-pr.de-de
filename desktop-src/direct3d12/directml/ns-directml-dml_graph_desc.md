---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Beschreibt ein Diagramm von DirectML-Operatoren, die zum Kompilieren eines kombinierten, optimierten Operators verwendet werden.
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
ms.openlocfilehash: a42996fc9fd7825e13232b245ab764c6439f9489
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417799"
---
# <a name="dml_graph_desc-structure-directmlh"></a>DML_GRAPH_DESC -Struktur (directml.h)

Beschreibt ein Diagramm von DirectML-Operatoren, die zum Kompilieren eines kombinierten, optimierten Operators verwendet werden. Siehe [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a>Member

`InputCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Eingaben des Gesamtdiagramms. Jede Grapheingabe kann mit einer variablen Anzahl interner Knoten verbunden sein, daher kann sich dies von *InputEdgeCount unterscheiden.*


`OutputCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Ausgaben des Gesamtdiagramms. Jede Graphausgabe kann mit einer variablen Anzahl interner Knoten verbunden sein, daher kann sich dies von *OutputEdgeCount unterscheiden.*


`NodeCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der internen Knoten im Diagramm.


`Nodes`

Typ: \_ \_ Feldgröße \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***

Die internen Knoten im Diagramm.


`InputEdgeCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Verbindungen zwischen Grapheingaben und Eingaben interner Knoten im Diagramm.


`InputEdges`

Typ: \_ \_ Feldgröße \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Ein Array von Verbindungen zwischen Grapheingaben und Eingaben interner Knoten im Diagramm. Das *Feld Typ* in jedem Element sollte auf DML_GRAPH_EDGE_TYPE_INPUT. [](./ne-directml-dml_graph_edge_type.md)


`OutputEdgeCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Verbindungen zwischen Graph-Ausgaben und Ausgaben interner Knoten im Diagramm.


`OutputEdges`

Typ: \_ \_ Feldgröße \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Ein Array von Verbindungen zwischen Graph-Ausgaben und Ausgaben interner Knoten im Diagramm. Das *Feld Typ* in jedem Element sollte auf DML_GRAPH_EDGE_TYPE_OUTPUT. [](./ne-directml-dml_graph_edge_type.md)


`IntermediateEdgeCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der internen Verbindungen zwischen Knoten im Diagramm.


`IntermediateEdges`

Typ: \_ \_ Feldgröße \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Ein Array von Verbindungen zwischen Ein- und Ausgaben interner Knoten im Diagramm. Das Feld Typ in jedem Element sollte auf ["DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)


## <a name="remarks"></a>Hinweise
Das von dieser Struktur beschriebene Diagramm muss ein gerichtetes azyklisches Diagramm sein. Sie müssen eine Verbindung für die Ein- und Ausgabe jedes angegebenen Knotens definieren, mit Ausnahme von Ein- und Ausgaben, die für den zugeordneten Operator optional sind.

Knoten können Operatoren verwenden, die mit dem [DML_TENSOR_FLAG_OWNED_BY_DML-Flag](/windows/win32/api/directml/ne-directml-dml_tensor_flags) für bestimmte Eingaben erstellt wurden. Alle Operatoreingaben, die dieses Flag verwenden, müssen mit Grapheingaben verbunden sein. Alle Operatoreingaben, die mit derselben Grapheingabe verbunden sind, müssen dieses Flag entsprechend verwenden oder weglassen.

Es ist gesetzlich, Operatoren zu verbinden, deren verbundene Eingaben und Ausgaben unterschiedliche Dimensionsanzahlen, Größen und Datentypen verwenden. Dies bedeutet, dass das Tensor-Datenblob von jedem Operator unterschiedlich interpretiert wird. Das *Feld TotalTensorSizeInBytes* der verbundenen Tensoreingaben und -ausgaben muss jedoch identisch sein. Operatoren sollten nur Bereiche von Tensoren lesen, die von früheren Operatoren geschrieben wurden. Alle Auf padding-Bereiche in der Ausgabe eines Vorgangs (die sich aus der Verwendung von Strides ergeben) werden von Downstreamoperatoren nicht als 0 (null) gelesen.

## <a name="availability"></a>Verfügbarkeit

Diese API wurde in der DirectML-Version `1.1.0` eingeführt.


## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Siehe auch

* [IDMLDevice1::CompileGraph-Methode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_NODE_DESC Struktur](./ns-directml-dml_graph_node_desc.md)
* [DML_GRAPH_EDGE_DESC Struktur](./ns-directml-dml_graph_edge_desc.md)