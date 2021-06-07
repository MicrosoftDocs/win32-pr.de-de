---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: Dekribiert einen Knoten in einem Diagramm [](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) von DirectML-Operatoren, die durch DML_GRAPH_DESC definiert und an [IDMLDevice1::CompileGraph übergeben werden.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
helpviewer_keywords:
- DML_OPERATOR_GRAPH_NODE_DESC
- DML_OPERATOR_GRAPH_NODE_DESC structure
- direct3d12.dml_operator_graph_node_desc
- directml/DML_OPERATOR_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/05/2020
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
- DML_OPERATOR_GRAPH_NODE_DESC
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
ms.openlocfilehash: 997f441de76a60229b76f2f7d67b7acf1a26ed5f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417230"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a>DML_OPERATOR_GRAPH_NODE_DESC -Struktur (directml.h)
Dekribiert einen Knoten in einem Diagramm [](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) von DirectML-Operatoren, die durch DML_GRAPH_DESC definiert und an [IDMLDevice1::CompileGraph übergeben werden.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)

Das Verhalten dieses Knotens wird durch einen DirectML-Operator definiert.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_OPERATOR_GRAPH_NODE_DESC {
  IDMLOperator *Operator;
  const char   *Name;
};
```



## <a name="members"></a>Member

`Operator`

Typ: <b> [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)*</b>

Ein DirectML-Operator, der das Verhalten des Knotens definiert.


`Name`

Typ: \_ Feld \_ z \_ \_ Maybenull const \_ **char \***

Ein optionaler Name für die Graphverbindung. Falls angegeben, kann dies in bestimmten Fehlermeldungen verwendet werden, die von der DirectML-Debugebene ausgegeben werden.

## <a name="availability"></a>Verfügbarkeit

Diese API wurde in der DirectML-Version `1.1.0` eingeführt.



## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Siehe auch

* [IDMLDevice1::CompileGraph-Methode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC-Struktur](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [DML_GRAPH_NODE_DESC-Struktur](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)