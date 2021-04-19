---
description: Hinzufügen eines Decoders zu einer Topologie
ms.assetid: 32c088d5-d9dd-43d3-a63b-219e6a7a36b1
title: Hinzufügen eines Decoders zu einer Topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506963ee65490365b60788808a4da87c21355247
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359824"
---
# <a name="adding-a-decoder-to-a-topology"></a><span data-ttu-id="67ad4-103">Hinzufügen eines Decoders zu einer Topologie</span><span class="sxs-lookup"><span data-stu-id="67ad4-103">Adding a Decoder to a Topology</span></span>

<span data-ttu-id="67ad4-104">In diesem Thema wird beschrieben, wie Sie eine Audiodatei oder einen Video Decoder zu einer Topologie hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67ad4-104">This topic describes how to add an audio or video decoder to a topology.</span></span>

<span data-ttu-id="67ad4-105">Bei den meisten Wiedergabe Anwendungen können Sie die Decoder aus der partiellen Topologie weglassen, die Sie an die Medien Sitzung senden.</span><span class="sxs-lookup"><span data-stu-id="67ad4-105">For most playback applications, you can omit the decoders from the partial topology that you send to the Media Session.</span></span> <span data-ttu-id="67ad4-106">Die Medien Sitzung verwendet den topologielader zum Vervollständigen der Topologie, und das topologielader fügt alle benötigten Decoder ein.</span><span class="sxs-lookup"><span data-stu-id="67ad4-106">The Media Session uses the topology loader to complete the topology, and the topology loader inserts any decoders that are needed.</span></span> <span data-ttu-id="67ad4-107">Wenn Sie jedoch einen bestimmten Decoder auswählen möchten, können Sie der Topologie manuell einen Decoder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67ad4-107">If you want to select a particular decoder, however, you can manually add a decoder to the topology.</span></span>

<span data-ttu-id="67ad4-108">Hier finden Sie die allgemeinen Schritte zum Hinzufügen eines Decoders zu einer Topologie.</span><span class="sxs-lookup"><span data-stu-id="67ad4-108">Here are the overall steps for adding a decoder to a topology.</span></span>

1.  <span data-ttu-id="67ad4-109">Suchen Sie die CLSID des Decoders.</span><span class="sxs-lookup"><span data-stu-id="67ad4-109">Find the CLSID of the decoder.</span></span>
2.  <span data-ttu-id="67ad4-110">Fügen Sie einen Knoten für den Decoder in der Topologie hinzu.</span><span class="sxs-lookup"><span data-stu-id="67ad4-110">Add a node for the decoder in the topology.</span></span>
3.  <span data-ttu-id="67ad4-111">Aktivieren Sie für einen Video Decoder die DirectX-Videobeschleunigung.</span><span class="sxs-lookup"><span data-stu-id="67ad4-111">For a video decoder, enable DirectX Video Acceleration.</span></span> <span data-ttu-id="67ad4-112">Dieser Schritt ist für Audiodecoder nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="67ad4-112">This step is not required for audio decoders.</span></span>

## <a name="find-the-decoder-clsid"></a><span data-ttu-id="67ad4-113">Suchen der decoderclsid</span><span class="sxs-lookup"><span data-stu-id="67ad4-113">Find the Decoder CLSID</span></span>

<span data-ttu-id="67ad4-114">Wenn Sie einen bestimmten Decoder verwenden möchten, sind Sie möglicherweise bereits mit der CLSID des Decoders vertraut.</span><span class="sxs-lookup"><span data-stu-id="67ad4-114">If you want to use a particular decoder, you might already know the CLSID of the decoder.</span></span> <span data-ttu-id="67ad4-115">In diesem Fall können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="67ad4-115">If so, you can skip this step.</span></span> <span data-ttu-id="67ad4-116">Verwenden Sie andernfalls die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion, um die CLSID in der Registrierung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="67ad4-116">Otherwise, use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function to look up the CLSID in the registry.</span></span> <span data-ttu-id="67ad4-117">Diese Funktion nimmt mehrere Suchkriterien als Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="67ad4-117">This function takes several search criteria as input.</span></span> <span data-ttu-id="67ad4-118">Wenn Sie einen Decoder suchen möchten, müssen Sie nur das Eingabeformat angeben (Haupttyp und Untertyp).</span><span class="sxs-lookup"><span data-stu-id="67ad4-118">To find a decoder, you need to specify only the input format (major type and subtype).</span></span> <span data-ttu-id="67ad4-119">Sie können diese aus dem Datenstrom Deskriptor erhalten, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="67ad4-119">You can get these from the stream descriptor, as shown in the following code.</span></span>


```C++
// Returns the MFT decoder based on the major type GUID.

HRESULT GetDecoderCategory(const GUID& majorType, GUID *pCategory)
{
    if (majorType == MFMediaType_Video)
    {
        *pCategory = MFT_CATEGORY_VIDEO_DECODER;
    }
    else if (majorType == MFMediaType_Audio)
    {
        *pCategory = MFT_CATEGORY_AUDIO_DECODER;
    }
    else
    {
        return MF_E_INVALIDMEDIATYPE;
    }
    return S_OK;
}

// Finds a decoder for a stream.
//
// If the stream is not compressed, pCLSID receives the value GUID_NULL.

HRESULT FindDecoderForStream(
    IMFStreamDescriptor *pSD,   // Stream descriptor for the stream.
    CLSID *pCLSID               // Receives the CLSID of the decoder.
    )
{
    BOOL    bIsCompressed = FALSE;
    GUID    guidMajorType = GUID_NULL;
    GUID    guidSubtype = GUID_NULL;
    GUID    guidDecoderCategory = GUID_NULL;

    CLSID *pDecoderCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cDecoderCLSIDs = NULL;   // Size of the array.

    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pMediaType = NULL;

    // Find the media type for the stream.
    HRESULT hr = pSD->GetMediaTypeHandler(&pHandler);

    if (SUCCEEDED(hr))
    {
        hr = pHandler->GetCurrentMediaType(&pMediaType);
    }

    // Get the major type and subtype.
    if (SUCCEEDED(hr))
    {
        hr = pMediaType->GetMajorType(&guidMajorType);
    }

    if (SUCCEEDED(hr))
    {
        hr = pMediaType->GetGUID(MF_MT_SUBTYPE, &guidSubtype);
    }

    // Check whether the stream is compressed.
    if (SUCCEEDED(hr))
    {
        hr = pMediaType->IsCompressedFormat(&bIsCompressed);
    }

#if (WINVER < _WIN32_WINNT_WIN7)

    // Starting in Windows 7, you can connect an uncompressed video source 
    // directly to the EVR. In earlier versions of Media Foundation, this
    // is not supported.

    if (SUCCEEDED(hr))
    {
        if (!bIsCompressed && (guidMajorType == MFMediaType_Video))
        {
            hr = MF_E_INVALIDMEDIATYPE;
        }
    }
#endif

    // If the stream is compressed, find a decoder.
    if (SUCCEEDED(hr))
    {
        if (bIsCompressed)
        {
            // Select the decoder category from the major type (audio/video).
            hr = GetDecoderCategory(guidMajorType, &guidDecoderCategory);

            // Look for a decoder.

            if (SUCCEEDED(hr))
            {
                MFT_REGISTER_TYPE_INFO tinfo;
                tinfo.guidMajorType = guidMajorType;
                tinfo.guidSubtype = guidSubtype;

                hr = MFTEnum(
                        guidDecoderCategory,
                        0,               // Reserved
                        &tinfo,          // Input type to match. (Encoded type.)
                        NULL,            // Output type to match. (Don't care.)
                        NULL,            // Attributes to match. (None.)
                        &pDecoderCLSIDs, // Receives a pointer to an array of CLSIDs.
                        &cDecoderCLSIDs  // Receives the size of the array.
                        );
            }

            // MFTEnum can return zero matches.
            if (SUCCEEDED(hr) && (cDecoderCLSIDs == 0))
            {
                hr = MF_E_TOPO_CODEC_NOT_FOUND;
            }

            // Return the first CLSID in the list to the caller.
            if (SUCCEEDED(hr))
            {
                *pCLSID = pDecoderCLSIDs[0];
            }
        }
        else
        {
            // Uncompressed. A decoder is not required.
            *pCLSID = GUID_NULL;
        }
    }

    SafeRelease(&pHandler);
    SafeRelease(&pMediaType);
    CoTaskMemFree(pDecoderCLSIDs);

    return hr;
}
```



<span data-ttu-id="67ad4-120">Weitere Informationen zu streamdeskriptoren finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="67ad4-120">For more information about stream descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="67ad4-121">Die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion gibt einen Zeiger auf ein Array von CLSIDs zurück.</span><span class="sxs-lookup"><span data-stu-id="67ad4-121">The [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function returns a pointer to an array of CLSIDs.</span></span> <span data-ttu-id="67ad4-122">Die Reihenfolge des zurückgegebenen Arrays ist willkürlich.</span><span class="sxs-lookup"><span data-stu-id="67ad4-122">The order of the returned array is arbitrary.</span></span> <span data-ttu-id="67ad4-123">In diesem Beispiel verwendet die-Funktion die erste CLSID im-Array.</span><span class="sxs-lookup"><span data-stu-id="67ad4-123">In this example, the function uses the first CLSID in the array.</span></span> <span data-ttu-id="67ad4-124">Weitere Informationen zu einem Decoder, einschließlich des anzeigen Amens des Decoders, erhalten Sie durch Aufrufen von " [**mftgetinfo**](/windows/desktop/api/mfapi/nf-mfapi-mftgetinfo)".</span><span class="sxs-lookup"><span data-stu-id="67ad4-124">You can get more information about a decoder, including the friendly name of the decoder, by calling [**MFTGetInfo**](/windows/desktop/api/mfapi/nf-mfapi-mftgetinfo).</span></span> <span data-ttu-id="67ad4-125">Beachten Sie außerdem, dass **mftenum** erfolgreich sein kann, aber ein leeres Array zurückgibt. Daher ist es wichtig, die Array Größe zu überprüfen, die im letzten Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="67ad4-125">Also, note that **MFTEnum** can succeed but return an empty array, so it is important to check the array size, which is returned in the last parameter.</span></span>

## <a name="add-the-decoder-node-to-the-topology"></a><span data-ttu-id="67ad4-126">Fügen Sie den Decoder-Knoten der Topologie hinzu.</span><span class="sxs-lookup"><span data-stu-id="67ad4-126">Add the Decoder Node to the Topology</span></span>

<span data-ttu-id="67ad4-127">Nachdem Sie die CLSID für den Decoder erstellt haben, erstellen Sie einen neuen Transformations Knoten durch Aufrufen von [**mfcreatetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="67ad4-127">After you have the CLSID for the decoder, create a new transform node by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span> <span data-ttu-id="67ad4-128">Geben Sie die CLSID an, indem Sie das [**MF \_ toponode \_ Transform \_ objectID**](mf-toponode-transform-objectid-attribute.md) -Attribut auf dem Knoten festlegen.</span><span class="sxs-lookup"><span data-stu-id="67ad4-128">Specify the CLSID by setting the [**MF\_TOPONODE\_TRANSFORM\_OBJECTID**](mf-toponode-transform-objectid-attribute.md) attribute on the node.</span></span> <span data-ttu-id="67ad4-129">Ein Beispiel zum Erstellen eines Transformations Knotens finden Sie unter [Erstellen von Transformations Knoten](creating-transform-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="67ad4-129">For an example of how to create a transform node, see [Creating Transform Nodes](creating-transform-nodes.md).</span></span> <span data-ttu-id="67ad4-130">Verbinden Sie dann den Quellknoten mit dem Decoder-Knoten und dem Decoder-Knoten mit dem Ausgabe Knoten, indem Sie [**imftopologynode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="67ad4-130">Then connect the source node to the decoder node, and the decoder node to the output node, by calling [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput).</span></span>

<span data-ttu-id="67ad4-131">Im folgenden Beispiel wird gezeigt, wie Sie die Knoten erstellen und verbinden.</span><span class="sxs-lookup"><span data-stu-id="67ad4-131">The following example shows how to create the nodes and connect them.</span></span> <span data-ttu-id="67ad4-132">Das Beispiel ähnelt der Beispiel Funktion mit dem Namen `AddBranchToPartialTopology` , die im Thema [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md)gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="67ad4-132">The example is very similar to the example function named `AddBranchToPartialTopology` that is shown in the topic [Creating Playback Topologies](creating-playback-topologies.md).</span></span> <span data-ttu-id="67ad4-133">Der einzige Unterschied besteht darin, dass in diesem Beispiel der zusätzliche Knoten für den Decoder hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="67ad4-133">The only difference is that this example adds the extra node for the decoder.</span></span>


```C++
HRESULT AddBranchToPartialTopologyWithDecoder(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd                  // Window for video playback.
    )
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;
    IMFTopologyNode     *pDecoderNode = NULL;

    BOOL fSelected = FALSE;
    CLSID clsidDecoder = GUID_NULL;

    // Get the stream descriptor.
    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        return hr;
    }

    if (fSelected)
    {
        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);

        // Create the media sink activation object.
        if (SUCCEEDED(hr))
        {
            hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        }

        // Create the output node for the renderer.
        if (SUCCEEDED(hr))
        {
            hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        }

        // Find a decoder.
        if (SUCCEEDED(hr))
        {
            hr = FindDecoderForStream(pSD, &clsidDecoder);
        }

        if (SUCCEEDED(hr))
        {
            if (clsidDecoder == GUID_NULL)
            {
                // No decoder is required. 
                // Connect the source node to the output node.
                hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
            }
            else
            {
                // Add a decoder node.
                hr = AddTransformNode(pTopology, clsidDecoder, &pDecoderNode);

                // Connect the source node to the decoder node.
                if (SUCCEEDED(hr))
                {
                    hr = pSourceNode->ConnectOutput(0, pDecoderNode, 0);
                }

                // Connect the decoder node to the output node.
                if (SUCCEEDED(hr))
                {
                    hr = pDecoderNode->ConnectOutput(0, pOutputNode, 0);
                }
            }
        }

        // Mark this branch as not requiring a decoder.
        if (SUCCEEDED(hr))
        {
            hr = pOutputNode->SetUINT32(
                MF_TOPONODE_CONNECT_METHOD, 
                MF_CONNECT_ALLOW_CONVERTER
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pDecoderNode->SetUINT32(
                MF_TOPONODE_CONNECT_METHOD, 
                MF_CONNECT_ALLOW_CONVERTER
                );
        }

    }
    // else: If not selected, don't add the branch. 

    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pDecoderNode);

    return hr;
}
```



## <a name="enable-video-acceleration"></a><span data-ttu-id="67ad4-134">Video Beschleunigung aktivieren</span><span class="sxs-lookup"><span data-stu-id="67ad4-134">Enable Video Acceleration</span></span>

<span data-ttu-id="67ad4-135">Der nächste Schritt beim Hinzufügen eines Audio-oder Video-Decoders zu einer Topologie gilt nur für Video Decoder.</span><span class="sxs-lookup"><span data-stu-id="67ad4-135">The next step in adding an audio or video decoder to a topology applies only to video decoders.</span></span> <span data-ttu-id="67ad4-136">Um die beste Leistung für die Videowiedergabe zu erzielen, sollten Sie die DirectX-Videobeschleunigung (DXVA) aktivieren, wenn Sie vom Video Decoder unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="67ad4-136">To get the best performance for video playback, you should enable DirectX Video Acceleration (DXVA) if the video decoder supports it.</span></span> <span data-ttu-id="67ad4-137">Dieser Schritt wird normalerweise vom topologielader ausgeführt, aber wenn Sie den Decoder der Topologie manuell hinzufügen, müssen Sie diesen Schritt selbst ausführen.</span><span class="sxs-lookup"><span data-stu-id="67ad4-137">Usually this step is performed by the topology loader, but if you add the decoder to the topology manually, then you must perform this step yourself.</span></span>

<span data-ttu-id="67ad4-138">Als Vorbedingung für diesen Schritt müssen alle Ausgabe Knoten in der Topologie an Medien senken gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="67ad4-138">As a precondition for this step, all output nodes in the topology must be bound to media sinks.</span></span> <span data-ttu-id="67ad4-139">Weitere Informationen finden Sie unter [Binden von Ausgabe Knoten an Medien senken](binding-output-nodes-to-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="67ad4-139">For more information, see [Binding Output Nodes to Media Sinks](binding-output-nodes-to-media-sinks.md).</span></span>

<span data-ttu-id="67ad4-140">Suchen Sie zuerst das-Objekt in der Topologie, die den Direct3D-Geräte-Manager hostet.</span><span class="sxs-lookup"><span data-stu-id="67ad4-140">First, find the object in the topology that hosts the Direct3D device manager.</span></span> <span data-ttu-id="67ad4-141">Hierzu können Sie den Objekt Zeiger von jedem Knoten und das Objekt für den [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Dienst Abfragen.</span><span class="sxs-lookup"><span data-stu-id="67ad4-141">To do so, get the object pointer from each node and query the object for the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) service.</span></span> <span data-ttu-id="67ad4-142">In der Regel wird diese Rolle vom erweiterten Videorenderer (EVR) bedient.</span><span class="sxs-lookup"><span data-stu-id="67ad4-142">Typically the enhanced video renderer (EVR) serves this role.</span></span> <span data-ttu-id="67ad4-143">Der folgende Code zeigt eine Funktion, die den Geräte-Manager findet:</span><span class="sxs-lookup"><span data-stu-id="67ad4-143">The following code shows a function that finds the device manager:</span></span>


```C++
// Finds the node in the topology that provides the Direct3D device manager. 

HRESULT FindDeviceManager(
    IMFTopology *pTopology,         // Topology to search.
    IUnknown **ppDeviceManager,     // Receives a pointer to the device manager.
    IMFTopologyNode **ppNode        // Receives a pointer to the node.
    )
{
    HRESULT hr = S_OK;
    WORD cNodes = 0;
    BOOL bFound = FALSE;

    IMFTopologyNode *pNode = NULL;
    IUnknown *pNodeObject = NULL;
    IDirect3DDeviceManager9 *pD3DManager = NULL;

    // Search all of the nodes in the topology.
    
    hr = pTopology->GetNodeCount(&cNodes);

    if (FAILED(hr))
    {
        return hr;
    }

    for (WORD i = 0; i < cNodes; i++)
    {
        // For each of the following calls, failure just means we 
        // did not find the node we're looking for, so keep looking. 

        hr = pTopology->GetNode(i, &pNode);

        // Get the node's object pointer.
        if (SUCCEEDED(hr))
        {
            hr = pNode->GetObject(&pNodeObject);
        }

        // Query the node object for the device manager service.
        if (SUCCEEDED(hr))
        {
            hr = MFGetService(
                pNodeObject, 
                MR_VIDEO_ACCELERATION_SERVICE, 
                IID_PPV_ARGS(&pD3DManager)
                );
        }

        if (SUCCEEDED(hr))
        {
            // Found the right node. Return the pointers to the caller.
            *ppDeviceManager = pD3DManager;
            (*ppDeviceManager)->AddRef();

            *ppNode = pNode;
            (*ppNode)->AddRef();

            bFound = TRUE;
            break;
        }

        SafeRelease(&pNodeObject);
        SafeRelease(&pD3DManager);
        SafeRelease(&pNode);

    } // End of for loop.

    SafeRelease(&pNodeObject);
    SafeRelease(&pD3DManager);
    SafeRelease(&pNode);

    return bFound ? S_OK : E_FAIL;
}
```



<span data-ttu-id="67ad4-144">Suchen Sie als nächstes den Transformations Knoten, der direkt über den Knoten mit dem Direct3D-Geräte-Manager verfügt.</span><span class="sxs-lookup"><span data-stu-id="67ad4-144">Next, find the transform node that is directly upstream from the node that contains the Direct3D device manager.</span></span> <span data-ttu-id="67ad4-145">Hiermit wird der [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Zeiger von diesem Transformations Knoten abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="67ad4-145">Get the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer from this transform node.</span></span> <span data-ttu-id="67ad4-146">Der **imftransform** -Zeiger stellt eine Media Foundation Transformation (MFT) dar.</span><span class="sxs-lookup"><span data-stu-id="67ad4-146">The **IMFTransform** pointer represents a Media Foundation transform (MFT).</span></span> <span data-ttu-id="67ad4-147">Abhängig von der Art und Weise, wie der Knoten erstellt wurde, müssen Sie möglicherweise die MFT durch Aufrufen von **CoCreateInstance** erstellen oder die MFT von einem Aktivierungs Objekt aktivieren.</span><span class="sxs-lookup"><span data-stu-id="67ad4-147">Depending on how the node was created, you might need to create the MFT by calling **CoCreateInstance**, or activate the MFT from an activation object.</span></span> <span data-ttu-id="67ad4-148">Im folgenden Code werden alle unterschiedlichen Fälle behandelt:</span><span class="sxs-lookup"><span data-stu-id="67ad4-148">The following code handles all of the various cases:</span></span>


```C++
// Returns the MFT for a transform node.

HRESULT GetTransformFromNode(
    IMFTopologyNode *pNode, 
    IMFTransform **ppMFT
    )
{
    MF_TOPOLOGY_TYPE type = MF_TOPOLOGY_MAX;

    IUnknown *pNodeObject = NULL;
    IMFTransform *pMFT = NULL;
    IMFActivate *pActivate = NULL;
    IMFAttributes *pAttributes = NULL;

    // Is this a transform node?
    HRESULT hr = pNode->GetNodeType(&type);

    if (FAILED(hr))
    {
        return hr;
    }

    if (type != MF_TOPOLOGY_TRANSFORM_NODE)
    {
        // Wrong node type.
        return E_FAIL;
    }

    // Check whether the node has an object pointer.
    hr = pNode->GetObject(&pNodeObject);

    if (SUCCEEDED(hr))
    {
        // The object pointer should be one of the following:
        // 1. Pointer to an MFT.
        // 2. Pointer to an activation object.

        // Is it an MFT? Query for IMFTransform.
        hr = pNodeObject->QueryInterface(IID_IMFTransform, (void**)&pMFT);
        if (FAILED(hr))
        {
            // It is not an MFT, so it should be an activation object.
            hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pActivate));

            // Use the activation object to create the MFT.

            if (SUCCEEDED(hr))
            {
                hr = pActivate->ActivateObject(IID_PPV_ARGS(&pMFT));
            }

            // Replace the node's object pointer with the MFT.
            if (SUCCEEDED(hr))
            {
                hr = pNode->SetObject(pMFT);
            }

            // If the activation object has the MF_ACTIVATE_MFT_LOCKED 
            // attribute, transfer this value to the
            // MF_TOPONODE_MFT_LOCKED attribute on the node.
            // However, don't fail if this attribute is not found.
            if (SUCCEEDED(hr))
            {
                BOOL bLocked = MFGetAttributeUINT32(
                    pActivate, MF_ACTIVATE_MFT_LOCKED, FALSE);


                hr = pNode->SetUINT32(MF_TOPONODE_LOCKED, bLocked);
            }
        }
    }
    else
    {
        GUID clsidMFT;

        // The node does not have an object pointer. Look for a CLSID.
        hr = pNode->GetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, &clsidMFT);
       
        // Create the MFT.
        if (SUCCEEDED(hr))
        {
            hr = CoCreateInstance(
                clsidMFT, NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pMFT)
                );
        }

        // If the MFT supports attributes, copy the node attributes to the 
        // MFT attribute store. 
        if (SUCCEEDED(hr))
        {
            if (SUCCEEDED(pMFT->GetAttributes(&pAttributes)))
            {
                // Copy from pNode to pAttributes.
                hr = pNode->CopyAllItems(pAttributes); 
            }
        }

        // Set the object on the node.
        if (SUCCEEDED(hr))
        {
            hr = pNode->SetObject(pMFT);
        }
    }

    // Return the IMFTransform pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppMFT = pMFT;
        (*ppMFT)->AddRef();
    }

    SafeRelease(&pNodeObject);
    SafeRelease(&pMFT);
    SafeRelease(&pActivate);
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="67ad4-149">Wenn die MFT über das Attribut [**MF \_ sa \_ D3D \_ Aware**](mf-sa-d3d-aware-attribute.md) mit dem Wert **true** verfügt, bedeutet dies, dass die MFT eine DirectX-Video Beschleunigung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="67ad4-149">If the MFT has the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute with the value **TRUE**, it means that the MFT supports DirectX Video Acceleration.</span></span> <span data-ttu-id="67ad4-150">Die folgende Funktion testet auf dieses Attribut:</span><span class="sxs-lookup"><span data-stu-id="67ad4-150">The following function tests for this attribute:</span></span>


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



<span data-ttu-id="67ad4-151">Um die Videobeschleunigung auf diesem MFT zu aktivieren, wenden Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der Nachricht MFT \_ Message \_ Set \_ D3D \_ Manager an.</span><span class="sxs-lookup"><span data-stu-id="67ad4-151">To enable video acceleration on this MFT, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the MFT\_MESSAGE\_SET\_D3D\_MANAGER message.</span></span> <span data-ttu-id="67ad4-152">Legen Sie außerdem das [**MF- \_ toponode \_ D3DAWARE**](mf-toponode-d3daware-attribute.md) -Attribut für den Transformations Knoten auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="67ad4-152">Also set the [**MF\_TOPONODE\_D3DAWARE**](mf-toponode-d3daware-attribute.md) attribute to **TRUE** on the transform node.</span></span> <span data-ttu-id="67ad4-153">Mit diesem Attribut wird der Pipeline mitgeteilt, dass die Videobeschleunigung aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="67ad4-153">This attribute informs the pipeline that video acceleration has been enabled.</span></span> <span data-ttu-id="67ad4-154">Der folgende Code führt folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="67ad4-154">The following code performs these steps:</span></span>


```C++
// Enables or disables DirectX Video Acceleration in a topology.

HRESULT EnableVideoAcceleration(IMFTopology *pTopology, BOOL bEnable)
{
    IMFTopologyNode *pD3DManagerNode = NULL;
    IMFTopologyNode *pUpstreamNode = NULL;
    IUnknown *pD3DManager = NULL;
    IMFTransform *pMFT = NULL;

    // Look for the node that supports the Direct3D Manager.
    
    HRESULT hr = FindDeviceManager(pTopology, &pD3DManager, &pD3DManagerNode); 
    if (FAILED(hr))
    {
        //  There is no Direct3D device manager in the topology.
        //  This is not a failure case.
        return S_OK;
    }

    DWORD dwOutputIndex = 0;

    // Get the node upstream from the device manager node.
    hr = pD3DManagerNode->GetInput(0, &pUpstreamNode, &dwOutputIndex);

    // Get the MFT from the upstream node.
    if (SUCCEEDED(hr))
    {
        hr = GetTransformFromNode(pUpstreamNode, &pMFT);
    }

    // If the MFT is Direct3D-aware, notify the MFT of the device 
    // manager and mark the topology node as Direct3D-aware.
    if (SUCCEEDED(hr))
    {
        if (IsTransformD3DAware(pMFT))
        {
            ULONG_PTR ptr = bEnable ? (ULONG_PTR)pD3DManager : NULL;

            hr = pMFT->ProcessMessage(MFT_MESSAGE_SET_D3D_MANAGER, ptr);

            // Mark the node.
            if (SUCCEEDED(hr))
            {
                hr = pUpstreamNode->SetUINT32(MF_TOPONODE_D3DAWARE, bEnable);
            }
        }
    }

    SafeRelease(&pD3DManagerNode);
    SafeRelease(&pUpstreamNode);
    SafeRelease(&pD3DManager);
    SafeRelease(&pMFT);
    return hr;
}
```



<span data-ttu-id="67ad4-155">Weitere Informationen zu DXVA in Media Foundation finden Sie unter [DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="67ad4-155">For more information about DXVA in Media Foundation, see [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67ad4-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67ad4-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67ad4-157">Erweiterte topologiebildung</span><span class="sxs-lookup"><span data-stu-id="67ad4-157">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> </dl>

 

 



