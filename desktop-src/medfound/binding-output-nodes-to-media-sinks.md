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
# <a name="binding-output-nodes-to-media-sinks"></a><span data-ttu-id="c008b-103">Binden von Ausgabe Knoten an Medien senken</span><span class="sxs-lookup"><span data-stu-id="c008b-103">Binding Output Nodes to Media Sinks</span></span>

<span data-ttu-id="c008b-104">In diesem Thema wird beschrieben, wie die Ausgabe Knoten in einer Topologie initialisiert werden, wenn Sie das topologielader außerhalb der Medien Sitzung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c008b-104">This topic describes how to initialize the output nodes in a topology, if you are using the topology loader outside of the Media Session.</span></span> <span data-ttu-id="c008b-105">Ein Ausgabe Knoten enthält anfänglich einen der folgenden:</span><span class="sxs-lookup"><span data-stu-id="c008b-105">An output node initially contains one of the following:</span></span>

-   <span data-ttu-id="c008b-106">Ein [**IMF streamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c008b-106">An [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer.</span></span>
-   <span data-ttu-id="c008b-107">Ein [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c008b-107">An [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>

<span data-ttu-id="c008b-108">Im letzteren Fall muss der [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger in einen [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Zeiger konvertiert werden, bevor der topologielader die Topologie auflöst.</span><span class="sxs-lookup"><span data-stu-id="c008b-108">In the latter case, the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer must be converted to an [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer before the topology loader resolves the topology.</span></span> <span data-ttu-id="c008b-109">In den meisten Szenarien funktioniert der Prozess wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c008b-109">In most scenarios, the process works as follows:</span></span>

1.  <span data-ttu-id="c008b-110">Die Anwendung fügt eine partielle Topologie in die Medien Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="c008b-110">The application queues a partial topology on the Media Session.</span></span>
2.  <span data-ttu-id="c008b-111">Für alle Ausgabe Knoten konvertiert die Medien Sitzung [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger auf [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c008b-111">For all output nodes, the Media Session converts [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers to [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointers.</span></span> <span data-ttu-id="c008b-112">Dieser Vorgang wird als *binden* des Ausgabe Knotens an eine Medien Senke bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c008b-112">This process is called *binding* the output node to a media sink.</span></span>
3.  <span data-ttu-id="c008b-113">Die Medien Sitzung sendet die geänderte Topologie an die [**imftopoloader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c008b-113">The Media Session sends the modified topology to the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="c008b-114">Wenn Sie jedoch das topologielader direkt (außerhalb der Medien sesession) verwenden, muss die Anwendung die Ausgabe Knoten vor dem Aufrufen von [**imftopoloader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load)binden.</span><span class="sxs-lookup"><span data-stu-id="c008b-114">However, if you are using the topology loader directly (outside of the media sesssion), your application must bind the output nodes prior to calling [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span></span> <span data-ttu-id="c008b-115">Gehen Sie folgendermaßen vor, um einen Ausgabe Knoten zu binden:</span><span class="sxs-lookup"><span data-stu-id="c008b-115">To bind an output node, do the following:</span></span>

1.  <span data-ttu-id="c008b-116">Aufrufen von [**imftopologynode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) zum Abrufen des Objekt Zeigers für den Knoten.</span><span class="sxs-lookup"><span data-stu-id="c008b-116">Call [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) to get the node's object pointer.</span></span>
2.  <span data-ttu-id="c008b-117">Abfragen des Objekt Zeigers für die [**imbstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c008b-117">Query the object pointer for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="c008b-118">Wenn dieser Vorgang erfolgreich ist, gibt es nichts mehr zu tun. überspringen Sie die restlichen Schritte.</span><span class="sxs-lookup"><span data-stu-id="c008b-118">If this call succeeds, there is nothing more to do, so skip the remaining steps.</span></span>
3.  <span data-ttu-id="c008b-119">Wenn der vorherige Schritt fehlgeschlagen ist, Fragen Sie den Objekt Zeiger nach der [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="c008b-119">If the previous step failed, query the object pointer for the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
4.  <span data-ttu-id="c008b-120">Erstellen Sie die Medien Senke, indem Sie [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c008b-120">Create the media sink by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="c008b-121">Geben Sie **IID \_ imfmediasink** an, um einen Zeiger auf die [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Schnittstelle der Medien Senke zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c008b-121">Specify **IID\_IMFMediaSink** to get a pointer to the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface.</span></span>
5.  <span data-ttu-id="c008b-122">Fragen Sie den Knoten für das [**MF- \_ toponode \_ streamid**](mf-toponode-streamid-attribute.md) -Attribut ab.</span><span class="sxs-lookup"><span data-stu-id="c008b-122">Query the node for the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute.</span></span> <span data-ttu-id="c008b-123">Der Wert dieses Attributs ist der Bezeichner der streamsenke für diesen Knoten.</span><span class="sxs-lookup"><span data-stu-id="c008b-123">The value of this attribute is the identifier of the stream sink for this node.</span></span> <span data-ttu-id="c008b-124">Wenn das **MF- \_ toponode \_ streamid** -Attribut nicht festgelegt ist, ist der Standarddaten Strom Bezeichner 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c008b-124">If the **MF\_TOPONODE\_STREAMID** attribute is not set, the default stream identifier is zero.</span></span>
6.  <span data-ttu-id="c008b-125">Die entsprechende streamsenke ist möglicherweise bereits in der Medien Senke vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c008b-125">The appropriate stream sink might already exist on the media sink.</span></span> <span data-ttu-id="c008b-126">Um dies zu überprüfen, wenden Sie [**imfmediasink:: getstreamsinkbyid**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) für die Medien Senke an.</span><span class="sxs-lookup"><span data-stu-id="c008b-126">To check, call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) on the media sink.</span></span> <span data-ttu-id="c008b-127">Wenn die streamsenke vorhanden ist, gibt die Methode einen Zeiger auf die zugehörige [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="c008b-127">If the stream sink exists, the method returns a pointer to its [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="c008b-128">Wenn dieser Aufruf fehlschlägt, versuchen Sie, eine neue streamsenke durch Aufrufen von [**imfmediasink:: addstreamsink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink)hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c008b-128">If this call fails, try to add a new stream sink by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span> <span data-ttu-id="c008b-129">Wenn beide Aufrufe fehlschlagen, bedeutet dies, dass die Medien Senke den angeforderten Datenstrom Bezeichner nicht unterstützt. dieser topologieknoten ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c008b-129">If both calls fail, it means the media sink does not support the requested stream identifier, and this topology node is not configured correctly.</span></span> <span data-ttu-id="c008b-130">Geben Sie einen Fehlercode zurück, und überspringen Sie den nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="c008b-130">Return an error code and skip the next step.</span></span>
7.  <span data-ttu-id="c008b-131">Nennen Sie [**imftopologynode:: abtobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), und übergeben Sie den [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Zeiger aus dem vorherigen Schritt.</span><span class="sxs-lookup"><span data-stu-id="c008b-131">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passing in the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer from the previous step.</span></span> <span data-ttu-id="c008b-132">Dieser Befehl ersetzt den Objekt Zeiger des Knotens, sodass der Knoten anstelle eines Zeigers auf das Aktivierungs Objekt einen Zeiger auf die streamsenke enthält.</span><span class="sxs-lookup"><span data-stu-id="c008b-132">This call replaces the node's object pointer, so that the node contains a pointer to the stream sink, instead of a pointer to the activation object.</span></span>

<span data-ttu-id="c008b-133">Der folgende Code zeigt, wie ein Ausgabe Knoten gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="c008b-133">The following code shows how to bind an output node.</span></span>


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
> <span data-ttu-id="c008b-134">In diesem Beispiel wird die Funktion " [saferelease](saferelease.md) " verwendet, um Schnittstellen Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c008b-134">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="c008b-135">Im nächsten Beispiel wird gezeigt, wie alle Ausgabe Knoten in einer Topologie gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="c008b-135">The next example shows how to bind all of the output nodes in a topology.</span></span> <span data-ttu-id="c008b-136">In diesem Beispiel wird die [**imftopology:: getoutputnodecollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) -Methode verwendet, um eine Auflistung von Ausgabe Knoten aus der Topologie zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c008b-136">This example uses the [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) method to get a collection of output nodes from the topology.</span></span> <span data-ttu-id="c008b-137">Anschließend wird die im vorherigen Beispiel gezeigte Funktion auf jedem dieser Knoten aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c008b-137">Then it calls the function shown in the previous example on each of those nodes in turn.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c008b-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c008b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c008b-139">Erweiterte topologiebildung</span><span class="sxs-lookup"><span data-stu-id="c008b-139">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> <dt>

[<span data-ttu-id="c008b-140">Medien senken</span><span class="sxs-lookup"><span data-stu-id="c008b-140">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="c008b-141">**Imftopoloader**</span><span class="sxs-lookup"><span data-stu-id="c008b-141">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



