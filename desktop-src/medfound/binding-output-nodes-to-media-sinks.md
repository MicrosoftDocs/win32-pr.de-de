---
description: Binden von Ausgabe Knoten an Medien senken
ms.assetid: d4f93f34-0af1-431f-9333-70ea09691b64
title: Binden von Ausgabe Knoten an Medien senken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbea075badf74ac9e0e9354d82f4100a6167a0c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530479"
---
# <a name="binding-output-nodes-to-media-sinks"></a>Binden von Ausgabe Knoten an Medien senken

In diesem Thema wird beschrieben, wie die Ausgabe Knoten in einer Topologie initialisiert werden, wenn Sie das topologielader außerhalb der Medien Sitzung verwenden. Ein Ausgabe Knoten enthält anfänglich einen der folgenden:

-   Ein [**IMF streamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Zeiger.
-   Ein [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger.

Im letzteren Fall muss der [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger in einen [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Zeiger konvertiert werden, bevor der topologielader die Topologie auflöst. In den meisten Szenarien funktioniert der Prozess wie folgt:

1.  Die Anwendung fügt eine partielle Topologie in die Medien Sitzung ein.
2.  Für alle Ausgabe Knoten konvertiert die Medien Sitzung [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger auf [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Zeiger. Dieser Vorgang wird als *binden* des Ausgabe Knotens an eine Medien Senke bezeichnet.
3.  Die Medien Sitzung sendet die geänderte Topologie an die [**imftopoloader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) -Methode.

Wenn Sie jedoch das topologielader direkt (außerhalb der Medien sesession) verwenden, muss die Anwendung die Ausgabe Knoten vor dem Aufrufen von [**imftopoloader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load)binden. Gehen Sie folgendermaßen vor, um einen Ausgabe Knoten zu binden:

1.  Aufrufen von [**imftopologynode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) zum Abrufen des Objekt Zeigers für den Knoten.
2.  Abfragen des Objekt Zeigers für die [**imbstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle. Wenn dieser Vorgang erfolgreich ist, gibt es nichts mehr zu tun. überspringen Sie die restlichen Schritte.
3.  Wenn der vorherige Schritt fehlgeschlagen ist, Fragen Sie den Objekt Zeiger nach der [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle ab.
4.  Erstellen Sie die Medien Senke, indem Sie [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)aufrufen. Geben Sie **IID \_ imfmediasink** an, um einen Zeiger auf die [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Schnittstelle der Medien Senke zu erhalten.
5.  Fragen Sie den Knoten für das [**MF- \_ toponode \_ streamid**](mf-toponode-streamid-attribute.md) -Attribut ab. Der Wert dieses Attributs ist der Bezeichner der streamsenke für diesen Knoten. Wenn das **MF- \_ toponode \_ streamid** -Attribut nicht festgelegt ist, ist der Standarddaten Strom Bezeichner 0 (null).
6.  Die entsprechende streamsenke ist möglicherweise bereits in der Medien Senke vorhanden. Um dies zu überprüfen, wenden Sie [**imfmediasink:: getstreamsinkbyid**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) für die Medien Senke an. Wenn die streamsenke vorhanden ist, gibt die Methode einen Zeiger auf die zugehörige [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle zurück. Wenn dieser Aufruf fehlschlägt, versuchen Sie, eine neue streamsenke durch Aufrufen von [**imfmediasink:: addstreamsink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink)hinzuzufügen. Wenn beide Aufrufe fehlschlagen, bedeutet dies, dass die Medien Senke den angeforderten Datenstrom Bezeichner nicht unterstützt. dieser topologieknoten ist nicht ordnungsgemäß konfiguriert. Geben Sie einen Fehlercode zurück, und überspringen Sie den nächsten Schritt.
7.  Nennen Sie [**imftopologynode:: abtobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), und übergeben Sie den [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Zeiger aus dem vorherigen Schritt. Dieser Befehl ersetzt den Objekt Zeiger des Knotens, sodass der Knoten anstelle eines Zeigers auf das Aktivierungs Objekt einen Zeiger auf die streamsenke enthält.

Der folgende Code zeigt, wie ein Ausgabe Knoten gebunden wird.


```C++
// BindOutputNode
// Sets the IMFStreamSink pointer on an output node.

HRESULT BindOutputNode(IMFTopologyNode *pNode)
{
    IUnknown *pNodeObject = NULL;
    IMFActivate *pActivate = NULL;
    IMFStreamSink *pStream = NULL;
    IMFMediaSink *pSink = NULL;

    // Get the node's object pointer.
    HRESULT hr = pNode->GetObject(&pNodeObject);
    if (FAILED(hr))
    {
        return hr;
    }

    // The object pointer should be one of the following:
    // 1. An activation object for the media sink.
    // 2. The stream sink.

    // If it's #2, then we're already done.

    // First, check if it's an activation object.
    hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pActivate));

    if (SUCCEEDED(hr))
    {
        DWORD dwStreamID = 0;

        // The object pointer is an activation object. 
        
        // Try to create the media sink.
        hr = pActivate->ActivateObject(IID_PPV_ARGS(&pSink));

        // Look up the stream ID. (Default to zero.)

        if (SUCCEEDED(hr))
        {
           dwStreamID = MFGetAttributeUINT32(pNode, MF_TOPONODE_STREAMID, 0);
        }

        // Now try to get or create the stream sink.

        // Check if the media sink already has a stream sink with the requested ID.

        if (SUCCEEDED(hr))
        {
            hr = pSink->GetStreamSinkById(dwStreamID, &pStream);
            if (FAILED(hr))
            {
                // Try to add a new stream sink.
                hr = pSink->AddStreamSink(dwStreamID, NULL, &pStream);
            }
        }

        // Replace the node's object pointer with the stream sink. 
        if (SUCCEEDED(hr))
        {
            hr = pNode->SetObject(pStream);
        }
    }
    else
    {
        // Not an activation object. Is it a stream sink?
        hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pStream));
    }

    SafeRelease(&pNodeObject);
    SafeRelease(&pActivate);
    SafeRelease(&pStream);
    SafeRelease(&pSink);
    return hr;
}
```



> [!Note]  
> In diesem Beispiel wird die Funktion " [saferelease](saferelease.md) " verwendet, um Schnittstellen Zeiger freizugeben.

 

Im nächsten Beispiel wird gezeigt, wie alle Ausgabe Knoten in einer Topologie gebunden werden. In diesem Beispiel wird die [**imftopology:: getoutputnodecollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) -Methode verwendet, um eine Auflistung von Ausgabe Knoten aus der Topologie zu erhalten. Anschließend wird die im vorherigen Beispiel gezeigte Funktion auf jedem dieser Knoten aufgerufen.


```C++
// BindOutputNodes
// Sets the IMFStreamSink pointers on all of the output nodes in a topology.

HRESULT BindOutputNodes(IMFTopology *pTopology)
{
    DWORD cNodes = 0;

    IMFCollection *pCol = NULL;
    IUnknown *pUnk = NULL;
    IMFTopologyNode *pNode = NULL;

    // Get the collection of output nodes. 
    HRESULT hr = pTopology->GetOutputNodeCollection(&pCol);
    
    // Enumerate all of the nodes in the collection.
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            hr = pCol->GetElement(i, &pUnk);

            if (FAILED(hr)) { break; }

            hr = pUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);

            if (FAILED(hr)) { break; }

            // Bind this node.
            hr = BindOutputNode(pNode);

            if (FAILED(hr)) { break; }
        }
    }

    SafeRelease(&pCol);
    SafeRelease(&pUnk);
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte topologiebildung](advanced-topology-building.md)
</dt> <dt>

[Medien senken](media-sinks.md)
</dt> <dt>

[**Imftopoloader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



