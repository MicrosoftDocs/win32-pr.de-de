---
description: Erstellen von Quellknoten
ms.assetid: 44c26bcd-04a9-48c3-b536-25c2b18c34c1
title: Erstellen von Quellknoten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b1e882dd6f8e9345244b56eace332c2fad4bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344234"
---
# <a name="creating-source-nodes"></a><span data-ttu-id="417fd-103">Erstellen von Quellknoten</span><span class="sxs-lookup"><span data-stu-id="417fd-103">Creating Source Nodes</span></span>

<span data-ttu-id="417fd-104">Ein Quellknoten stellt einen Stream aus einer Medienquelle dar.</span><span class="sxs-lookup"><span data-stu-id="417fd-104">A source node represents one stream from a media source.</span></span> <span data-ttu-id="417fd-105">Der Quellknoten muss Zeiger auf die Medienquelle, den Präsentations Deskriptor und den Datenstrom Deskriptor enthalten.</span><span class="sxs-lookup"><span data-stu-id="417fd-105">The source node must contain pointers to the media source, the presentation descriptor, and the stream descriptor.</span></span>

<span data-ttu-id="417fd-106">Gehen Sie folgendermaßen vor, um einer Topologie einen Quellknoten hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="417fd-106">To add a source node to a topology, do the following:</span></span>

1.  <span data-ttu-id="417fd-107">Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Flag für die **MF- \_ \_ topologisourcestream- \_ Knoten** auf, um den Quellknoten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="417fd-107">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** flag to create the source node.</span></span>
2.  <span data-ttu-id="417fd-108">Legen Sie das [**MF- \_ toponode- \_ Quell**](mf-toponode-source-attribute.md) Attribut auf dem Knoten mit einem Zeiger auf die Medienquelle fest.</span><span class="sxs-lookup"><span data-stu-id="417fd-108">Set the [**MF\_TOPONODE\_SOURCE**](mf-toponode-source-attribute.md) attribute on the node, with a pointer to the media source.</span></span>
3.  <span data-ttu-id="417fd-109">Legen Sie das [**MF- \_ toponode- \_ Präsentations \_ deskriptorattribut**](mf-toponode-presentation-descriptor-attribute.md) für den Knoten mit einem Zeiger auf den Präsentations Deskriptor der Medienquelle fest.</span><span class="sxs-lookup"><span data-stu-id="417fd-109">Set the [**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**](mf-toponode-presentation-descriptor-attribute.md) attribute on the node, with a pointer to the presentation descriptor of the media source.</span></span>
4.  <span data-ttu-id="417fd-110">Legen Sie das Attribut " [**MF \_ toponode \_ Stream \_ Deskriptor**](mf-toponode-stream-descriptor-attribute.md) " für den Knoten mit einem Zeiger auf den Datenstrom Deskriptor für den Stream fest.</span><span class="sxs-lookup"><span data-stu-id="417fd-110">Set the [**MF\_TOPONODE\_STREAM\_DESCRIPTOR**](mf-toponode-stream-descriptor-attribute.md) attribute on the node, with a pointer to the stream descriptor for the stream.</span></span>
5.  <span data-ttu-id="417fd-111">Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="417fd-111">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="417fd-112">Im folgenden Beispiel wird ein Quellknoten erstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="417fd-112">The following example creates and initializes a source node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="417fd-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="417fd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="417fd-114">Erstellen von Topologien</span><span class="sxs-lookup"><span data-stu-id="417fd-114">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="417fd-115">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="417fd-115">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="417fd-116">Topologien</span><span class="sxs-lookup"><span data-stu-id="417fd-116">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="417fd-117">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="417fd-117">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



