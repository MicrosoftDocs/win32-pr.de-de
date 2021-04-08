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
# <a name="creating-output-nodes"></a><span data-ttu-id="9bb46-103">Erstellen von Ausgabe Knoten</span><span class="sxs-lookup"><span data-stu-id="9bb46-103">Creating Output Nodes</span></span>

<span data-ttu-id="9bb46-104">Ein Ausgabe Knoten stellt eine streamsenke für eine Medien Senke dar.</span><span class="sxs-lookup"><span data-stu-id="9bb46-104">An output node represents a stream sink on a media sink.</span></span> <span data-ttu-id="9bb46-105">Es gibt zwei Möglichkeiten, einen Ausgabe Knoten zu initialisieren:</span><span class="sxs-lookup"><span data-stu-id="9bb46-105">There are two ways to initialize an output node:</span></span>

-   <span data-ttu-id="9bb46-106">Von einem Zeiger auf die streamsenke.</span><span class="sxs-lookup"><span data-stu-id="9bb46-106">From a pointer to the stream sink.</span></span>
-   <span data-ttu-id="9bb46-107">Von einem Zeiger auf ein Aktivierungs Objekt für die Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="9bb46-107">From a pointer to an activation object for the media sink.</span></span>

<span data-ttu-id="9bb46-108">Wenn Sie die Topologie in den geschützten Medien Pfad (PMP) laden möchten, müssen Sie ein Aktivierungs Objekt verwenden, damit die Medien Senke innerhalb des geschützten Prozesses erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9bb46-108">If you are going to load the topology inside the protected media path (PMP), you must use an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="9bb46-109">Der erste Ansatz (mit einem Zeiger auf die streamsenke) funktioniert nicht mit dem PMP.</span><span class="sxs-lookup"><span data-stu-id="9bb46-109">The first approach (using a pointer to the stream sink) does not work with the PMP.</span></span>

## <a name="creating-an-output-node-from-a-stream-sink"></a><span data-ttu-id="9bb46-110">Erstellen eines Ausgabe Knotens aus einer Stream-Senke</span><span class="sxs-lookup"><span data-stu-id="9bb46-110">Creating an Output Node from a Stream Sink</span></span>

<span data-ttu-id="9bb46-111">Gehen Sie folgendermaßen vor, um einen Ausgabe Knoten aus einer Stream-Senke zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="9bb46-111">To create an output node from a stream sink, do the following:</span></span>

1.  <span data-ttu-id="9bb46-112">Erstellen Sie eine Instanz der Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="9bb46-112">Create an instance of the media sink.</span></span>
2.  <span data-ttu-id="9bb46-113">Verwenden Sie die [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Schnittstelle der Medien Senke, um einen Zeiger auf die gewünschte streamsenke zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9bb46-113">Use the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface to get a pointer to the desired stream sink.</span></span> <span data-ttu-id="9bb46-114">(Die **imfmediasink** -Schnittstelle verfügt über mehrere Methoden, die Zeiger auf eine streamsenke zurückgeben.)</span><span class="sxs-lookup"><span data-stu-id="9bb46-114">(The **IMFMediaSink** interface has several methods that return pointers to a stream sink.)</span></span>
3.  <span data-ttu-id="9bb46-115">Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Flag der **MF- \_ topologieausgabeknoten \_ \_** auf, um den Ausgabe Knoten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9bb46-115">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
4.  <span data-ttu-id="9bb46-116">Aufrufen von [**imftopologynode:: abtobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) und übergeben eines Zeigers an die [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle der Stream-Senke.</span><span class="sxs-lookup"><span data-stu-id="9bb46-116">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in a pointer to the stream sink's [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span>
5.  <span data-ttu-id="9bb46-117">Legen Sie den [**MF- \_ toponode- \_ noshutdown \_ \_**](mf-toponode-noshutdown-on-remove-attribute.md) -Wert für das Remove-Attribut auf **false** fest (optional, jedoch empfohlen)</span><span class="sxs-lookup"><span data-stu-id="9bb46-117">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **FALSE** (optional but recommended).</span></span>
6.  <span data-ttu-id="9bb46-118">Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9bb46-118">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="9bb46-119">Im folgenden Beispiel wird ein Ausgabe Knoten aus einer streamsenke erstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="9bb46-119">The following example creates and initializes an output node from a stream sink.</span></span>


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



<span data-ttu-id="9bb46-120">Wenn die Anwendung die Medien Sitzung herunterfährt, wird die Medien Senke von der Medien Sitzung automatisch heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="9bb46-120">When the application shuts down the Media Session, the Media Session automatically shuts down the media sink.</span></span> <span data-ttu-id="9bb46-121">Daher können Sie die Medien Senke nicht mit einer anderen Instanz der Medien Sitzung wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="9bb46-121">Therefore, you cannot re-use the media sink with another instance of the Media Session.</span></span>

## <a name="creating-an-output-node-from-an-activation-object"></a><span data-ttu-id="9bb46-122">Erstellen eines Ausgabe Knotens aus einem Aktivierungs Objekt</span><span class="sxs-lookup"><span data-stu-id="9bb46-122">Creating an Output Node from an Activation Object</span></span>

<span data-ttu-id="9bb46-123">Jede vertrauenswürdige Medien Senke muss ein Aktivierungs Objekt bereitstellen, damit die Medien Senke innerhalb des geschützten Prozesses erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9bb46-123">Any trusted media sink must provide an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="9bb46-124">Weitere Informationen finden Sie unter [Activation Objects](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9bb46-124">For more information, see [Activation Objects](activation-objects.md).</span></span> <span data-ttu-id="9bb46-125">Die spezielle Funktion, die das Aktivierungs Objekt erstellt, hängt von der Medien Senke ab.</span><span class="sxs-lookup"><span data-stu-id="9bb46-125">The particular function that creates the activation object will depend on the media sink.</span></span>

<span data-ttu-id="9bb46-126">Gehen Sie folgendermaßen vor, um einen Ausgabe Knoten aus einem Aktivierungs Objekt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="9bb46-126">To create an output node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="9bb46-127">Erstellen Sie das Aktivierungs Objekt, und rufen Sie einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle des Aktivierungs Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="9bb46-127">Create the activation object and get a pointer to the activation object's [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="9bb46-128">Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Flag der **MF- \_ topologieausgabeknoten \_ \_** auf, um den Ausgabe Knoten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9bb46-128">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
3.  <span data-ttu-id="9bb46-129">Legen Sie optional das [**MF- \_ toponode \_ streamid**](mf-toponode-streamid-attribute.md) -Attribut für den Knoten fest, um den Datenstrom Bezeichner der Datenstrom Senke anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9bb46-129">Optionally, set the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute on the node to specify the stream identifier of the stream sink.</span></span> <span data-ttu-id="9bb46-130">Wenn Sie dieses Attribut weglassen, verwendet der Knoten standardmäßig Stream Sink 0.</span><span class="sxs-lookup"><span data-stu-id="9bb46-130">If you omit this attribute, the node defaults to using stream sink 0.</span></span>
4.  <span data-ttu-id="9bb46-131">Legen Sie den [**MF- \_ toponode- \_ noshutdown \_ \_**](mf-toponode-noshutdown-on-remove-attribute.md) -Wert für das Remove-Attribut auf **true** (optional, aber empfohlen)</span><span class="sxs-lookup"><span data-stu-id="9bb46-131">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **TRUE** (optional but recommended).</span></span>
5.  <span data-ttu-id="9bb46-132">Nennen Sie [**imftopologynode:: abtobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) , und übergeben Sie den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="9bb46-132">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
6.  <span data-ttu-id="9bb46-133">Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9bb46-133">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="9bb46-134">Im folgenden Beispiel wird ein Ausgabe Knoten von einem Aktivierungs Objekt erstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="9bb46-134">The following example creates and initializes an output node from an activation object.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9bb46-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9bb46-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bb46-136">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="9bb46-136">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="9bb46-137">Erstellen von Topologien</span><span class="sxs-lookup"><span data-stu-id="9bb46-137">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="9bb46-138">Medien senken</span><span class="sxs-lookup"><span data-stu-id="9bb46-138">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="9bb46-139">Topologien</span><span class="sxs-lookup"><span data-stu-id="9bb46-139">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



