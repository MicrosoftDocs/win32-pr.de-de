---
description: 'Wird ausgelöst, nachdem die imfmediasession:: settopology-Methode asynchron abgeschlossen wurde. Die Medien Sitzung löst dieses Ereignis aus, nachdem die Topologie in eine vollständige Topologie aufgelöst und die Topologie zur Wiedergabe in die Warteschlange eingereiht wurde.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Mesessiontopologyset-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959300"
---
# <a name="mesessiontopologyset-event"></a>Mesessiontopologyset-Ereignis

Wird ausgelöst, nachdem die [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Methode asynchron abgeschlossen wurde. Die Medien Sitzung löst dieses Ereignis aus, nachdem die Topologie in eine vollständige Topologie aufgelöst und die Topologie zur Wiedergabe in die Warteschlange eingereiht wurde.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| VT \_ leer<br/>   | Keine Ereignisdaten.<br/> <br/>                                                                    |
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Schnittstelle der vollständigen Topologie.<br/> <br/> |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird der [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Zeiger von einem mesessiontopologyset-Ereignis abgerufen.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




