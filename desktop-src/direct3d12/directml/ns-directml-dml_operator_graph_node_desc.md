---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: 'Decoiert einen Knoten innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.'
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
ms.openlocfilehash: 6081f81044ff2ce384f7906af9c6e80f6b06f774
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106357143"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a>DML_OPERATOR_GRAPH_NODE_DESC-Struktur (directml. h)
Decoiert einen Knoten innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.

Das Verhalten dieses Knotens wird durch einen directml-Operator definiert.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax
```cpp
struct DML_OPERATOR_GRAPH_NODE_DESC {
  IDMLOperator *Operator;
  const char   *Name;
};
```



## <a name="members"></a>Member

`Operator`

Typ: <b> [idmloperator](/windows/win32/api/directml/nn-directml-idmloperator)*</b>

Ein directml-Operator, der das Verhalten des Knotens definiert.


`Name`

Typ: \_ Field \_ z \_ \_ maybenull \_ **Konstanten \*** Zeichen

Ein optionaler Name für die Diagramm Verbindung. Wenn bereitgestellt, kann dies in bestimmten Fehlermeldungen verwendet werden, die von der directml-debugschicht ausgegeben werden.

## <a name="availability"></a>Verfügbarkeit

Diese API wurde in der directml-Version eingeführt `1.1.0` .



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |

## <a name="see-also"></a>Siehe auch

* [IDMLDevice1:: compilegraph-Methode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC Struktur](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [DML_GRAPH_NODE_DESC Struktur](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)