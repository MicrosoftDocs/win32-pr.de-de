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
# <a name="dml_output_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="ba72b-104">DML_OUTPUT_GRAPH_EDGE_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="ba72b-104">DML_OUTPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="ba72b-105">Beschreibt eine Verbindung innerhalb eines Graphen von DirectML-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ba72b-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="ba72b-106">Diese Struktur wird verwendet, um eine Verbindung zwischen einer Ausgabe eines internen Knotens und einer Graphausgabe zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ba72b-106">This structure is used to define a connection from an output of an internal node to a graph output.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba72b-107">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="ba72b-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ba72b-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="ba72b-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ba72b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba72b-109">Syntax</span></span>
```cpp
struct DML_OUTPUT_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       GraphOutputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="ba72b-110">Member</span><span class="sxs-lookup"><span data-stu-id="ba72b-110">Members</span></span>

`FromNodeIndex`




`FromNodeOutputIndex`




`GraphOutputIndex`

<span data-ttu-id="ba72b-111">Typ: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ba72b-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ba72b-112">Der Index der Graphausgabe, mit der eine Verbindung von einer internen Knotenausgabe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba72b-112">The index of the graph output to which a connection from an internal node output is specified.</span></span>


`Name`

<span data-ttu-id="ba72b-113">Typ: \_ Feld \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="ba72b-113">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="ba72b-114">Ein optionaler Name für die Graphverbindung.</span><span class="sxs-lookup"><span data-stu-id="ba72b-114">An optional name for the graph connection.</span></span> <span data-ttu-id="ba72b-115">Falls angegeben, kann dies in bestimmten Fehlermeldungen verwendet werden, die von der DirectML-Debugebene ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ba72b-115">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="ba72b-116">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ba72b-116">Availability</span></span>

<span data-ttu-id="ba72b-117">Diese API wurde in der DirectML-Version `1.1.0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ba72b-117">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="ba72b-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ba72b-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ba72b-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="ba72b-119">**Header**</span></span> | <span data-ttu-id="ba72b-120">directml.h</span><span class="sxs-lookup"><span data-stu-id="ba72b-120">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ba72b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba72b-121">See also</span></span>

* [<span data-ttu-id="ba72b-122">IDMLDevice1::CompileGraph-Methode</span><span class="sxs-lookup"><span data-stu-id="ba72b-122">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="ba72b-123">DML_GRAPH_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="ba72b-123">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="ba72b-124">DML_GRAPH_EDGE_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="ba72b-124">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)