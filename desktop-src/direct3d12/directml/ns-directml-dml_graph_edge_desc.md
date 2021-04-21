---
UID: NS:directml.DML_GRAPH_EDGE_DESC
title: DML_GRAPH_EDGE_DESC
description: Ein generischer Container für eine Verbindung innerhalb eines Graphen von DirectML-Operatoren, die durch [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) definiert und an [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.
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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802914"
---
# <a name="dml_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="fd74c-103">DML_GRAPH_EDGE_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="fd74c-103">DML_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="fd74c-104">Ein generischer Container für eine Verbindung innerhalb eines Graphen von DirectML-Operatoren, die durch [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) definiert und an [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="fd74c-104">A generic container for a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd74c-105">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="fd74c-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="fd74c-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="fd74c-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd74c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd74c-107">Syntax</span></span>
```cpp
struct DML_GRAPH_EDGE_DESC {
  DML_GRAPH_EDGE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a><span data-ttu-id="fd74c-108">Member</span><span class="sxs-lookup"><span data-stu-id="fd74c-108">Members</span></span>

`Type`

<span data-ttu-id="fd74c-109">Typ: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span><span class="sxs-lookup"><span data-stu-id="fd74c-109">Type: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span></span>

<span data-ttu-id="fd74c-110">Der Typ des Graphrands.</span><span class="sxs-lookup"><span data-stu-id="fd74c-110">The type of graph edge.</span></span> <span data-ttu-id="fd74c-111">Unter [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) finden Sie verfügbare Typen und [DML_GRAPH_DESC,](./ns-directml-dml_graph_desc.md) wo die einzelnen Typen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fd74c-111">See [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) for available types, and [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) for where to use each type.</span></span>


`Desc`

<span data-ttu-id="fd74c-112">Typ: \_ \_ Feldgröße \_ ( \_ Unausdruckbar \_ ("Abhängig vom Edgetyp")) **const void \***</span><span class="sxs-lookup"><span data-stu-id="fd74c-112">Type: \_Field\_size\_(\_Inexpressible\_("Dependent on edge type")) **const void\***</span></span>

<span data-ttu-id="fd74c-113">Ein Zeiger auf die Graph-Edgebeschreibung.</span><span class="sxs-lookup"><span data-stu-id="fd74c-113">A pointer to the graph edge description.</span></span> <span data-ttu-id="fd74c-114">Der Typ der Struktur, auf die gezeigt wird, muss mit dem in *Typ* angegebenen Wert übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="fd74c-114">The type of the pointed-to struct must match the value specified in *Type*.</span></span>

## <a name="availability"></a><span data-ttu-id="fd74c-115">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="fd74c-115">Availability</span></span>

<span data-ttu-id="fd74c-116">Diese API wurde in DirectML-Version `1.1.0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fd74c-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="fd74c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd74c-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fd74c-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="fd74c-118">**Header**</span></span> | <span data-ttu-id="fd74c-119">directml.h</span><span class="sxs-lookup"><span data-stu-id="fd74c-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="fd74c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd74c-120">See also</span></span>

* [<span data-ttu-id="fd74c-121">IDMLDevice1::CompileGraph-Methode</span><span class="sxs-lookup"><span data-stu-id="fd74c-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="fd74c-122">DML_GRAPH_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="fd74c-122">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)