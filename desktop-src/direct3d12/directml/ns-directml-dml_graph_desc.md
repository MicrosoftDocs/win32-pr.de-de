---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Beschreibt ein Diagramm der directml-Operatoren, die zum Kompilieren eines kombinierten, optimierten Operators verwendet werden.
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
ms.openlocfilehash: e72209d19bb26524576783becbbfbf94566d8370
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361110"
---
# <a name="dml_graph_desc-structure-directmlh"></a>DML_GRAPH_DESC-Struktur (directml. h)

Beschreibt ein Diagramm der directml-Operatoren, die zum Kompilieren eines kombinierten, optimierten Operators verwendet werden. Weitere Informationen finden Sie unter [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Eingaben des Gesamt Diagramms. Jede Diagramm Eingabe kann mit einer Variablen Anzahl interner Knoten verbunden werden. Daher kann sich dies von *inputedgecount* unterscheiden.


`OutputCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Ausgaben des gesamten Diagramms. Jede Diagramm Ausgabe kann mit einer Variablen Anzahl interner Knoten verbunden werden. Daher kann sich dies von *outputedgecount* unterscheiden.


`NodeCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der internen Knoten im Diagramm.


`Nodes`

Type: \_ Field \_ size \_ (NodeCount) **Konstanten [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***

Die internen Knoten im Diagramm.


`InputEdgeCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Verbindungen zwischen Graph-Eingaben und Eingaben interner Knoten im Diagramm.


`InputEdges`

Type: \_ Field \_ size \_ (inputedgecount) **Konstanten [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Ein Array von Verbindungen zwischen Graph-Eingaben und Eingaben interner Knoten im Diagramm. Das *typanfeld* innerhalb der einzelnen Elemente sollte auf [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md)festgelegt werden.


`OutputEdgeCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der Verbindungen zwischen Diagramm Ausgaben und Ausgaben interner Knoten im Diagramm.


`OutputEdges`

Type: \_ Field \_ size \_ (outputedgecount) **Konstanten [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Ein Array von Verbindungen zwischen Diagramm Ausgaben und Ausgaben interner Knoten im Diagramm. Das *typanfeld* innerhalb der einzelnen Elemente sollte auf [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md)festgelegt werden.


`IntermediateEdgeCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der internen Verbindungen zwischen den Knoten im Diagramm.


`IntermediateEdges`

Type: \_ Field \_ size \_ (intermediateedgecount) **Konstanten [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Ein Array von Verbindungen zwischen Eingaben und Ausgaben interner Knoten im Diagramm. Das typanfeld innerhalb der einzelnen Elemente sollte auf festgelegt werden [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)


## <a name="remarks"></a>Bemerkungen
Das von dieser Struktur beschriebene Diagramm muss ein gerichtetes azyklisches Diagramm sein. Sie müssen eine Verbindung für die Eingabe und die Ausgabe der einzelnen bereitgestellten Knoten definieren, mit Ausnahme von Eingaben und Ausgaben, die für den zugeordneten Operator optional sind.

Knoten können Operatoren verwenden, die mit dem [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) -Flag für bestimmte Eingaben erstellt wurden. Alle Operator Eingaben, die dieses Flag verwenden, müssen mit Graph-Eingaben verbunden sein. Alle Operator Eingaben, die mit derselben Diagramm Eingabe verbunden sind, müssen dieses Flag gleichwertig verwenden oder weglassen.

Es ist für Verbindungs Operatoren zulässig, deren verbundene Eingaben und Ausgaben verschiedene Dimensions Zähler, Größen und Datentypen verwenden. Dies bedeutet, dass das tensorflow-datenblob von jedem Operator anders interpretiert wird. Das *totaltensorsizeinbytes* -Feld der verbundenen tensorflow-Eingaben und-Ausgaben muss jedoch identisch sein. Operatoren sollten nur Regionen von Tensoren lesen, die von früheren Operatoren geschrieben wurden. Alle Leerraum Bereiche in der Ausgabe eines Vorgangs (die sich aus der Verwendung von Fortschritten ergeben) werden nicht garantiert als 0 (null) von Datenstrom Operatoren gelesen.

## <a name="availability"></a>Verfügbarkeit

Diese API wurde in der directml-Version eingeführt `1.1.0` .


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |

## <a name="see-also"></a>Siehe auch

* [IDMLDevice1:: compilegraph-Methode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_NODE_DESC-Struktur](./ns-directml-dml_graph_node_desc.md)
* [DML_GRAPH_EDGE_DESC-Struktur](./ns-directml-dml_graph_edge_desc.md)