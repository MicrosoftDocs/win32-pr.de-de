---
UID: NS:directml.DML_GRAPH_EDGE_DESC
title: DML_GRAPH_EDGE_DESC
description: 'Ein generischer Container für eine Verbindung innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.'
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
ms.openlocfilehash: 636556cec6fa9982ea1a30e02f6019f93b815cf8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106367264"
---
# <a name="dml_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="abca2-103">DML_GRAPH_EDGE_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="abca2-103">DML_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="abca2-104">Ein generischer Container für eine Verbindung innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="abca2-104">A generic container for a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abca2-105">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="abca2-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="abca2-106">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="abca2-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="abca2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="abca2-107">Syntax</span></span>
```cpp
struct DML_GRAPH_EDGE_DESC {
  DML_GRAPH_EDGE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a><span data-ttu-id="abca2-108">Member</span><span class="sxs-lookup"><span data-stu-id="abca2-108">Members</span></span>

`Type`

<span data-ttu-id="abca2-109">Typ: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span><span class="sxs-lookup"><span data-stu-id="abca2-109">Type: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span></span>

<span data-ttu-id="abca2-110">Der Typ der Diagramm Kante.</span><span class="sxs-lookup"><span data-stu-id="abca2-110">The type of graph edge.</span></span> <span data-ttu-id="abca2-111">Weitere Informationen finden Sie unter [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) für verfügbare Typen und [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) , wo die einzelnen Typen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="abca2-111">See [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) for available types, and [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) for where to use each type.</span></span>


`Desc`

<span data-ttu-id="abca2-112">Type: \_ Field \_ size \_ (ungültig \_ \_ ("abhängig von Edge-Typ")) Konstante **void \***</span><span class="sxs-lookup"><span data-stu-id="abca2-112">Type: \_Field\_size\_(\_Inexpressible\_("Dependent on edge type")) **const void\***</span></span>

<span data-ttu-id="abca2-113">Ein Zeiger auf die Diagramm Kanten Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="abca2-113">A pointer to the graph edge description.</span></span> <span data-ttu-id="abca2-114">Der Typ der Pointto-Struktur muss mit dem in *Type* angegebenen Wert identisch sein.</span><span class="sxs-lookup"><span data-stu-id="abca2-114">The type of the pointed-to struct must match the value specified in *Type*.</span></span>

## <a name="availability"></a><span data-ttu-id="abca2-115">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="abca2-115">Availability</span></span>

<span data-ttu-id="abca2-116">Diese API wurde in der directml-Version eingeführt `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="abca2-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="abca2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abca2-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="abca2-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="abca2-118">**Header**</span></span> | <span data-ttu-id="abca2-119">directml. h</span><span class="sxs-lookup"><span data-stu-id="abca2-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="abca2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abca2-120">See also</span></span>

* [<span data-ttu-id="abca2-121">IDMLDevice1:: compilegraph-Methode</span><span class="sxs-lookup"><span data-stu-id="abca2-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="abca2-122">DML_GRAPH_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="abca2-122">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)