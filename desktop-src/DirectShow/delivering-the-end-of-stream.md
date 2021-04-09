---
description: Über das Ende des Streams
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Über das Ende des Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bd80d186bd62e6360fa1600f4ba970281315aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860037"
---
# <a name="delivering-the-end-of-stream"></a>Über das Ende des Streams

Wenn die Eingabe-PIN eine Benachrichtigung über das Ende des Datenstroms empfängt, wird der-Rückruf weitergegeben. Alle Downstream-Filter, die Daten von dieser Eingabe-PIN empfangen, sollten auch die Datenstrom-Benachrichtigung erhalten. Nehmen Sie erneut die streamingsperre und nicht die Filter Sperre vor. Wenn der Filter ausstehende Daten aufweist, die noch nicht übermittelt wurden, sollte der Filter ihn jetzt übermitteln, bevor er die Benachrichtigung über das Ende des Datenstroms sendet. Nach dem Ende des Streams sollten keine Daten gesendet werden.


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



Die [**cbaseoutputpin::D eliverendof Stream**](cbaseoutputpin-deliverendofstream.md) -Methode ruft [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) für die downstreameingabepin auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Threads und kritische Abschnitte](threads-and-critical-sections.md)
</dt> </dl>

 

 



