---
description: Abrufen von Ereignissen
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Abrufen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1132b2b0140c86c2be1e7916e8d1de28e231b2eca50596714aaa82346aaf83eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072724"
---
# <a name="retrieving-events"></a>Abrufen von Ereignissen

Der Filter Graph Manager macht drei Schnittstellen verfügbar, die Ereignisbenachrichtigungen unterstützen.

-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) enthält die -Methode für Filter zum Veröffentlichen von Ereignissen.
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) enthält Methoden zum Abrufen von Ereignissen durch Anwendungen.
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) erbt von und erweitert die [**IMediaEvent-Schnittstelle.**](/windows/desktop/api/Control/nn-control-imediaevent)

Filtert Ereignisbenachrichtigungen, indem die [**IMediaEventSink::Notify-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) im Filter Graph Manager aufgerufen wird. Eine Ereignisbenachrichtigung besteht aus einem Ereigniscode, der den Ereignistyp definiert, und zwei Parametern, die zusätzliche Informationen liefern. Abhängig vom Ereigniscode können die Parameter Zeiger, Rückgabecodes, Verweiszeiten oder andere Informationen enthalten. Eine vollständige Liste der Ereigniscodes und Parameter finden Sie unter [Ereignisbenachrichtigungscodes.](event-notification-codes.md)

Um ein Ereignis aus der Warteschlange abzurufen, ruft die Anwendung die [**IMediaEvent::GetEvent-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) im Filter Graph Manager auf. Diese Methode blockiert, bis ein zurückzugebendes Ereignis vorhanden ist oder bis eine angegebene Zeit verstrichen ist. Wenn ein Ereignis in der Warteschlange vorhanden ist, gibt die Methode mit dem Ereigniscode und den beiden Ereignisparametern zurück. Nach dem Aufruf von **GetEvent** sollte eine Anwendung immer die [**IMediaEvent::FreeEventParams-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) aufrufen, um alle Ressourcen freizugeben, die den Ereignisparametern zugeordnet sind. Ein Parameter kann beispielsweise ein **BSTR-Wert** sein, der vom Filterdiagramm zugeordnet wurde.

Im folgenden Codebeispiel wird beschrieben, wie Ereignisse aus der Warteschlange abgerufen werden.


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



Um die Standardbehandlung des Filter Graph-Managers für ein Ereignis zu überschreiben, rufen Sie die [**IMediaEvent::CancelDefaultHandling-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) mit dem Ereigniscode als Parameter auf. Sie können die Standardbehandlung durch Aufrufen der [**IMediaEvent::RestoreDefaultHandling-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) wiederherstellen. Wenn das Filterdiagramm keine Standardbehandlung für den angegebenen Ereigniscode ausführt, hat der Aufruf dieser Methoden keine Auswirkungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



