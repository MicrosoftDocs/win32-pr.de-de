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
# <a name="how-to-set-the-playback-stop-time"></a>Festlegen der Endzeit für die Wiedergabe Wiedergabe

In diesem Thema wird beschrieben, wie eine Endzeit für die Wiedergabe bei Verwendung der [Medien Sitzung](media-session.md)festgelegt wird.

## <a name="setting-the-stop-time-before-playback-begins"></a>Festlegen der Endzeit vor der Wiedergabe

Bevor Sie eine Topologie für die Wiedergabe in die Warteschlange stellen, können Sie die Endzeit mithilfe des [MF- \_ toponode \_ mediastop](mf-toponode-mediastop-attribute.md) -Attributs angeben. Legen Sie für jeden Ausgabe Knoten in der Topologie den Wert von MF \_ toponode \_ mediastop auf die Endzeit in 100-Nanosecond-Einheiten fest.

Beachten Sie, dass das Festlegen dieses Attributs nach dem wiedergeben keine Auswirkung hat. Legen Sie daher vor dem Aufrufen von [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)das-Attribut fest.

Der folgende Code zeigt, wie die Endzeit für eine vorhandene Topologie festgelegt wird.


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



## <a name="setting-the-stop-time-after-playback-has-started"></a>Festlegen der Endzeit, nachdem die Wiedergabe gestartet wurde

Mithilfe der [**imftopologynodeattributeeditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) -Schnittstelle kann die beendenden Zeit nach der Wiedergabe der [Medien Sitzung](media-session.md) festgelegt werden.

> [!IMPORTANT]
> Diese Schnittstelle hat eine ernsthafte Einschränkung, da die Endzeit als 32-Bit-Wert angegeben wird. Dies bedeutet, dass die maximale Endzeit, die Sie mithilfe dieser Schnittstelle festlegen können, 0xFFFFFFFF oder nur über 7 Minuten beträgt. Diese Einschränkung ist auf eine falsche Struktur Definition zurückzuführen.

 

Führen Sie die folgenden Schritte aus, um die Endzeit mithilfe der [**imftopologynodeattributeeditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) -Schnittstelle festzulegen.

1.  Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) zum Abrufen der [**imftopologynodeattributeeditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) -Schnittstelle aus der Medien Sitzung.
2.  Aufrufen von [**imftopology:: gettopologyid**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) zum Abrufen der ID der Wiedergabe Topologie.
3.  Nennen Sie für jeden Ausgabe Knoten in der Topologie [**imftopologynodeattributeeditor:: updatenodeattributs**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes). Diese Methode nimmt die topologiekennung und einen Zeiger auf die Update Struktur des [**mftoponode- \_ \_ Attributs**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) an. Initialisieren Sie die Struktur wie folgt.

    | Member               | Wert                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | **NodeId**           | Die Knoten-ID. Um die Knoten-ID abzurufen, wenden Sie den Befehl [**imftopologynode:: gettoponodeid**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid)an. |
    | **guidattributekey** | **MF- \_ toponode- \_ mediastop**                                                                                         |
    | **attrtype**         | **MF- \_ Attribut \_ UINT64**                                                                                           |
    | **u64**              | Die Endzeit in 100-Nanosecond-Einheiten.                                                                             |

    

     

Achten Sie darauf, den Wert von **attrtype** ordnungsgemäß festzulegen. Obwohl **U64** ein 32-Bit-Typ ist, erfordert die-Methode, dass **attrtype** auf das **MF- \_ Attribut \_ UINT64** festgelegt wird.

Der folgende Code zeigt diese Schritte.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> </dl>

 

 



