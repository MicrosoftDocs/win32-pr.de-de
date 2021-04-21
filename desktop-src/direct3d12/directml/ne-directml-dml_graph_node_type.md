---
UID: NE:directml.DML_GRAPH_NODE_TYPE
title: DML_GRAPH_NODE_TYPE
description: Definiert Konstanten, die einen Graphknotentyp angeben. Informationen [zur DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) Enumeration finden Sie unter DML_GRAPH_NODE_DESC.
helpviewer_keywords:
- DML_GRAPH_NODE_TYPE
- DML_GRAPH_NODE_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_GRAPH_NODE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_TYPE, DML_GRAPH_NODE_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
- directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
ms.openlocfilehash: 0bb0712370da35c4b8c9278ad7721d2ffc7d875d
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803681"
---
# <a name="dml_graph_node_type-enumeration-directmlh"></a><span data-ttu-id="071db-104">DML_GRAPH_NODE_TYPE -Enumeration (directml.h)</span><span class="sxs-lookup"><span data-stu-id="071db-104">DML_GRAPH_NODE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="071db-105">Definiert Konstanten, die einen Graphknotentyp angeben.</span><span class="sxs-lookup"><span data-stu-id="071db-105">Defines constants that specify a type of graph node.</span></span> <span data-ttu-id="071db-106">Informationen [zur DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) Enumeration finden Sie unter DML_GRAPH_NODE_DESC.</span><span class="sxs-lookup"><span data-stu-id="071db-106">See [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="071db-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="071db-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="071db-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="071db-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="071db-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="071db-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_NODE_TYPE {
  DML_GRAPH_NODE_TYPE_INVALID,
  DML_GRAPH_NODE_TYPE_OPERATOR
} ;
```

## <a name="constants"></a><span data-ttu-id="071db-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="071db-110">Constants</span></span>

| <span data-ttu-id="071db-111">Name</span><span class="sxs-lookup"><span data-stu-id="071db-111">Name</span></span> | <span data-ttu-id="071db-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="071db-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="071db-113">DML_GRAPH_NODE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="071db-113">DML_GRAPH_NODE_TYPE_INVALID</span></span> | <span data-ttu-id="071db-114">Gibt einen unbekannten Graphenrandtyp an und ist nie gültig.</span><span class="sxs-lookup"><span data-stu-id="071db-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="071db-115">Die Verwendung dieses Werts führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="071db-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="071db-116">DML_GRAPH_NODE_TYPE_OPERATOR</span><span class="sxs-lookup"><span data-stu-id="071db-116">DML_GRAPH_NODE_TYPE_OPERATOR</span></span> | <span data-ttu-id="071db-117">Gibt an, dass der Graphrand von der -Struktur [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) wird.</span><span class="sxs-lookup"><span data-stu-id="071db-117">Specifies that the graph edge is described by the [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) structure.</span></span><br><br><span data-ttu-id="071db-118">##-Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="071db-118">## Availability</span></span><br><br><span data-ttu-id="071db-119">Diese API wurde in der DirectML-Version `1.1.0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="071db-119">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="071db-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="071db-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="071db-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="071db-121">**Header**</span></span> | <span data-ttu-id="071db-122">directml.h</span><span class="sxs-lookup"><span data-stu-id="071db-122">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="071db-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="071db-123">See also</span></span>

* [<span data-ttu-id="071db-124">IDMLDevice1::CompileGraph-Methode</span><span class="sxs-lookup"><span data-stu-id="071db-124">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="071db-125">DML_GRAPH_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="071db-125">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="071db-126">DML_GRAPH_NODE_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="071db-126">DML_GRAPH_NODE_DESC structure</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="071db-127">DML_OPERATOR_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="071db-127">DML_OPERATOR_GRAPH_NODE_DESC</span></span>](./ns-directml-dml_operator_graph_node_desc.md)