---
description: Erstellen von Transformations Knoten
ms.assetid: d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682
title: Erstellen von Transformations Knoten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f39eed9f49e10501fadc00f47b57cf95705a7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524611"
---
# <a name="creating-transform-nodes"></a><span data-ttu-id="e71e7-103">Erstellen von Transformations Knoten</span><span class="sxs-lookup"><span data-stu-id="e71e7-103">Creating Transform Nodes</span></span>

<span data-ttu-id="e71e7-104">Ein Transformations Knoten stellt eine Media Foundation Transformation (MFT) dar, z. b. einen Decoder oder einen Encoder.</span><span class="sxs-lookup"><span data-stu-id="e71e7-104">A transform node represents a Media Foundation transform (MFT), such as a decoder or encoder.</span></span> <span data-ttu-id="e71e7-105">Es gibt verschiedene Möglichkeiten, einen Transformations Knoten zu initialisieren:</span><span class="sxs-lookup"><span data-stu-id="e71e7-105">There are several different ways to initialize a transform node:</span></span>

-   <span data-ttu-id="e71e7-106">Von einem Zeiger auf die MFT.</span><span class="sxs-lookup"><span data-stu-id="e71e7-106">From a pointer to the MFT.</span></span>
-   <span data-ttu-id="e71e7-107">Von einer CLSID für die MFT.</span><span class="sxs-lookup"><span data-stu-id="e71e7-107">From a CLSID for the MFT.</span></span>
-   <span data-ttu-id="e71e7-108">Von einem Zeiger auf ein Aktivierungs Objekt für die MFT.</span><span class="sxs-lookup"><span data-stu-id="e71e7-108">From a pointer to an activation object for the MFT.</span></span>

<span data-ttu-id="e71e7-109">Wenn Sie die Topologie innerhalb des geschützten Medien Pfads (PMP) laden möchten, müssen Sie entweder die CLSID oder ein Aktivierungs Objekt verwenden, damit die MFT im geschützten Prozess erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e71e7-109">If you are going to load the topology inside the protected media path (PMP), you must use either the CLSID or an activation object, so that the MFT can be created inside the protected process.</span></span> <span data-ttu-id="e71e7-110">Der erste Ansatz (mithilfe eines Zeigers auf die MFT) funktioniert nicht mit dem PMP.</span><span class="sxs-lookup"><span data-stu-id="e71e7-110">The first approach (using a pointer to the MFT) does not work with the PMP.</span></span>

## <a name="creating-a-transform-node-from-an-mft"></a><span data-ttu-id="e71e7-111">Erstellen eines Transformations Knotens aus einem MFT</span><span class="sxs-lookup"><span data-stu-id="e71e7-111">Creating a Transform Node from an MFT</span></span>

<span data-ttu-id="e71e7-112">Gehen Sie folgendermaßen vor, um einen Transformations Knoten von einem MFT zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e71e7-112">To create a transform node from an MFT, do the following:</span></span>

1.  <span data-ttu-id="e71e7-113">Erstellen Sie eine Instanz des MFT, und rufen Sie einen Zeiger auf die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle der MFT ab.</span><span class="sxs-lookup"><span data-stu-id="e71e7-113">Create an instance of the MFT and get a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the MFT.</span></span>
2.  <span data-ttu-id="e71e7-114">Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Knoten Flag für die **MF- \_ Topologie \_ \_** auf, um den Transformations Knoten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e71e7-114">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="e71e7-115">Nennen Sie [**imftopologynode:: abtobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) , und übergeben Sie den [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="e71e7-115">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer.</span></span>
4.  <span data-ttu-id="e71e7-116">Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e71e7-116">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="e71e7-117">Im folgenden Beispiel wird ein Transformations Knoten von einem MFT erstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e71e7-117">The following example creates and initializes a transform node from an MFT.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFTransform *pMFT,         // MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pMFT);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-a-clsid"></a><span data-ttu-id="e71e7-118">Erstellen eines Transformations Knotens aus einer CLSID</span><span class="sxs-lookup"><span data-stu-id="e71e7-118">Creating a Transform Node from a CLSID</span></span>

<span data-ttu-id="e71e7-119">Gehen Sie folgendermaßen vor, um einen Transformations Knoten aus einer CLSID zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e71e7-119">To create a transform node from a CLSID, do the following:</span></span>

1.  <span data-ttu-id="e71e7-120">Suchen Sie die CLSID des MFT.</span><span class="sxs-lookup"><span data-stu-id="e71e7-120">Find the CLSID of the MFT.</span></span> <span data-ttu-id="e71e7-121">Sie können die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion verwenden, um die CLSIDs von MFTs nach Kategorie zu suchen, z. b. Decoder oder Encoder.</span><span class="sxs-lookup"><span data-stu-id="e71e7-121">You can use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function to find the CLSIDs of MFTs by category, such as decoders or encoders.</span></span> <span data-ttu-id="e71e7-122">Sie können auch die CLSID einer bestimmten MFT kennen, die Sie verwenden möchten (z. b. Wenn Sie Ihre eigene benutzerdefinierte MFT implementiert haben).</span><span class="sxs-lookup"><span data-stu-id="e71e7-122">You might also know the CLSID of a particular MFT that you want to use (for example, if you implemented your own custom MFT).</span></span>
2.  <span data-ttu-id="e71e7-123">Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Knoten Flag für die **MF- \_ Topologie \_ \_** auf, um den Transformations Knoten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e71e7-123">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="e71e7-124">Legen Sie das Attribut " **MF \_ toponode \_ Transform \_ objectID** " für den Knoten fest.</span><span class="sxs-lookup"><span data-stu-id="e71e7-124">Set the **MF\_TOPONODE\_TRANSFORM\_OBJECTID** attribute on the node.</span></span> <span data-ttu-id="e71e7-125">Der Attribut Wert ist die CLSID.</span><span class="sxs-lookup"><span data-stu-id="e71e7-125">The attribute value is the CLSID.</span></span>
4.  <span data-ttu-id="e71e7-126">Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e71e7-126">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="e71e7-127">Im folgenden Beispiel wird ein Transformations Knoten aus einer CLSID erstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e71e7-127">The following example creates and initializes a transform node from a CLSID.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    const CLSID& clsid,         // CLSID of the MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the CLSID attribute.

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, clsid);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-an-activation-object"></a><span data-ttu-id="e71e7-128">Erstellen eines Transformations Knotens aus einem Aktivierungs Objekt</span><span class="sxs-lookup"><span data-stu-id="e71e7-128">Creating a Transform Node from an Activation Object</span></span>

<span data-ttu-id="e71e7-129">Einige MFTs stellen Aktivierungs Objekte bereit.</span><span class="sxs-lookup"><span data-stu-id="e71e7-129">Some MFTs provide activation objects.</span></span> <span data-ttu-id="e71e7-130">Beispielsweise gibt die [**MF**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) -Funktion (MF-Datei) ein Aktivierungs Objekt für den Windows Media Audio (WMA)-Encoder zurück.</span><span class="sxs-lookup"><span data-stu-id="e71e7-130">For example, the [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) function returns an activation object for the Windows Media Audio (WMA) encoder.</span></span> <span data-ttu-id="e71e7-131">Die genaue Funktion hängt vom MFT ab.</span><span class="sxs-lookup"><span data-stu-id="e71e7-131">The exact function depends on the MFT.</span></span> <span data-ttu-id="e71e7-132">Nicht jede MFT stellt ein Aktivierungs Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="e71e7-132">Not every MFT provides an activation object.</span></span> <span data-ttu-id="e71e7-133">Weitere Informationen finden Sie unter [Activation Objects](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e71e7-133">For more information, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="e71e7-134">Sie können auch ein MFT-Aktivierungs Objekt abrufen, indem Sie die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e71e7-134">You can also get an MFT activation object by calling the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="e71e7-135">Gehen Sie folgendermaßen vor, um einen Transformations Knoten aus einem Aktivierungs Objekt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e71e7-135">To create a transform node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="e71e7-136">Erstellen Sie das Aktivierungs Objekt, und rufen Sie einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle des Aktivierungs Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="e71e7-136">Create the activation object and get a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface of the activation object.</span></span>
2.  <span data-ttu-id="e71e7-137">Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Knoten Flag für die **MF- \_ Topologie \_ \_** auf, um den Transformations Knoten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e71e7-137">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="e71e7-138">Nennen Sie [**imftopologynode:: abtobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) , und übergeben Sie den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="e71e7-138">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
4.  <span data-ttu-id="e71e7-139">Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e71e7-139">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="e71e7-140">Im folgenden Beispiel wird ein Transformations Knoten von einem Aktivierungs Objekt erstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e71e7-140">The following example creates and initializes a transform node from an activation object.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // MFT activation object.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pActivate);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e71e7-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e71e7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e71e7-142">Erstellen von Topologien</span><span class="sxs-lookup"><span data-stu-id="e71e7-142">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="e71e7-143">Topologien</span><span class="sxs-lookup"><span data-stu-id="e71e7-143">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="e71e7-144">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="e71e7-144">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



