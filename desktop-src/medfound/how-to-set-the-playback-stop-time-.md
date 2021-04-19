---
description: In diesem Thema wird beschrieben, wie eine Endzeit für die Wiedergabe bei Verwendung der Medien Sitzung festgelegt wird.
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: Festlegen der Endzeit für die Wiedergabe Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65269260b1e40d7907f0233fad653deb9636848b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347843"
---
# <a name="how-to-set-the-playback-stop-time"></a><span data-ttu-id="aca4d-103">Festlegen der Endzeit für die Wiedergabe Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="aca4d-103">How to Set the Playback Stop Time</span></span>

<span data-ttu-id="aca4d-104">In diesem Thema wird beschrieben, wie eine Endzeit für die Wiedergabe bei Verwendung der [Medien Sitzung](media-session.md)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="aca4d-104">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span>

## <a name="setting-the-stop-time-before-playback-begins"></a><span data-ttu-id="aca4d-105">Festlegen der Endzeit vor der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="aca4d-105">Setting the Stop Time Before Playback Begins</span></span>

<span data-ttu-id="aca4d-106">Bevor Sie eine Topologie für die Wiedergabe in die Warteschlange stellen, können Sie die Endzeit mithilfe des [MF- \_ toponode \_ mediastop](mf-toponode-mediastop-attribute.md) -Attributs angeben.</span><span class="sxs-lookup"><span data-stu-id="aca4d-106">Before you queue a topology for playback, you can specify the stop time by using the [MF\_TOPONODE\_MEDIASTOP](mf-toponode-mediastop-attribute.md) attribute.</span></span> <span data-ttu-id="aca4d-107">Legen Sie für jeden Ausgabe Knoten in der Topologie den Wert von MF \_ toponode \_ mediastop auf die Endzeit in 100-Nanosecond-Einheiten fest.</span><span class="sxs-lookup"><span data-stu-id="aca4d-107">For each output node in the topology, set the value of the MF\_TOPONODE\_MEDIASTOP to the stop time in 100-nanosecond units.</span></span>

<span data-ttu-id="aca4d-108">Beachten Sie, dass das Festlegen dieses Attributs nach dem wiedergeben keine Auswirkung hat.</span><span class="sxs-lookup"><span data-stu-id="aca4d-108">Note that setting this attribute after playback starts has no effect.</span></span> <span data-ttu-id="aca4d-109">Legen Sie daher vor dem Aufrufen von [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)das-Attribut fest.</span><span class="sxs-lookup"><span data-stu-id="aca4d-109">Therefore, set the attribute before calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

<span data-ttu-id="aca4d-110">Der folgende Code zeigt, wie die Endzeit für eine vorhandene Topologie festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="aca4d-110">The following code shows how to set the stop time on an existing topology.</span></span>


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD dwIndex, Q **ppObject)
{
    *ppObject = NULL;   // zero output

    IUnknown *pUnk = NULL;
    HRESULT hr = pCollection->GetElement(dwIndex, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObject));
        pUnk->Release();
    }
    return hr;
}

HRESULT SetMediaStop(IMFTopology *pTopology, const LONGLONG& stop)
{
    IMFCollection *pCol = NULL;
    DWORD cNodes;

    HRESULT hr = pTopology->GetSourceNodeCollection(&pCol);
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }
    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            IMFTopologyNode *pNode;
            hr = GetCollectionObject(pCol, i, &pNode);
            if (SUCCEEDED(hr))
            {
                pNode->SetUINT64(MF_TOPONODE_MEDIASTOP, stop);
            }
            pNode->Release();
        }
    }
    SafeRelease(&pCol);
    return hr;
}
```



## <a name="setting-the-stop-time-after-playback-has-started"></a><span data-ttu-id="aca4d-111">Festlegen der Endzeit, nachdem die Wiedergabe gestartet wurde</span><span class="sxs-lookup"><span data-stu-id="aca4d-111">Setting the Stop Time After Playback Has Started</span></span>

<span data-ttu-id="aca4d-112">Mithilfe der [**imftopologynodeattributeeditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) -Schnittstelle kann die beendenden Zeit nach der Wiedergabe der [Medien Sitzung](media-session.md) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aca4d-112">There is a way to set the stop time after the [Media Session](media-session.md) starts playback, by using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aca4d-113">Diese Schnittstelle hat eine ernsthafte Einschränkung, da die Endzeit als 32-Bit-Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aca4d-113">This interface has a serious limitation, because the stop time is specified as a 32-bit value.</span></span> <span data-ttu-id="aca4d-114">Dies bedeutet, dass die maximale Endzeit, die Sie mithilfe dieser Schnittstelle festlegen können, 0xFFFFFFFF oder nur über 7 Minuten beträgt.</span><span class="sxs-lookup"><span data-stu-id="aca4d-114">That means the maximum stop time that you can set using this interface is 0xFFFFFFFF, or just over 7 minutes.</span></span> <span data-ttu-id="aca4d-115">Diese Einschränkung ist auf eine falsche Struktur Definition zurückzuführen.</span><span class="sxs-lookup"><span data-stu-id="aca4d-115">This limitation is due to an incorrect structure definition.</span></span>

 

<span data-ttu-id="aca4d-116">Führen Sie die folgenden Schritte aus, um die Endzeit mithilfe der [**imftopologynodeattributeeditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) -Schnittstelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="aca4d-116">To set the stop time using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface, perform the following steps.</span></span>

1.  <span data-ttu-id="aca4d-117">Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) zum Abrufen der [**imftopologynodeattributeeditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) -Schnittstelle aus der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="aca4d-117">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface from the Media Session.</span></span>
2.  <span data-ttu-id="aca4d-118">Aufrufen von [**imftopology:: gettopologyid**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) zum Abrufen der ID der Wiedergabe Topologie.</span><span class="sxs-lookup"><span data-stu-id="aca4d-118">Call [**IMFTopology::GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) to get the ID of the playback topology.</span></span>
3.  <span data-ttu-id="aca4d-119">Nennen Sie für jeden Ausgabe Knoten in der Topologie [**imftopologynodeattributeeditor:: updatenodeattributs**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span><span class="sxs-lookup"><span data-stu-id="aca4d-119">For each output node in the topology, call [**IMFTopologyNodeAttributeEditor::UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span></span> <span data-ttu-id="aca4d-120">Diese Methode nimmt die topologiekennung und einen Zeiger auf die Update Struktur des [**mftoponode- \_ \_ Attributs**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) an.</span><span class="sxs-lookup"><span data-stu-id="aca4d-120">This method takes the topology ID and a pointer to a [**MFTOPONODE\_ATTRIBUTE\_UPDATE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) structure.</span></span> <span data-ttu-id="aca4d-121">Initialisieren Sie die Struktur wie folgt.</span><span class="sxs-lookup"><span data-stu-id="aca4d-121">Initialize the structure as follows.</span></span>

    | <span data-ttu-id="aca4d-122">Member</span><span class="sxs-lookup"><span data-stu-id="aca4d-122">Member</span></span>               | <span data-ttu-id="aca4d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="aca4d-123">Value</span></span>                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="aca4d-124">**NodeId**</span><span class="sxs-lookup"><span data-stu-id="aca4d-124">**NodeId**</span></span>           | <span data-ttu-id="aca4d-125">Die Knoten-ID.</span><span class="sxs-lookup"><span data-stu-id="aca4d-125">The node ID.</span></span> <span data-ttu-id="aca4d-126">Um die Knoten-ID abzurufen, wenden Sie den Befehl [**imftopologynode:: gettoponodeid**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid)an.</span><span class="sxs-lookup"><span data-stu-id="aca4d-126">To get the node ID, call call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span> |
    | <span data-ttu-id="aca4d-127">**guidattributekey**</span><span class="sxs-lookup"><span data-stu-id="aca4d-127">**guidAttributeKey**</span></span> | <span data-ttu-id="aca4d-128">**MF- \_ toponode- \_ mediastop**</span><span class="sxs-lookup"><span data-stu-id="aca4d-128">**MF\_TOPONODE\_MEDIASTOP**</span></span>                                                                                         |
    | <span data-ttu-id="aca4d-129">**attrtype**</span><span class="sxs-lookup"><span data-stu-id="aca4d-129">**attrType**</span></span>         | <span data-ttu-id="aca4d-130">**MF- \_ Attribut \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="aca4d-130">**MF\_ATTRIBUTE\_UINT64**</span></span>                                                                                           |
    | <span data-ttu-id="aca4d-131">**u64**</span><span class="sxs-lookup"><span data-stu-id="aca4d-131">**u64**</span></span>              | <span data-ttu-id="aca4d-132">Die Endzeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="aca4d-132">The stop time, in 100-nanosecond units.</span></span>                                                                             |

    

     

<span data-ttu-id="aca4d-133">Achten Sie darauf, den Wert von **attrtype** ordnungsgemäß festzulegen.</span><span class="sxs-lookup"><span data-stu-id="aca4d-133">Be careful to set the value of **attrType** correctly.</span></span> <span data-ttu-id="aca4d-134">Obwohl **U64** ein 32-Bit-Typ ist, erfordert die-Methode, dass **attrtype** auf das **MF- \_ Attribut \_ UINT64** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="aca4d-134">Although **u64** is a 32-bit type, the method requires that **attrType** be set to **MF\_ATTRIBUTE\_UINT64**.</span></span>

<span data-ttu-id="aca4d-135">Der folgende Code zeigt diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="aca4d-135">The following code shows these steps.</span></span>


```C++
HRESULT SetMediaStopDynamic(IMFMediaSession *pSession, IMFTopology *pTopology, const LONGLONG& stop)
{
    if (stop > MAXUINT32)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNodeAttributeEditor *pAttr = NULL;
    IMFCollection *pCol = NULL;
    IMFTopologyNode *pNode = NULL;

    HRESULT hr = MFGetService(pSession, MF_TOPONODE_ATTRIBUTE_EDITOR_SERVICE, IID_PPV_ARGS(&pAttr));
    if (FAILED(hr))
    {
        goto done;
    }

    TOPOID id;
    hr = pTopology->GetTopologyID(&id);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cNodes;
    hr = pTopology->GetSourceNodeCollection(&pCol);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pCol->GetElementCount(&cNodes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cNodes; i++)
    {
        IMFTopologyNode *pNode;
        hr = GetCollectionObject(pCol, i, &pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        TOPOID nodeID;
        hr = pNode->GetTopoNodeID(&nodeID);
        if (FAILED(hr))
        {
            goto done;
        }

        MFTOPONODE_ATTRIBUTE_UPDATE update;
        update.NodeId = nodeID;
        update.guidAttributeKey = MF_TOPONODE_MEDIASTOP;
        update.attrType = MF_ATTRIBUTE_UINT64;
        update.u64 = (UINT32)stop;

        hr = pAttr->UpdateNodeAttributes(id, 1, &update);
        if (FAILED(hr))
        {
            goto done;
        }
        SafeRelease(&pNode);
    }

done:
    SafeRelease(&pNode);
    SafeRelease(&pCol);
    SafeRelease(&pAttr);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="aca4d-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aca4d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aca4d-137">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="aca4d-137">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



