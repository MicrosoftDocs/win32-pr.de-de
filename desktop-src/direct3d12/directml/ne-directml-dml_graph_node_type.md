---
UID: NE:directml.DML_GRAPH_NODE_TYPE
title: DML_GRAPH_NODE_TYPE
description: Definiert Konstanten, die einen Typ von Diagrammknoten angeben. Informationen zur Verwendung dieser Enumeration finden Sie unter [DML_GRAPH_NODE_DESC.](./ns-directml-dml_graph_node_desc.md)
helpviewer_keywords:
- DML_GRAPH_NODE_TYPE
- DML_GRAPH_NODE_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_GRAPH_NODE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_TYPE, DML_GRAPH_NODE_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
- directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
ms.openlocfilehash: 0bb0712370da35c4b8c9278ad7721d2ffc7d875d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417179"
---
# <a name="dml_graph_node_type-enumeration-directmlh"></a>DML_GRAPH_NODE_TYPE-Enumeration (directml.h)

Definiert Konstanten, die einen Typ von Diagrammknoten angeben. Informationen zur Verwendung dieser Enumeration finden Sie unter [DML_GRAPH_NODE_DESC.](./ns-directml-dml_graph_node_desc.md)

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
typedef enum DML_GRAPH_NODE_TYPE {
  DML_GRAPH_NODE_TYPE_INVALID,
  DML_GRAPH_NODE_TYPE_OPERATOR
} ;
```

## <a name="constants"></a>Konstanten

| Name | BESCHREIBUNG |
| ---- |:---- |
| DML_GRAPH_NODE_TYPE_INVALID | Gibt einen unbekannten Graph-Edgetyp an und ist nie gültig. Die Verwendung dieses Werts führt zu einem Fehler. |
| DML_GRAPH_NODE_TYPE_OPERATOR | Gibt an, dass der Graphrand von der [DML_OPERATOR_GRAPH_NODE_DESC-Struktur](./ns-directml-dml_operator_graph_node_desc.md) beschrieben wird.<br><br>## Verfügbarkeit<br><br>Diese API wurde in DirectML-Version `1.1.0` eingeführt. |


## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Siehe auch

* [IDMLDevice1::CompileGraph-Methode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC-Struktur](./ns-directml-dml_graph_desc.md)     
* [DML_GRAPH_NODE_DESC Struktur](./ns-directml-dml_graph_node_desc.md)
* [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md)