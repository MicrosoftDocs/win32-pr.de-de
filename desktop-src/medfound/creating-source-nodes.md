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
# <a name="creating-source-nodes"></a>Erstellen von Quellknoten

Ein Quellknoten stellt einen Stream aus einer Medienquelle dar. Der Quellknoten muss Zeiger auf die Medienquelle, den Präsentations Deskriptor und den Datenstrom Deskriptor enthalten.

Gehen Sie folgendermaßen vor, um einer Topologie einen Quellknoten hinzuzufügen:

1.  Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Flag für die **MF- \_ \_ topologisourcestream- \_ Knoten** auf, um den Quellknoten zu erstellen.
2.  Legen Sie das [**MF- \_ toponode- \_ Quell**](mf-toponode-source-attribute.md) Attribut auf dem Knoten mit einem Zeiger auf die Medienquelle fest.
3.  Legen Sie das [**MF- \_ toponode- \_ Präsentations \_ deskriptorattribut**](mf-toponode-presentation-descriptor-attribute.md) für den Knoten mit einem Zeiger auf den Präsentations Deskriptor der Medienquelle fest.
4.  Legen Sie das Attribut " [**MF \_ toponode \_ Stream \_ Deskriptor**](mf-toponode-stream-descriptor-attribute.md) " für den Knoten mit einem Zeiger auf den Datenstrom Deskriptor für den Stream fest.
5.  Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.

Im folgenden Beispiel wird ein Quellknoten erstellt und initialisiert.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Topologien](creating-topologies.md)
</dt> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[Topologien](topologies.md)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



