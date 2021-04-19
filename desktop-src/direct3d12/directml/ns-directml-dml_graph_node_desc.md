---
UID: NS:directml.DML_GRAPH_NODE_DESC
title: DML_GRAPH_NODE_DESC
description: 'Ein generischer Container für einen Knoten innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.'
helpviewer_keywords:
- DML_GRAPH_NODE_DESC
- DML_GRAPH_NODE_DESC structure
- direct3d12.dml_graph_node_desc
- directml/DML_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_DESC, DML_GRAPH_NODE_DESC structure, direct3d12.dml_graph_node_desc, directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
- directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
ms.openlocfilehash: 8c79719f51efb4a59f9459a28765d3442ed3f4ee
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106353249"
---
# <a name="dml_graph_node_desc-structure-directmlh"></a>DML_GRAPH_NODE_DESC-Struktur (directml. h)
Ein generischer Container für einen Knoten innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax
```cpp
struct DML_GRAPH_NODE_DESC {
  DML_GRAPH_NODE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a>Member

`Type`

Typ: **[DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md)**

Der Typ des Diagramm Knotens. Unter [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) finden Sie verfügbare Typen.


`Desc`

Type: \_ Field \_ size \_ (ungültig \_ \_ ("abhängig von Knotentyp")) Konstante **void \***

Ein Zeiger auf die Diagramm Knoten Beschreibung. Der Typ der Pointto-Struktur muss mit dem in *Type* angegebenen Wert identisch sein.

## <a name="availability"></a>Verfügbarkeit

Diese API wurde in der directml-Version eingeführt `1.1.0` .



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |

## <a name="see-also"></a>Siehe auch

* [IDMLDevice1:: compilegraph-Methode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC Struktur](./ns-directml-dml_graph_desc.md)