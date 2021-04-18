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
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="fd314-104">DML_INTERMEDIATE_GRAPH_EDGE_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="fd314-104">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="fd314-105">Beschreibt eine Verbindung innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="fd314-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="fd314-106">Diese Struktur wird verwendet, um eine Verbindung zwischen internen Knoten zu definieren.</span><span class="sxs-lookup"><span data-stu-id="fd314-106">This structure is used to define a connection between internal nodes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd314-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="fd314-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="fd314-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fd314-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd314-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd314-109">Syntax</span></span>
```cpp
struct DML_INTERMEDIATE_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="fd314-110">Member</span><span class="sxs-lookup"><span data-stu-id="fd314-110">Members</span></span>

`FromNodeIndex`

<span data-ttu-id="fd314-111">Typ: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fd314-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="fd314-112">Der Index des Graph-Knotens, von dem eine Verbindung mit einem anderen Knoten angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd314-112">The index of the graph node from which a connection to another node is specified.</span></span>


`FromNodeOutputIndex`

<span data-ttu-id="fd314-113">Typ: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fd314-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="fd314-114">Der Index der Ausgabe auf dem Knoten bei Index *fromnodeindex* , an dem die Verbindung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fd314-114">The index of the output on the node at index *FromNodeIndex* where the connection is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="fd314-115">Typ: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fd314-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="fd314-116">Der Index des Graph-Knotens, in dem eine Verbindung von einem anderen Knoten angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd314-116">The index of the graph node into which a connection from another node is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="fd314-117">Typ: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fd314-117">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="fd314-118">Der Index der Eingabe auf dem Knoten beim Index *tonodeindex* , an dem die Verbindung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fd314-118">The index of the input on the node at index *ToNodeIndex* where the connection is specified.</span></span>


`Name`

<span data-ttu-id="fd314-119">Typ: \_ Field \_ z \_ \_ maybenull \_ **Konstanten \*** Zeichen</span><span class="sxs-lookup"><span data-stu-id="fd314-119">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="fd314-120">Ein optionaler Name für die Diagramm Verbindung.</span><span class="sxs-lookup"><span data-stu-id="fd314-120">An optional name for the graph connection.</span></span> <span data-ttu-id="fd314-121">Wenn bereitgestellt, kann dies in bestimmten Fehlermeldungen verwendet werden, die von der directml-debugschicht ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fd314-121">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="fd314-122">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="fd314-122">Availability</span></span>

<span data-ttu-id="fd314-123">Diese API wurde in der directml-Version eingeführt `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="fd314-123">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="fd314-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd314-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fd314-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="fd314-125">**Header**</span></span> | <span data-ttu-id="fd314-126">directml. h</span><span class="sxs-lookup"><span data-stu-id="fd314-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="fd314-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd314-127">See also</span></span>

* [<span data-ttu-id="fd314-128">IDMLDevice1:: compilegraph-Methode</span><span class="sxs-lookup"><span data-stu-id="fd314-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="fd314-129">DML_GRAPH_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="fd314-129">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="fd314-130">DML_GRAPH_EDGE_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="fd314-130">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)