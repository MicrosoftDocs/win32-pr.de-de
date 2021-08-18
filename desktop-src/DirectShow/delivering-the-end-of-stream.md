---
description: Bereitstellen des Endes von Stream
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Bereitstellen des Endes von Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebae0fe3238f32f630c0a2ecd0787f6bd9b75a9aed6342e202f187d3fe8dac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831350"
---
# <a name="delivering-the-end-of-stream"></a>Bereitstellen des Endes von Stream

Wenn der Eingabepin eine End-of-Stream-Benachrichtigung empfängt, wird der Aufruf downstream weitergegeben. Alle Downstreamfilter, die Daten von diesem Eingabepin empfangen, sollten ebenfalls die End-of-Stream-Benachrichtigung erhalten. Nehmen Sie erneut die Streamingsperre und nicht die Filtersperre. Wenn der Filter ausstehende Daten enthält, die noch nicht übermittelt wurden, sollte der Filter ihn jetzt übermitteln, bevor er die Benachrichtigung zum Ende des Streams sendet. Nach dem Ende des Streams sollten keine Daten gesendet werden.


```C++
HRESULT CMyInputPin::EndOfStream()
{
    CAutoLock lock_it(&m_csReceive);

    /* If the pin has not delivered all of the data in the stream 
       (based on what it received previously), do so now.  */

    // Propagate EndOfStream call downstream, via your output pin(s).
    for (each output pin)
    {    
        hr = pOutputPin->DeliverEndOfStream();
    }
    return S_OK;
}
```



Die [**CBaseOutputPin::D eliverEndOfStream-Methode**](cbaseoutputpin-deliverendofstream.md) ruft [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) auf dem Downstreameingabepin auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Threads und kritische Abschnitte](threads-and-critical-sections.md)
</dt> </dl>

 

 



