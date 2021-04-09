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
# <a name="delivering-the-end-of-stream"></a><span data-ttu-id="d48a5-103">Über das Ende des Streams</span><span class="sxs-lookup"><span data-stu-id="d48a5-103">Delivering the End of Stream</span></span>

<span data-ttu-id="d48a5-104">Wenn die Eingabe-PIN eine Benachrichtigung über das Ende des Datenstroms empfängt, wird der-Rückruf weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="d48a5-104">When the input pin receives an end-of-stream notification, it propagates the call downstream.</span></span> <span data-ttu-id="d48a5-105">Alle Downstream-Filter, die Daten von dieser Eingabe-PIN empfangen, sollten auch die Datenstrom-Benachrichtigung erhalten.</span><span class="sxs-lookup"><span data-stu-id="d48a5-105">Any downstream filters that receive data from this input pin should also get the end-of-stream notification.</span></span> <span data-ttu-id="d48a5-106">Nehmen Sie erneut die streamingsperre und nicht die Filter Sperre vor.</span><span class="sxs-lookup"><span data-stu-id="d48a5-106">Again, take the streaming lock and not the filter lock.</span></span> <span data-ttu-id="d48a5-107">Wenn der Filter ausstehende Daten aufweist, die noch nicht übermittelt wurden, sollte der Filter ihn jetzt übermitteln, bevor er die Benachrichtigung über das Ende des Datenstroms sendet.</span><span class="sxs-lookup"><span data-stu-id="d48a5-107">If the filter has pending data that was not yet delivered, the filter should deliver it now, before it sends the end-of-stream notification.</span></span> <span data-ttu-id="d48a5-108">Nach dem Ende des Streams sollten keine Daten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d48a5-108">It should not send any data after the end of the stream.</span></span>


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



<span data-ttu-id="d48a5-109">Die [**cbaseoutputpin::D eliverendof Stream**](cbaseoutputpin-deliverendofstream.md) -Methode ruft [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) für die downstreameingabepin auf.</span><span class="sxs-lookup"><span data-stu-id="d48a5-109">The [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method calls [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d48a5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d48a5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d48a5-111">Threads und kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="d48a5-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



