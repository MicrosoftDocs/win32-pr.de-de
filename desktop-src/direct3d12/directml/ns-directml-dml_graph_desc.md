---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Beschreibt ein Diagramm von DirectML-Operatoren, die zum Kompilieren eines kombinierten, optimierten Operators verwendet werden.
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
ms.openlocfilehash: a42996fc9fd7825e13232b245ab764c6439f9489
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802883"
---
# <a name="dml_graph_desc-structure-directmlh"></a><span data-ttu-id="9f2b4-103">DML_GRAPH_DESC -Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="9f2b4-103">DML_GRAPH_DESC structure (directml.h)</span></span>

<span data-ttu-id="9f2b4-104">Beschreibt ein Diagramm von DirectML-Operatoren, die zum Kompilieren eines kombinierten, optimierten Operators verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-104">Describes a graph of DirectML operators used to compile a combined, optimized operator.</span></span> <span data-ttu-id="9f2b4-105">Siehe [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="9f2b4-105">See [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f2b4-106">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="9f2b4-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="9f2b4-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="9f2b4-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f2b4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f2b4-108">Syntax</span></span>
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a><span data-ttu-id="9f2b4-109">Member</span><span class="sxs-lookup"><span data-stu-id="9f2b4-109">Members</span></span>

`InputCount`

<span data-ttu-id="9f2b4-110">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="9f2b4-110">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="9f2b4-111">Die Anzahl der Eingaben des Gesamtdiagramms.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-111">The number of inputs of the overall graph.</span></span> <span data-ttu-id="9f2b4-112">Jede Grapheingabe kann mit einer variablen Anzahl interner Knoten verbunden sein, daher kann sich dies von *InputEdgeCount unterscheiden.*</span><span class="sxs-lookup"><span data-stu-id="9f2b4-112">Each graph input may be connected to a variable number of internal nodes, therefore this may be different from *InputEdgeCount*.</span></span>


`OutputCount`

<span data-ttu-id="9f2b4-113">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="9f2b4-113">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="9f2b4-114">Die Anzahl der Ausgaben des Gesamtdiagramms.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-114">The number of outputs of the overall graph.</span></span> <span data-ttu-id="9f2b4-115">Jede Graphausgabe kann mit einer variablen Anzahl interner Knoten verbunden sein, daher kann sich dies von *OutputEdgeCount unterscheiden.*</span><span class="sxs-lookup"><span data-stu-id="9f2b4-115">Each graph output may be connected to a variable number of internal nodes, therefore this may be different from *OutputEdgeCount*.</span></span>


`NodeCount`

<span data-ttu-id="9f2b4-116">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="9f2b4-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="9f2b4-117">Die Anzahl der internen Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-117">The number of internal nodes in the graph.</span></span>


`Nodes`

<span data-ttu-id="9f2b4-118">Typ: \_ \_ Feldgröße \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f2b4-118">Type: \_Field\_size\_(NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)\***</span></span>

<span data-ttu-id="9f2b4-119">Die internen Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-119">The internal nodes in the graph.</span></span>


`InputEdgeCount`

<span data-ttu-id="9f2b4-120">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="9f2b4-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="9f2b4-121">Die Anzahl der Verbindungen zwischen Grapheingaben und Eingaben interner Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-121">The number of connections between graph inputs and inputs of internal nodes in the graph.</span></span>


`InputEdges`

<span data-ttu-id="9f2b4-122">Typ: \_ \_ Feldgröße \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f2b4-122">Type: \_Field\_size\_(InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="9f2b4-123">Ein Array von Verbindungen zwischen Grapheingaben und Eingaben interner Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-123">An array of connections between graph inputs and inputs of internal nodes in the graph.</span></span> <span data-ttu-id="9f2b4-124">Das *Feld Type* innerhalb jedes Elements sollte auf [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-124">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`OutputEdgeCount`

<span data-ttu-id="9f2b4-125">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="9f2b4-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="9f2b4-126">Die Anzahl der Verbindungen zwischen Graphausgaben und Ausgaben interner Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-126">The number of connections between graph outputs and outputs of internal nodes in the graph.</span></span>


`OutputEdges`

<span data-ttu-id="9f2b4-127">Typ: \_ \_ Feldgröße \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f2b4-127">Type: \_Field\_size\_(OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="9f2b4-128">Ein Array von Verbindungen zwischen Graphausgaben und Ausgaben interner Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-128">An array of connections between graph outputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="9f2b4-129">Das *Feld Type* innerhalb jedes Elements sollte auf [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-129">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`IntermediateEdgeCount`

<span data-ttu-id="9f2b4-130">Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="9f2b4-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="9f2b4-131">Die Anzahl der internen Verbindungen zwischen Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-131">The number of internal connections between nodes in the graph.</span></span>


`IntermediateEdges`

<span data-ttu-id="9f2b4-132">Typ: \_ \_ Feldgröße \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f2b4-132">Type: \_Field\_size\_(IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="9f2b4-133">Ein Array von Verbindungen zwischen Eingaben und Ausgaben interner Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-133">An array of connections between inputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="9f2b4-134">Das Feld Typ innerhalb jedes Elements sollte auf [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span><span class="sxs-lookup"><span data-stu-id="9f2b4-134">The Type field within each element should be set to [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span></span>


## <a name="remarks"></a><span data-ttu-id="9f2b4-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f2b4-135">Remarks</span></span>
<span data-ttu-id="9f2b4-136">Das von dieser Struktur beschriebene Diagramm muss ein gerichteter azyklischer Graph sein.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-136">The graph described by this structure must be a directed acyclic graph.</span></span> <span data-ttu-id="9f2b4-137">Sie müssen eine Verbindung für die Ein- und Ausgabe jedes angegebenen Knotens definieren, mit Ausnahme von Eingaben und Ausgaben, die für den zugeordneten Operator optional sind.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-137">You must define a connection for the input and output of each supplied node, except for inputs and outputs that are optional for the associated operator.</span></span>

<span data-ttu-id="9f2b4-138">Knoten können Operatoren verwenden, die mit dem [flag DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) für bestimmte Eingaben erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-138">Nodes may use operators that were created using the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag for certain inputs.</span></span> <span data-ttu-id="9f2b4-139">Alle Operatoreingaben, die dieses Flag verwenden, müssen mit Grapheingaben verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-139">Any operator inputs using this flag must be connected to graph inputs.</span></span> <span data-ttu-id="9f2b4-140">Alle Operatoreingaben, die mit derselben Grapheingabe verbunden sind, müssen dieses Flag entsprechend verwenden oder weglassen.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-140">All operator inputs connected to the same graph input must use or omit this flag equivalently.</span></span>

<span data-ttu-id="9f2b4-141">Es ist zulässig, Operatoren zu verbinden, deren verbundene Eingaben und Ausgaben unterschiedliche Dimensionsanzahlen, Größen und Datentypen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-141">It is legal to connect operators whose connected inputs and outputs use different dimension counts, sizes, and data types.</span></span> <span data-ttu-id="9f2b4-142">Dies bedeutet, dass das Tensordatenblob von jedem Operator unterschiedlich interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-142">This implies that the tensor data blob is interpreted differently by each operator.</span></span> <span data-ttu-id="9f2b4-143">Das Feld *TotalTensorSizeInBytes* der verbundenen Tensoreingaben und -ausgaben muss jedoch identisch sein.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-143">The *TotalTensorSizeInBytes* field of connected tensor inputs and outputs must be identical, though.</span></span> <span data-ttu-id="9f2b4-144">Operatoren sollten nur Bereiche mit Tensoren lesen, die von früheren Operatoren geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-144">Operators should only read regions of tensors written by earlier operators.</span></span> <span data-ttu-id="9f2b4-145">Alle Auf padding-Bereiche in der Ausgabe eines Vorgangs (die sich aus der Verwendung von Strides ergeben) werden von Downstreamoperatoren nicht als 0 (null) gelesen.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-145">Any padding regions in the output of an operation (resulting from the use of strides) are not guaranteed to be read as zero by down-stream operators.</span></span>

## <a name="availability"></a><span data-ttu-id="9f2b4-146">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="9f2b4-146">Availability</span></span>

<span data-ttu-id="9f2b4-147">Diese API wurde in der DirectML-Version `1.1.0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9f2b4-147">This API was introduced in DirectML version `1.1.0`.</span></span>


## <a name="requirements"></a><span data-ttu-id="9f2b4-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f2b4-148">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9f2b4-149">**Header**</span><span class="sxs-lookup"><span data-stu-id="9f2b4-149">**Header**</span></span> | <span data-ttu-id="9f2b4-150">directml.h</span><span class="sxs-lookup"><span data-stu-id="9f2b4-150">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="9f2b4-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f2b4-151">See also</span></span>

* [<span data-ttu-id="9f2b4-152">IDMLDevice1::CompileGraph-Methode</span><span class="sxs-lookup"><span data-stu-id="9f2b4-152">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="9f2b4-153">DML_GRAPH_NODE_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="9f2b4-153">DML_GRAPH_NODE_DESC struct</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="9f2b4-154">DML_GRAPH_EDGE_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="9f2b4-154">DML_GRAPH_EDGE_DESC struct</span></span>](./ns-directml-dml_graph_edge_desc.md)