---
description: Wird ausgelöst, nachdem die ASYNCHRONOUSMediaSession::SetTopology-Methode asynchron abgeschlossen wurde. Die Mediensitzung löst dieses Ereignis aus, nachdem die Topologie in eine vollständige Topologie aufgelöst und die Topologie für die Wiedergabe in die Warteschlange eingereiht wurde.
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: MESessionTopologySet-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2b5454309855ff472c633388cddabe0c12fab09e2ae462aacd2de49c3c9bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957400"
---
# <a name="mesessiontopologyset-event"></a>MESessionTopologySet-Ereignis

Wird ausgelöst, nachdem die [**ASYNCHRONOUSMediaSession::SetTopology-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) asynchron abgeschlossen wurde. Die Mediensitzung löst dieses Ereignis aus, nachdem die Topologie in eine vollständige Topologie aufgelöst und die Topologie für die Wiedergabe in die Warteschlange eingereiht wurde.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE                | BESCHREIBUNG                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Keine Ereignisdaten.<br/> <br/>                                                                    |
| VT \_ UNKNOWN<br/> | Zeiger auf die [**INTERFACESTopology-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) der vollständigen Topologie.<br/> <br/> |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird der [**POINTERTopology-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) aus einem MESessionTopologySet-Ereignis abgerufen.


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




