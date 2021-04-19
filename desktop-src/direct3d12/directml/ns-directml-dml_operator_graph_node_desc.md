---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: 'Decoiert einen Knoten innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.'
helpviewer_keywords:
- DML_OPERATOR_GRAPH_NODE_DESC
- DML_OPERATOR_GRAPH_NODE_DESC structure
- direct3d12.dml_operator_graph_node_desc
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
ms.openlocfilehash: 6081f81044ff2ce384f7906af9c6e80f6b06f774
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106357143"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a><span data-ttu-id="fbd11-103">DML_OPERATOR_GRAPH_NODE_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="fbd11-103">DML_OPERATOR_GRAPH_NODE_DESC structure (directml.h)</span></span>
<span data-ttu-id="fbd11-104">Decoiert einen Knoten innerhalb eines Diagramms von directml-Operatoren, die durch [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) definiert und an [IDMLDevice1:: compilegraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="fbd11-104">Decribes a node within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

<span data-ttu-id="fbd11-105">Das Verhalten dieses Knotens wird durch einen directml-Operator definiert.</span><span class="sxs-lookup"><span data-stu-id="fbd11-105">The behavior of this node is defined by a DirectML operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fbd11-106">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="fbd11-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="fbd11-107">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fbd11-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd11-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbd11-108">Syntax</span></span>
```cpp
struct DML_OPERATOR_GRAPH_NODE_DESC {
  IDMLOperator *Operator;
  const char   *Name;
};
```



## <a name="members"></a><span data-ttu-id="fbd11-109">Member</span><span class="sxs-lookup"><span data-stu-id="fbd11-109">Members</span></span>

`Operator`

<span data-ttu-id="fbd11-110">Typ: <b> [idmloperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span><span class="sxs-lookup"><span data-stu-id="fbd11-110">Type: <b>[IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span></span>

<span data-ttu-id="fbd11-111">Ein directml-Operator, der das Verhalten des Knotens definiert.</span><span class="sxs-lookup"><span data-stu-id="fbd11-111">A DirectML operator defining the behavior of the node.</span></span>


`Name`

<span data-ttu-id="fbd11-112">Typ: \_ Field \_ z \_ \_ maybenull \_ **Konstanten \*** Zeichen</span><span class="sxs-lookup"><span data-stu-id="fbd11-112">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="fbd11-113">Ein optionaler Name für die Diagramm Verbindung.</span><span class="sxs-lookup"><span data-stu-id="fbd11-113">An optional name for the graph connection.</span></span> <span data-ttu-id="fbd11-114">Wenn bereitgestellt, kann dies in bestimmten Fehlermeldungen verwendet werden, die von der directml-debugschicht ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fbd11-114">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="fbd11-115">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="fbd11-115">Availability</span></span>

<span data-ttu-id="fbd11-116">Diese API wurde in der directml-Version eingeführt `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="fbd11-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="fbd11-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbd11-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fbd11-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="fbd11-118">**Header**</span></span> | <span data-ttu-id="fbd11-119">directml. h</span><span class="sxs-lookup"><span data-stu-id="fbd11-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="fbd11-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbd11-120">See also</span></span>

* [<span data-ttu-id="fbd11-121">IDMLDevice1:: compilegraph-Methode</span><span class="sxs-lookup"><span data-stu-id="fbd11-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="fbd11-122">DML_GRAPH_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="fbd11-122">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="fbd11-123">DML_GRAPH_NODE_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="fbd11-123">DML_GRAPH_NODE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)