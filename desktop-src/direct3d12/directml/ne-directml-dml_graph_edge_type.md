---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Definiert Konstanten, die einen Typ des Graphenrands angeben. Informationen [zur DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) Enumeration finden Sie unter DML_GRAPH_EDGE_DESC.
helpviewer_keywords:
- DML_GRAPH_EDGE_TYPE
- DML_GRAPH_EDGE_TYPE structure
- direct3d12.dml_graph_edge_type
- directml/DML_GRAPH_EDGE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
- directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
ms.openlocfilehash: d65649fcd2115cc7cdcc1b01da20ef44b0436e6f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417919"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a><span data-ttu-id="b0563-104">DML_GRAPH_EDGE_TYPE -Enumeration (directml.h)</span><span class="sxs-lookup"><span data-stu-id="b0563-104">DML_GRAPH_EDGE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="b0563-105">Definiert Konstanten, die einen Typ des Graphenrands angeben.</span><span class="sxs-lookup"><span data-stu-id="b0563-105">Defines constants that specify a type of graph edge.</span></span> <span data-ttu-id="b0563-106">Informationen [zur DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) Enumeration finden Sie unter DML_GRAPH_EDGE_DESC.</span><span class="sxs-lookup"><span data-stu-id="b0563-106">See [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0563-107">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="b0563-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b0563-108">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="b0563-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0563-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0563-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a><span data-ttu-id="b0563-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b0563-110">Constants</span></span>

| <span data-ttu-id="b0563-111">Name</span><span class="sxs-lookup"><span data-stu-id="b0563-111">Name</span></span> | <span data-ttu-id="b0563-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0563-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="b0563-113">DML_GRAPH_EDGE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="b0563-113">DML_GRAPH_EDGE_TYPE_INVALID</span></span> | <span data-ttu-id="b0563-114">Gibt einen unbekannten Graphenrandtyp an und ist nie gültig.</span><span class="sxs-lookup"><span data-stu-id="b0563-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="b0563-115">Die Verwendung dieses Werts führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="b0563-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="b0563-116">DML_GRAPH_EDGE_TYPE_INPUT</span><span class="sxs-lookup"><span data-stu-id="b0563-116">DML_GRAPH_EDGE_TYPE_INPUT</span></span> | <span data-ttu-id="b0563-117">Gibt an, dass der Graphrand von der -Struktur [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) wird.</span><span class="sxs-lookup"><span data-stu-id="b0563-117">Specifies that the graph edge is described by the [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="b0563-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0563-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span></span> | <span data-ttu-id="b0563-119">Gibt an, dass der Graphrand von der -Struktur [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) wird.</span><span class="sxs-lookup"><span data-stu-id="b0563-119">Specifies that the graph edge is described by the [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="b0563-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span><span class="sxs-lookup"><span data-stu-id="b0563-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span></span> | <span data-ttu-id="b0563-121">Gibt an, dass der Graphrand von der -Struktur [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) wird.</span><span class="sxs-lookup"><span data-stu-id="b0563-121">Specifies that the graph edge is described by the [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) structure.</span></span><br><br><span data-ttu-id="b0563-122">##-Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="b0563-122">## Availability</span></span><br><br><span data-ttu-id="b0563-123">Diese API wurde in der DirectML-Version `1.1.0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b0563-123">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="b0563-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b0563-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b0563-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="b0563-125">**Header**</span></span> | <span data-ttu-id="b0563-126">directml.h</span><span class="sxs-lookup"><span data-stu-id="b0563-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="b0563-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0563-127">See also</span></span>

* [<span data-ttu-id="b0563-128">IDMLDevice1::CompileGraph-Methode</span><span class="sxs-lookup"><span data-stu-id="b0563-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="b0563-129">DML_GRAPH_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="b0563-129">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="b0563-130">DML_GRAPH_EDGE_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="b0563-130">DML_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_graph_edge_desc.md)
* [<span data-ttu-id="b0563-131">DML_INPUT_GRAPH_EDGE_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="b0563-131">DML_INPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_input_graph_edge_desc.md)
* [<span data-ttu-id="b0563-132">DML_OUTPUT_GRAPH_EDGE_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="b0563-132">DML_OUTPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_output_graph_edge_desc.md)
* [<span data-ttu-id="b0563-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="b0563-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_intermediate_graph_edge_desc.md)