---
UID: NS:directml.DML_OUTPUT_GRAPH_EDGE_DESC
title: DML_OUTPUT_GRAPH_EDGE_DESC
description: Beschreibt eine Verbindung innerhalb eines Graphen von DirectML-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden. Diese Struktur wird verwendet, um eine Verbindung zwischen einer Ausgabe eines internen Knotens und einer Graphausgabe zu definieren.
helpviewer_keywords:
- DML_OUTPUT_GRAPH_EDGE_DESC
- DML_OUTPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_output_graph_edge_desc
- directml/DML_OUTPUT_GRAPH_EDGE_DESC
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
- DML_OUTPUT_GRAPH_EDGE_DESC
- directml/DML_OUTPUT_GRAPH_EDGE_DESC
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
- DML_OUTPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: 55d234fcf487e7ad92b39b60d43eb992b46d0d2c
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417229"
---
# <a name="dml_output_graph_edge_desc-structure-directmlh"></a>DML_OUTPUT_GRAPH_EDGE_DESC-Struktur (directml.h)
Beschreibt eine Verbindung innerhalb eines Graphen von DirectML-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden. Diese Struktur wird verwendet, um eine Verbindung zwischen einer Ausgabe eines internen Knotens und einer Graphausgabe zu definieren.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_OUTPUT_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       GraphOutputIndex;
  const char *Name;
};
```



## <a name="members"></a>Member

`FromNodeIndex`




`FromNodeOutputIndex`




`GraphOutputIndex`

Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**

Der Index der Graphausgabe, mit der eine Verbindung von einer internen Knotenausgabe angegeben wird.


`Name`

Typ: \_ Feld \_ z \_ \_ Maybenull \_ **const char \***

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