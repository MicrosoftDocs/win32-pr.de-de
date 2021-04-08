---
description: Erstellen von Ausgabe Knoten
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Erstellen von Ausgabe Knoten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4388258c82c12f8473dc07df83ba3b9467eed7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861815"
---
# <a name="creating-output-nodes"></a>Erstellen von Ausgabe Knoten

Ein Ausgabe Knoten stellt eine streamsenke für eine Medien Senke dar. Es gibt zwei Möglichkeiten, einen Ausgabe Knoten zu initialisieren:

-   Von einem Zeiger auf die streamsenke.
-   Von einem Zeiger auf ein Aktivierungs Objekt für die Medien Senke.

Wenn Sie die Topologie in den geschützten Medien Pfad (PMP) laden möchten, müssen Sie ein Aktivierungs Objekt verwenden, damit die Medien Senke innerhalb des geschützten Prozesses erstellt werden kann. Der erste Ansatz (mit einem Zeiger auf die streamsenke) funktioniert nicht mit dem PMP.

## <a name="creating-an-output-node-from-a-stream-sink"></a>Erstellen eines Ausgabe Knotens aus einer Stream-Senke

Gehen Sie folgendermaßen vor, um einen Ausgabe Knoten aus einer Stream-Senke zu erstellen:

1.  Erstellen Sie eine Instanz der Medien Senke.
2.  Verwenden Sie die [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Schnittstelle der Medien Senke, um einen Zeiger auf die gewünschte streamsenke zu erhalten. (Die **imfmediasink** -Schnittstelle verfügt über mehrere Methoden, die Zeiger auf eine streamsenke zurückgeben.)
3.  Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Flag der **MF- \_ topologieausgabeknoten \_ \_** auf, um den Ausgabe Knoten zu erstellen.
4.  Aufrufen von [**imftopologynode:: abtobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) und übergeben eines Zeigers an die [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle der Stream-Senke.
5.  Legen Sie den [**MF- \_ toponode- \_ noshutdown \_ \_**](mf-toponode-noshutdown-on-remove-attribute.md) -Wert für das Remove-Attribut auf **false** fest (optional, jedoch empfohlen)
6.  Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.

Im folgenden Beispiel wird ein Ausgabe Knoten aus einer streamsenke erstellt und initialisiert.


```C++
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFStreamSink *pStreamSink, // Stream sink.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    IMFTopologyNode *pNode = NULL;
    HRESULT hr = S_OK;
    
    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pStreamSink);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, TRUE);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    if (pNode)
    {
        pNode->Release();
    }
    return hr;
}
```



Wenn die Anwendung die Medien Sitzung herunterfährt, wird die Medien Senke von der Medien Sitzung automatisch heruntergefahren. Daher können Sie die Medien Senke nicht mit einer anderen Instanz der Medien Sitzung wieder verwenden.

## <a name="creating-an-output-node-from-an-activation-object"></a>Erstellen eines Ausgabe Knotens aus einem Aktivierungs Objekt

Jede vertrauenswürdige Medien Senke muss ein Aktivierungs Objekt bereitstellen, damit die Medien Senke innerhalb des geschützten Prozesses erstellt werden kann. Weitere Informationen finden Sie unter [Activation Objects](activation-objects.md). Die spezielle Funktion, die das Aktivierungs Objekt erstellt, hängt von der Medien Senke ab.

Gehen Sie folgendermaßen vor, um einen Ausgabe Knoten aus einem Aktivierungs Objekt zu erstellen:

1.  Erstellen Sie das Aktivierungs Objekt, und rufen Sie einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle des Aktivierungs Objekts ab.
2.  Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Flag der **MF- \_ topologieausgabeknoten \_ \_** auf, um den Ausgabe Knoten zu erstellen.
3.  Legen Sie optional das [**MF- \_ toponode \_ streamid**](mf-toponode-streamid-attribute.md) -Attribut für den Knoten fest, um den Datenstrom Bezeichner der Datenstrom Senke anzugeben. Wenn Sie dieses Attribut weglassen, verwendet der Knoten standardmäßig Stream Sink 0.
4.  Legen Sie den [**MF- \_ toponode- \_ noshutdown \_ \_**](mf-toponode-noshutdown-on-remove-attribute.md) -Wert für das Remove-Attribut auf **true** (optional, aber empfohlen)
5.  Nennen Sie [**imftopologynode:: abtobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) , und übergeben Sie den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger.
6.  Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.

Im folgenden Beispiel wird ein Ausgabe Knoten von einem Aktivierungs Objekt erstellt und initialisiert.


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
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

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Erstellen von Topologien](creating-topologies.md)
</dt> <dt>

[Medien senken](media-sinks.md)
</dt> <dt>

[Topologien](topologies.md)
</dt> </dl>

 

 



