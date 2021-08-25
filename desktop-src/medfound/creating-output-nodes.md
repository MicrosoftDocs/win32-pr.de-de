---
description: Erstellen von Ausgabeknoten
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Erstellen von Ausgabeknoten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af2842458fb360374d34583b15bfbf5005b2f2bbdd8b32332bc6756ca4e8157
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943020"
---
# <a name="creating-output-nodes"></a>Erstellen von Ausgabeknoten

Ein Ausgabeknoten stellt eine Streamsenke auf einer Mediensenke dar. Es gibt zwei Möglichkeiten, einen Ausgabeknoten zu initialisieren:

-   Von einem Zeiger auf die Streamsenke.
-   Von einem Zeiger auf ein Aktivierungsobjekt für die Mediensenke.

Wenn Sie die Topologie innerhalb des geschützten Medienpfads (PMP) laden möchten, müssen Sie ein Aktivierungsobjekt verwenden, damit die Mediensenke innerhalb des geschützten Prozesses erstellt werden kann. Der erste Ansatz (mit einem Zeiger auf die Streamsenke) funktioniert nicht mit dem PMP.

## <a name="creating-an-output-node-from-a-stream-sink"></a>Erstellen eines Ausgabeknotens aus einer Streamsenke

Gehen Sie wie folgt vor, um einen Ausgabeknoten aus einer Streamsenke zu erstellen:

1.  Erstellen Sie eine Instanz der Mediensenke.
2.  Verwenden Sie die [**BENUTZEROBERFLÄCHE DER MEDIENSenke,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) um einen Zeiger auf die gewünschte Streamsenke zu erhalten. (Die **BENUTZEROBERFLÄCHEMediaSink-Schnittstelle** verfügt über mehrere Methoden, die Zeiger auf eine Streamsenke zurückgeben.)
3.  Rufen [**Sie MFCreateTopologyNode mit dem**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) FLAG **MF \_ TOPOLOGY OUTPUT \_ \_ NODE** auf, um den Ausgabeknoten zu erstellen.
4.  Rufen [**Sie DIE TOPOLOGIENode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) auf, und übergeben Sie einen Zeiger auf die [**DURCHSTREAMStreamSink-Schnittstelle der Streamsenke.**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
5.  Legen Sie [**das \_ MF-Attribut TOPONODE \_ NOSHUTDOWN \_ ON \_ REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) auf **FALSE** fest (optional, aber empfohlen).
6.  Rufen [**Sie DIE TOPOLOGIE::AddNode auf,**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) um den Knoten der Topologie hinzuzufügen.

Im folgenden Beispiel wird ein Ausgabeknoten aus einer Streamsenke erstellt und initialisiert.


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



Wenn die Anwendung die Mediensitzung heruntergefahren hat, wird die Mediensenke automatisch von der Mediensitzung heruntergefahren. Daher können Sie die Mediensenke nicht mit einer anderen Instanz der Mediensitzung erneut verwenden.

## <a name="creating-an-output-node-from-an-activation-object"></a>Erstellen eines Ausgabeknotens aus einem Aktivierungsobjekt

Jede vertrauenswürdige Mediensenke muss ein Aktivierungsobjekt bereitstellen, damit die Mediensenke innerhalb des geschützten Prozesses erstellt werden kann. Weitere Informationen finden Sie unter [Activation Objects](activation-objects.md). Die spezielle Funktion, die das Aktivierungsobjekt erstellt, hängt von der Mediensenke ab.

Gehen Sie wie folgt vor, um einen Ausgabeknoten aus einem Aktivierungsobjekt zu erstellen:

1.  Erstellen Sie das Aktivierungsobjekt, und erhalten Sie einen Zeiger auf die [**ACTIVATIONActivate-Schnittstelle des Aktivierungsobjekts.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
2.  Rufen [**Sie MFCreateTopologyNode mit dem**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) FLAG **MF \_ TOPOLOGY OUTPUT \_ \_ NODE** auf, um den Ausgabeknoten zu erstellen.
3.  Legen Sie optional das [**MF \_ TOPONODE \_ STREAMID-Attribut**](mf-toponode-streamid-attribute.md) auf dem Knoten fest, um den Streambezeichner der Streamsenke anzugeben. Wenn Sie dieses Attribut weglassen, verwendet der Knoten standardmäßig die Streamsenke 0.
4.  Legen Sie [**das MF \_ TOPONODE \_ NOSHUTDOWN \_ ON \_ REMOVE-Attribut**](mf-toponode-noshutdown-on-remove-attribute.md) auf **TRUE** fest (optional, aber empfohlen).
5.  Rufen [**Sie DIE TOPOLOGIENode::SetObject auf,**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) und übergeben Sie [**den ZEIGER FÜR DIE AKTION.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
6.  Rufen [**Sie DIE TOPOLOGIE::AddNode auf,**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) um den Knoten der Topologie hinzuzufügen.

Im folgenden Beispiel wird ein Ausgabeknoten aus einem Aktivierungsobjekt erstellt und initialisiert.


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

[**TOPOLOGIENode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Erstellen von Topologien](creating-topologies.md)
</dt> <dt>

[Mediensenken](media-sinks.md)
</dt> <dt>

[Topologien](topologies.md)
</dt> </dl>

 

 



