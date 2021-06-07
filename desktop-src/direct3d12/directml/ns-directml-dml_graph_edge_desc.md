---
UID: NS:directml.DML_GRAPH_EDGE_DESC
title: DML_GRAPH_EDGE_DESC
description: Ein generischer Container für eine Verbindung innerhalb eines Graphen von [DirectML-Operatoren,](./ns-directml-dml_graph_desc.md) die durch DML_GRAPH_DESC definiert und an [IDMLDevice1::CompileGraph übergeben werden.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
helpviewer_keywords:
- DML_GRAPH_EDGE_DESC
- DML_GRAPH_EDGE_DESC structure
- direct3d12.dml_graph_edge_desc
- directml/DML_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_DESC, DML_GRAPH_EDGE_DESC structure, direct3d12.dml_graph_edge_desc, directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
- directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
ms.openlocfilehash: 58cdf22dd85b1464d68cf1db75ff47a34817514c
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417791"
---
# <a name="dml_graph_edge_desc-structure-directmlh"></a>DML_GRAPH_EDGE_DESC -Struktur (directml.h)
Ein generischer Container für eine Verbindung innerhalb eines Graphen von [DirectML-Operatoren,](./ns-directml-dml_graph_desc.md) die durch DML_GRAPH_DESC definiert und an [IDMLDevice1::CompileGraph übergeben werden.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_GRAPH_EDGE_DESC {
  DML_GRAPH_EDGE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a>Member

`Type`

Typ: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**

Der Typ des Diagrammrands. Unter [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) finden Sie informationen zu verfügbaren Typen und [DML_GRAPH_DESC,](./ns-directml-dml_graph_desc.md) wo die einzelnen Typen verwendet werden sollten.


`Desc`

Typ: \_ \_ Feldgröße \_ ( \_ Inexpressible \_ ("Abhängig vom Edgetyp")) **const void \***

Ein Zeiger auf die Graphenrandbeschreibung. Der Typ der Struktur, auf die verwiesen wird, muss mit dem in Typ angegebenen *Wert übereinstimmen.*

## <a name="availability"></a>Verfügbarkeit

Diese API wurde in der DirectML-Version `1.1.0` eingeführt.



## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Siehe auch

* [IDMLDevice1::CompileGraph-Methode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC-Struktur](./ns-directml-dml_graph_desc.md)