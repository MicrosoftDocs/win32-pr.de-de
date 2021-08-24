---
description: In diesem Thema wird beschrieben, wie Sie bei Verwendung der Mediensitzung eine Beendigungszeit für die Wiedergabe festlegen.
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: Festlegen der Wiedergabestoppzeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c14145f798795dfeb8116195afad2f020eb4219b9c2529f96b8fa904f2e1d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466000"
---
# <a name="how-to-set-the-playback-stop-time"></a>Festlegen der Wiedergabestoppzeit

In diesem Thema wird beschrieben, wie eine Beendigungszeit für die Wiedergabe festgelegt wird, wenn die [Mediensitzung](media-session.md)verwendet wird.

## <a name="setting-the-stop-time-before-playback-begins"></a>Festlegen der Beendigungszeit vor Beginn der Wiedergabe

Bevor Sie eine Topologie für die Wiedergabe in die Warteschlange stellen, können Sie die Beendigungszeit mithilfe des [MF \_ TOPONODE \_ MEDIASTOP-Attributs](mf-toponode-mediastop-attribute.md) angeben. Legen Sie für jeden Ausgabeknoten in der Topologie den Wert von MF \_ TOPONODE \_ MEDIASTOP auf die Beendigungszeit in Einheiten von 100 Nanosekunden fest.

Beachten Sie, dass das Festlegen dieses Attributs nach dem Start der Wiedergabe keine Auswirkungen hat. Legen Sie daher das -Attribut fest, bevor Sie [**DIESMEDIASession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)aufrufen.

Der folgende Code zeigt, wie die Beendigungszeit für eine vorhandene Topologie festgelegt wird.


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



## <a name="setting-the-stop-time-after-playback-has-started"></a>Festlegen der Beendigungszeit nach dem Starten der Wiedergabe

Es gibt eine Möglichkeit, die Beendigungszeit festzulegen, nachdem die [Mediensitzung](media-session.md) mit der Wiedergabe begonnen hat, indem Sie die [**SCHNITTSTELLE VONTOPTOPOLOGYNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) verwenden.

> [!IMPORTANT]
> Diese Schnittstelle weist eine schwerwiegende Einschränkung auf, da die Beendigungszeit als 32-Bit-Wert angegeben wird. Dies bedeutet, dass die maximale Beendigungszeit, die Sie mit dieser Schnittstelle festlegen können, 0xFFFFFFFF oder etwas mehr als 7 Minuten beträgt. Diese Einschränkung ist auf eine falsche Strukturdefinition zurückzuführen.

 

Führen Sie die folgenden Schritte aus, um die Beendigungszeit mithilfe der [**SCHNITTSTELLE VONTOPTOPOLOGYNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) festzulegen.

1.  Rufen Sie [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) auf, um die [**SCHNITTSTELLE VOMTOPTOPOLOGYNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) aus der Mediensitzung abzurufen.
2.  Rufen Sie [**DIE TOPOLOGIE::GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) auf, um die ID der Wiedergabetopologie abzurufen.
3.  Rufen Sie für jeden Ausgabeknoten in der Topologie [**DIE ATTRIBUTETopologyNodeAttributeEditor::UpdateNodeAttributes auf.**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes) Diese Methode verwendet die Topologie-ID und einen Zeiger auf eine [**MFTOPONODE \_ ATTRIBUTE \_ UPDATE-Struktur.**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) Initialisieren Sie die -Struktur wie folgt.

    | Member               | Wert                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | **NodeId**           | Die Knoten-ID. Rufen Sie ZUM Abrufen der Knoten-ID DEN AUFRUF [**VONTOPTOPOLOGYNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid)auf. |
    | **guidAttributeKey** | **MF \_ TOPONODE \_ MEDIASTOP**                                                                                         |
    | **attrType**         | **\_MF-ATTRIBUT \_ UINT64**                                                                                           |
    | **u64**              | Die Beendigungszeit in Einheiten von 100 Nanosekunden.                                                                             |

    

     

Achten Sie darauf, dass Sie den Wert von **attrType** richtig festlegen. Obwohl **u64** ein 32-Bit-Typ ist, erfordert die -Methode, dass **attrType** auf **MF ATTRIBUTE \_ \_ UINT64** festgelegt wird.

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

 

 



