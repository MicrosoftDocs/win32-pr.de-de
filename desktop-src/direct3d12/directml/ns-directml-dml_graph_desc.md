---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Beschreibt ein Diagramm der directml-Operatoren, die zum Kompilieren eines kombinierten, optimierten Operators verwendet werden.
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
ms.openlocfilehash: e72209d19bb26524576783becbbfbf94566d8370
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361110"
---
# <a name="dml_graph_desc-structure-directmlh"></a><span data-ttu-id="b34d9-103">DML_GRAPH_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b34d9-103">DML_GRAPH_DESC structure (directml.h)</span></span>

<span data-ttu-id="b34d9-104">Beschreibt ein Diagramm der directml-Operatoren, die zum Kompilieren eines kombinierten, optimierten Operators verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b34d9-104">Describes a graph of DirectML operators used to compile a combined, optimized operator.</span></span> <span data-ttu-id="b34d9-105">Weitere Informationen finden Sie unter [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="b34d9-105">See [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b34d9-106">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="b34d9-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="b34d9-107">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b34d9-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b34d9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b34d9-108">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="b34d9-109">Member</span><span class="sxs-lookup"><span data-stu-id="b34d9-109">Members</span></span>

`InputCount`

<span data-ttu-id="b34d9-110">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b34d9-110">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b34d9-111">Die Anzahl der Eingaben des Gesamt Diagramms.</span><span class="sxs-lookup"><span data-stu-id="b34d9-111">The number of inputs of the overall graph.</span></span> <span data-ttu-id="b34d9-112">Jede Diagramm Eingabe kann mit einer Variablen Anzahl interner Knoten verbunden werden. Daher kann sich dies von *inputedgecount* unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="b34d9-112">Each graph input may be connected to a variable number of internal nodes, therefore this may be different from *InputEdgeCount*.</span></span>


`OutputCount`

<span data-ttu-id="b34d9-113">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b34d9-113">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b34d9-114">Die Anzahl der Ausgaben des gesamten Diagramms.</span><span class="sxs-lookup"><span data-stu-id="b34d9-114">The number of outputs of the overall graph.</span></span> <span data-ttu-id="b34d9-115">Jede Diagramm Ausgabe kann mit einer Variablen Anzahl interner Knoten verbunden werden. Daher kann sich dies von *outputedgecount* unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="b34d9-115">Each graph output may be connected to a variable number of internal nodes, therefore this may be different from *OutputEdgeCount*.</span></span>


`NodeCount`

<span data-ttu-id="b34d9-116">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b34d9-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b34d9-117">Die Anzahl der internen Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b34d9-117">The number of internal nodes in the graph.</span></span>


`Nodes`

<span data-ttu-id="b34d9-118">Type: \_ Field \_ size \_ (NodeCount) **Konstanten [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="b34d9-118">Type: \_Field\_size\_(NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)\***</span></span>

<span data-ttu-id="b34d9-119">Die internen Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b34d9-119">The internal nodes in the graph.</span></span>


`InputEdgeCount`

<span data-ttu-id="b34d9-120">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b34d9-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b34d9-121">Die Anzahl der Verbindungen zwischen Graph-Eingaben und Eingaben interner Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b34d9-121">The number of connections between graph inputs and inputs of internal nodes in the graph.</span></span>


`InputEdges`

<span data-ttu-id="b34d9-122">Type: \_ Field \_ size \_ (inputedgecount) **Konstanten [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="b34d9-122">Type: \_Field\_size\_(InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="b34d9-123">Ein Array von Verbindungen zwischen Graph-Eingaben und Eingaben interner Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b34d9-123">An array of connections between graph inputs and inputs of internal nodes in the graph.</span></span> <span data-ttu-id="b34d9-124">Das *typanfeld* innerhalb der einzelnen Elemente sollte auf [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b34d9-124">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`OutputEdgeCount`

<span data-ttu-id="b34d9-125">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b34d9-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b34d9-126">Die Anzahl der Verbindungen zwischen Diagramm Ausgaben und Ausgaben interner Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b34d9-126">The number of connections between graph outputs and outputs of internal nodes in the graph.</span></span>


`OutputEdges`

<span data-ttu-id="b34d9-127">Type: \_ Field \_ size \_ (outputedgecount) **Konstanten [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="b34d9-127">Type: \_Field\_size\_(OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="b34d9-128">Ein Array von Verbindungen zwischen Diagramm Ausgaben und Ausgaben interner Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b34d9-128">An array of connections between graph outputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="b34d9-129">Das *typanfeld* innerhalb der einzelnen Elemente sollte auf [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b34d9-129">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`IntermediateEdgeCount`

<span data-ttu-id="b34d9-130">Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b34d9-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b34d9-131">Die Anzahl der internen Verbindungen zwischen den Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b34d9-131">The number of internal connections between nodes in the graph.</span></span>


`IntermediateEdges`

<span data-ttu-id="b34d9-132">Type: \_ Field \_ size \_ (intermediateedgecount) **Konstanten [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="b34d9-132">Type: \_Field\_size\_(IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="b34d9-133">Ein Array von Verbindungen zwischen Eingaben und Ausgaben interner Knoten im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b34d9-133">An array of connections between inputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="b34d9-134">Das typanfeld innerhalb der einzelnen Elemente sollte auf festgelegt werden [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span><span class="sxs-lookup"><span data-stu-id="b34d9-134">The Type field within each element should be set to [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span></span>


## <a name="remarks"></a><span data-ttu-id="b34d9-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b34d9-135">Remarks</span></span>
<span data-ttu-id="b34d9-136">Das von dieser Struktur beschriebene Diagramm muss ein gerichtetes azyklisches Diagramm sein.</span><span class="sxs-lookup"><span data-stu-id="b34d9-136">The graph described by this structure must be a directed acyclic graph.</span></span> <span data-ttu-id="b34d9-137">Sie müssen eine Verbindung für die Eingabe und die Ausgabe der einzelnen bereitgestellten Knoten definieren, mit Ausnahme von Eingaben und Ausgaben, die für den zugeordneten Operator optional sind.</span><span class="sxs-lookup"><span data-stu-id="b34d9-137">You must define a connection for the input and output of each supplied node, except for inputs and outputs that are optional for the associated operator.</span></span>

<span data-ttu-id="b34d9-138">Knoten können Operatoren verwenden, die mit dem [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) -Flag für bestimmte Eingaben erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b34d9-138">Nodes may use operators that were created using the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag for certain inputs.</span></span> <span data-ttu-id="b34d9-139">Alle Operator Eingaben, die dieses Flag verwenden, müssen mit Graph-Eingaben verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="b34d9-139">Any operator inputs using this flag must be connected to graph inputs.</span></span> <span data-ttu-id="b34d9-140">Alle Operator Eingaben, die mit derselben Diagramm Eingabe verbunden sind, müssen dieses Flag gleichwertig verwenden oder weglassen.</span><span class="sxs-lookup"><span data-stu-id="b34d9-140">All operator inputs connected to the same graph input must use or omit this flag equivalently.</span></span>

<span data-ttu-id="b34d9-141">Es ist für Verbindungs Operatoren zulässig, deren verbundene Eingaben und Ausgaben verschiedene Dimensions Zähler, Größen und Datentypen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b34d9-141">It is legal to connect operators whose connected inputs and outputs use different dimension counts, sizes, and data types.</span></span> <span data-ttu-id="b34d9-142">Dies bedeutet, dass das tensorflow-datenblob von jedem Operator anders interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="b34d9-142">This implies that the tensor data blob is interpreted differently by each operator.</span></span> <span data-ttu-id="b34d9-143">Das *totaltensorsizeinbytes* -Feld der verbundenen tensorflow-Eingaben und-Ausgaben muss jedoch identisch sein.</span><span class="sxs-lookup"><span data-stu-id="b34d9-143">The *TotalTensorSizeInBytes* field of connected tensor inputs and outputs must be identical, though.</span></span> <span data-ttu-id="b34d9-144">Operatoren sollten nur Regionen von Tensoren lesen, die von früheren Operatoren geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="b34d9-144">Operators should only read regions of tensors written by earlier operators.</span></span> <span data-ttu-id="b34d9-145">Alle Leerraum Bereiche in der Ausgabe eines Vorgangs (die sich aus der Verwendung von Fortschritten ergeben) werden nicht garantiert als 0 (null) von Datenstrom Operatoren gelesen.</span><span class="sxs-lookup"><span data-stu-id="b34d9-145">Any padding regions in the output of an operation (resulting from the use of strides) are not guaranteed to be read as zero by down-stream operators.</span></span>

## <a name="availability"></a><span data-ttu-id="b34d9-146">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="b34d9-146">Availability</span></span>

<span data-ttu-id="b34d9-147">Diese API wurde in der directml-Version eingeführt `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="b34d9-147">This API was introduced in DirectML version `1.1.0`.</span></span>


## <a name="requirements"></a><span data-ttu-id="b34d9-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b34d9-148">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b34d9-149">**Header**</span><span class="sxs-lookup"><span data-stu-id="b34d9-149">**Header**</span></span> | <span data-ttu-id="b34d9-150">directml. h</span><span class="sxs-lookup"><span data-stu-id="b34d9-150">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="b34d9-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b34d9-151">See also</span></span>

* [<span data-ttu-id="b34d9-152">IDMLDevice1:: compilegraph-Methode</span><span class="sxs-lookup"><span data-stu-id="b34d9-152">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="b34d9-153">DML_GRAPH_NODE_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="b34d9-153">DML_GRAPH_NODE_DESC struct</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="b34d9-154">DML_GRAPH_EDGE_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="b34d9-154">DML_GRAPH_EDGE_DESC struct</span></span>](./ns-directml-dml_graph_edge_desc.md)