---
description: Abrufen von Ereignissen
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Abrufen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d23cf4f8060c15db564e718ba3a2fa4a660022
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392335"
---
# <a name="retrieving-events"></a>Abrufen von Ereignissen

Der Filter Graph-Manager macht drei Schnittstellen verfügbar, die die Ereignis Benachrichtigung unterstützen.

-   [**Imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) enthält die-Methode für Filter zum Veröffentlichen von Ereignissen.
-   [**Imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) enthält Methoden, mit denen Anwendungen Ereignisse abrufen können.
-   [**Imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) erbt von und erweitert die [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) -Schnittstelle.

Filtert nach Ereignis Benachrichtigungen, indem die [**imediaeventsink:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) -Methode für den Filter Graph-Manager aufgerufen wird. Eine Ereignis Benachrichtigung besteht aus einem Ereignis Code, der den Ereignistyp definiert, und zwei Parametern, die zusätzliche Informationen enthalten. Abhängig vom Ereignis Code können die Parameter Zeiger, Rückgabecodes, Verweis Zeiten oder andere Informationen enthalten. Eine umfassende Liste von Ereignis Codes und Parametern finden Sie unter [Ereignis Benachrichtigungs Codes](event-notification-codes.md).

Um ein Ereignis aus der Warteschlange abzurufen, ruft die Anwendung die [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) -Methode für den Filter Graph-Manager auf. Diese Methode wird blockiert, bis ein Ereignis zurückgegeben werden kann oder bis eine angegebene Zeit verstrichen ist. Wenn ein Ereignis in der Warteschlange vorhanden ist, gibt die Methode mit dem Ereignis Code und den beiden Ereignis Parametern zurück. Nach dem Aufruf von **GetEvent** sollte eine Anwendung immer die Methode [**imediaevent:: freeventparser**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) aufrufen, um alle Ressourcen freizugeben, die den Ereignis Parametern zugeordnet sind. Ein Parameter kann z. b. ein **BSTR** -Wert sein, der vom Filter Diagramm zugeordnet wurde.

Im folgenden Codebeispiel wird erläutert, wie Ereignisse aus der Warteschlange abgerufen werden.


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



Um die Standardbehandlung des Filter Graph-Managers für ein Ereignis zu überschreiben, rufen Sie die [**imediaevent:: canceldefaulthandelt**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) -Methode mit dem Ereignis Code als Parameter auf. Sie können die Standardbehandlung wiederherstellen, indem Sie die [**imediaevent:: restoredefaulthandelt**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) -Methode aufrufen. Wenn das Filter Diagramm keine Standardbehandlung für den angegebenen Ereignis Code ausführt, hat das Aufrufen dieser Methoden keine Auswirkung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



