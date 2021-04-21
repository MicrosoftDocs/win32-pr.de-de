---
UID: NS:directml.DML_INPUT_GRAPH_EDGE_DESC
title: DML_INPUT_GRAPH_EDGE_DESC
description: Beschreibt eine Verbindung in einem Diagramm von [](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) DirectML-Operatoren, die durch DML_GRAPH_DESC definiert und an [IDMLDevice1::CompileGraph übergeben werden.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph) Diese Struktur wird verwendet, um eine Verbindung von einer Grapheingabe mit einer Eingabe eines internen Knotens zu definieren.
helpviewer_keywords:
- DML_INPUT_GRAPH_EDGE_DESC
- DML_INPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_input_graph_edge_desc
- directml/DML_INPUT_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INPUT_GRAPH_EDGE_DESC, DML_INPUT_GRAPH_EDGE_DESC structure, direct3d12.dml_input_graph_edge_desc, directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
- directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: 00fcece76f4cb7ac46589914df4d74321d957fbc
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802888"
---
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a>DML_INPUT_GRAPH_EDGE_DESC -Struktur (directml.h)
Beschreibt eine Verbindung in einem Diagramm von DirectML-Operatoren, die durch DML_GRAPH_DESC definiert und [an](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) [IDMLDevice1::CompileGraph übergeben werden.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph) Diese Struktur wird verwendet, um eine Verbindung von einer Grapheingabe mit einer Eingabe eines internen Knotens zu definieren.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a>Member

`GraphInputIndex`

Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**

Der Index der Grapheingabe, aus der eine Verbindung mit einer internen Knoteneingabe angegeben wird.


`ToNodeIndex`

Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**

Der Index des internen Knotens, für den die Verbindung aus der Grapheingabe angegeben wird.


`ToNodeInputIndex`

Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**

Der Index der Eingabe auf dem internen Knoten, auf dem die Verbindung angegeben ist.


`Name`

Typ: \_ Feld \_ z \_ \_ Maybenull const \_ **char \***

Ein optionaler Name für die Graphverbindung. Falls angegeben, kann dies in bestimmten Fehlermeldungen verwendet werden, die von der DirectML-Debugebene ausgegeben werden.

## <a name="availability"></a>Verfügbarkeit

Diese API wurde in der DirectML-Version `1.1.0` eingeführt.



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Siehe auch

* [IDMLDevice1::CompileGraph-Methode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC-Struktur](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [DML_GRAPH_EDGE_DESC Struktur](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)