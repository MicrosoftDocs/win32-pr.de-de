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
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="4ee95-104">DML_INPUT_GRAPH_EDGE_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="4ee95-104">DML_INPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="4ee95-105">Beschreibt eine Verbindung in einem Diagramm von DirectML-Operatoren, die durch DML_GRAPH_DESC definiert und [an](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) [IDMLDevice1::CompileGraph übergeben werden.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="4ee95-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="4ee95-106">Diese Struktur wird verwendet, um eine Verbindung von einer Grapheingabe mit einer Eingabe eines internen Knotens zu definieren.</span><span class="sxs-lookup"><span data-stu-id="4ee95-106">This structure is used to define a connection from a graph input to an input of an internal node.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ee95-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="4ee95-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4ee95-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="4ee95-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee95-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ee95-109">Syntax</span></span>
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="4ee95-110">Member</span><span class="sxs-lookup"><span data-stu-id="4ee95-110">Members</span></span>

`GraphInputIndex`

<span data-ttu-id="4ee95-111">Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4ee95-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="4ee95-112">Der Index der Grapheingabe, aus der eine Verbindung mit einer internen Knoteneingabe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4ee95-112">The index of the graph input from which a connection to an internal node input is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="4ee95-113">Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4ee95-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="4ee95-114">Der Index des internen Knotens, für den die Verbindung aus der Grapheingabe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4ee95-114">The index of the internal node onto which the connection from the graph input is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="4ee95-115">Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4ee95-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="4ee95-116">Der Index der Eingabe auf dem internen Knoten, auf dem die Verbindung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4ee95-116">The index of the input on the internal node where the connection is specified.</span></span>


`Name`

<span data-ttu-id="4ee95-117">Typ: \_ Feld \_ z \_ \_ Maybenull const \_ **char \***</span><span class="sxs-lookup"><span data-stu-id="4ee95-117">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="4ee95-118">Ein optionaler Name für die Graphverbindung.</span><span class="sxs-lookup"><span data-stu-id="4ee95-118">An optional name for the graph connection.</span></span> <span data-ttu-id="4ee95-119">Falls angegeben, kann dies in bestimmten Fehlermeldungen verwendet werden, die von der DirectML-Debugebene ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4ee95-119">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="4ee95-120">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="4ee95-120">Availability</span></span>

<span data-ttu-id="4ee95-121">Diese API wurde in der DirectML-Version `1.1.0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4ee95-121">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="4ee95-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ee95-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4ee95-123">**Header**</span><span class="sxs-lookup"><span data-stu-id="4ee95-123">**Header**</span></span> | <span data-ttu-id="4ee95-124">directml.h</span><span class="sxs-lookup"><span data-stu-id="4ee95-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="4ee95-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ee95-125">See also</span></span>

* [<span data-ttu-id="4ee95-126">IDMLDevice1::CompileGraph-Methode</span><span class="sxs-lookup"><span data-stu-id="4ee95-126">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="4ee95-127">DML_GRAPH_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="4ee95-127">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="4ee95-128">DML_GRAPH_EDGE_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="4ee95-128">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)