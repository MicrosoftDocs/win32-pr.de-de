---
UID: NS:directml.DML_INTERMEDIATE_GRAPH_EDGE_DESC
title: DML_INTERMEDIATE_GRAPH_EDGE_DESC
description: Beschreibt eine Verbindung in einem Diagramm von [](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) DirectML-Operatoren, die durch DML_GRAPH_DESC definiert und an [IDMLDevice1::CompileGraph übergeben werden.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph) Diese Struktur wird verwendet, um eine Verbindung zwischen internen Knoten zu definieren.
helpviewer_keywords:
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- DML_INTERMEDIATE_GRAPH_EDGE_DESC structure
- direct3d12.dml_intermediate_graph_edge_desc
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INTERMEDIATE_GRAPH_EDGE_DESC, DML_INTERMEDIATE_GRAPH_EDGE_DESC structure, direct3d12.dml_intermediate_graph_edge_desc, directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.openlocfilehash: 17cf62def075e84ba86e97a5adfa48fb452f475e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417174"
---
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a>DML_INTERMEDIATE_GRAPH_EDGE_DESC -Struktur (directml.h)
Beschreibt eine Verbindung in einem Diagramm von [](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) DirectML-Operatoren, die durch DML_GRAPH_DESC definiert und an [IDMLDevice1::CompileGraph übergeben werden.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph) Diese Struktur wird verwendet, um eine Verbindung zwischen internen Knoten zu definieren.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_INTERMEDIATE_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a>Member

`FromNodeIndex`

Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**

Der Index des Graphknotens, von dem aus eine Verbindung mit einem anderen Knoten angegeben wird.


`FromNodeOutputIndex`

Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**

Der Index der Ausgabe auf dem Knoten am *Index FromNodeIndex,* an dem die Verbindung angegeben ist.


`ToNodeIndex`

Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**

Der Index des Graphknotens, in den eine Verbindung von einem anderen Knoten angegeben wird.


`ToNodeInputIndex`

Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**

Der Index der Eingabe auf dem Knoten am *Index ToNodeIndex,* an dem die Verbindung angegeben wird.


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
* [DML_GRAPH_EDGE_DESC-Struktur](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)