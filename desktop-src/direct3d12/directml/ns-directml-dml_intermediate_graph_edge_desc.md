---
UID: NS:directml.DML_INTERMEDIATE_GRAPH_EDGE_DESC
title: DML_INTERMEDIATE_GRAPH_EDGE_DESC
description: 'Beschreibt eine Verbindung innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden. Diese Struktur wird verwendet, um eine Verbindung zwischen internen Knoten zu definieren.'
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
ms.openlocfilehash: 55b8385d3d8b6247681dd7078a04d8f5e196abd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106371815"
---
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a>DML_INTERMEDIATE_GRAPH_EDGE_DESC-Struktur (directml. h)
Beschreibt eine Verbindung innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden. Diese Struktur wird verwendet, um eine Verbindung zwischen internen Knoten zu definieren.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: **[uint](/windows/desktop/winprog/windows-data-types)**

Der Index des Graph-Knotens, von dem eine Verbindung mit einem anderen Knoten angegeben wird.


`FromNodeOutputIndex`

Typ: **[uint](/windows/desktop/winprog/windows-data-types)**

Der Index der Ausgabe auf dem Knoten bei Index *fromnodeindex* , an dem die Verbindung angegeben ist.


`ToNodeIndex`

Typ: **[uint](/windows/desktop/winprog/windows-data-types)**

Der Index des Graph-Knotens, in dem eine Verbindung von einem anderen Knoten angegeben wird.


`ToNodeInputIndex`

Typ: **[uint](/windows/desktop/winprog/windows-data-types)**

Der Index der Eingabe auf dem Knoten beim Index *tonodeindex* , an dem die Verbindung angegeben ist.


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
* [DML_GRAPH_EDGE_DESC Struktur](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)