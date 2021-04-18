---
UID: NS:directml.DML_OUTPUT_GRAPH_EDGE_DESC
title: DML_OUTPUT_GRAPH_EDGE_DESC
description: 'Beschreibt eine Verbindung innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden. Diese Struktur wird verwendet, um eine Verbindung zwischen einer Ausgabe eines internen Knotens und einer Diagramm Ausgabe zu definieren.'
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
ms.openlocfilehash: d1d48de0fa3bf2665269ebf2226de4e9911a1670
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106371812"
---
# <a name="dml_output_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="c33d3-104">DML_OUTPUT_GRAPH_EDGE_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="c33d3-104">DML_OUTPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="c33d3-105">Beschreibt eine Verbindung innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c33d3-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="c33d3-106">Diese Struktur wird verwendet, um eine Verbindung zwischen einer Ausgabe eines internen Knotens und einer Diagramm Ausgabe zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c33d3-106">This structure is used to define a connection from an output of an internal node to a graph output.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c33d3-107">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="c33d3-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="c33d3-108">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c33d3-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c33d3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c33d3-109">Syntax</span></span>
```cpp
struct DML_OUTPUT_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       GraphOutputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="c33d3-110">Member</span><span class="sxs-lookup"><span data-stu-id="c33d3-110">Members</span></span>

`FromNodeIndex`




`FromNodeOutputIndex`




`GraphOutputIndex`

<span data-ttu-id="c33d3-111">Typ: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c33d3-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="c33d3-112">Der Index der Diagramm Ausgabe, für die eine Verbindung aus einer internen Knoten Ausgabe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c33d3-112">The index of the graph output to which a connection from an internal node output is specified.</span></span>


`Name`

<span data-ttu-id="c33d3-113">Typ: \_ Field \_ z \_ \_ maybenull \_ **Konstanten \*** Zeichen</span><span class="sxs-lookup"><span data-stu-id="c33d3-113">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="c33d3-114">Ein optionaler Name für die Diagramm Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c33d3-114">An optional name for the graph connection.</span></span> <span data-ttu-id="c33d3-115">Wenn bereitgestellt, kann dies in bestimmten Fehlermeldungen verwendet werden, die von der directml-debugschicht ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c33d3-115">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="c33d3-116">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="c33d3-116">Availability</span></span>

<span data-ttu-id="c33d3-117">Diese API wurde in der directml-Version eingeführt `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="c33d3-117">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="c33d3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c33d3-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c33d3-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="c33d3-119">**Header**</span></span> | <span data-ttu-id="c33d3-120">directml. h</span><span class="sxs-lookup"><span data-stu-id="c33d3-120">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="c33d3-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c33d3-121">See also</span></span>

* [<span data-ttu-id="c33d3-122">IDMLDevice1:: compilegraph-Methode</span><span class="sxs-lookup"><span data-stu-id="c33d3-122">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="c33d3-123">DML_GRAPH_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="c33d3-123">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="c33d3-124">DML_GRAPH_EDGE_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="c33d3-124">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)