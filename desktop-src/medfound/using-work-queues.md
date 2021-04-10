---
description: In diesem Thema wird beschrieben, wie Sie Arbeits Warteschlangen in Microsoft Media Foundation verwenden.
ms.assetid: 6be05df7-e8ff-4110-8f73-a62eb31fd414
title: Verwenden von Arbeits Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb41b830742ca871d44cadac9bd26a9967aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215003"
---
# <a name="using-work-queues"></a>Verwenden von Arbeits Warteschlangen

In diesem Thema wird beschrieben, wie Sie Arbeits Warteschlangen in Microsoft Media Foundation verwenden.

-   [Verwenden von Arbeits Warteschlangen](#using-work-queues)
-   [Herunterfahren von Arbeits Warteschlangen](#shutting-down-work-queues)
-   [Verwenden geplanter Arbeitselemente](#using-scheduled-work-items)
-   [Verwenden regelmäßiger Rückrufe](#using-periodic-callbacks)
-   [Zugehörige Themen](#related-topics)

## <a name="using-work-queues"></a>Verwenden von Arbeits Warteschlangen

Eine Arbeits Warteschlange ist eine effiziente Möglichkeit, um asynchrone Vorgänge in einem anderen Thread auszuführen. Konzeptionell werden Arbeitselemente in die Warteschlange eingefügt, und die Warteschlange verfügt über einen Thread, der jedes Element aus der Warteschlange abruft und sendet. Arbeitselemente werden mithilfe der [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle als Rückrufe implementiert.

Media Foundation erstellt mehrere standardmäßige Arbeits Warteschlangen, die als *Platform Work Queues* bezeichnet werden. Anwendungen können auch eigene Arbeits Warteschlangen erstellen, die als *private Arbeits Warteschlangen* bezeichnet werden. Eine Liste der Platt Form Arbeitswarteschlangen finden Sie unter Bezeichner für [Arbeits](work-queue-identifiers.md)Warteschlangen. Um eine private Arbeits Warteschlange zu erstellen, rufen Sie [**mfbelegcateworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)auf. Diese Funktion gibt einen Bezeichner für die neue Arbeits Warteschlange zurück. Um ein Element in die Warteschlange einzufügen, nennen Sie [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) oder [**mfputworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). In beiden Fällen müssen Sie eine Rückruf Schnittstelle angeben.

-   [**Mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) nimmt einen Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle sowie ein optionales Zustands Objekt an, das **IUnknown** implementiert. Dabei handelt es sich um dieselben Parameter, die in asynchronen Methoden verwendet werden, wie im Thema [asynchrone Rückruf Methoden](asynchronous-callback-methods.md)beschrieben. Intern erstellt diese Funktion ein asynchrones Ergebnis Objekt, das an die [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode des Rückrufs übermittelt wird.
-   [**Mfputworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) übernimmt einen Zeiger auf die [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle. Diese Schnittstelle stellt ein asynchrones Ergebnis Objekt dar. Erstellen Sie dieses Objekt, indem Sie [**mfcreateasyncresult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) aufrufen und die Rückruf Schnittstelle und optional ein Zustands Objekt angeben.

In beiden Fällen ruft der Arbeits Warteschlangen Thread Ihre [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode auf. Verwenden Sie die Methode " **aufrufen** ", um das Arbeits Element auszuführen.

Wenn mehr als ein Thread oder eine Komponente dieselbe Arbeits Warteschlange gemeinsam verwendet, können Sie [**mflockworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mflockworkqueue) zum Sperren der Arbeits Warteschlange anrufen, wodurch die Plattform nicht freigegeben werden kann. Sie müssen für jeden [**mfbelegcateworkqueue-mfbelegungsqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) -Befehl oder **mflockworkqueue**-Befehl einmal [**mfunlockworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue) abrufen, um die Arbeits Warteschlange freizugeben. Wenn Sie z. b. eine neue Arbeits Warteschlange erstellen und diese dann einmal sperren, müssen Sie **mfunlockworkqueue** zweimal (einmal für den **mfbelegcateworkqueue** -Aufrufvorgang und einmal für den **mflockworkqueue**-Aufrufvorgang) aufzurufen.

Der folgende Code zeigt, wie Sie eine neue Arbeits Warteschlange erstellen, eine Arbeitsaufgabe in die Warteschlange stellen und die Arbeits Warteschlange freigeben.

Weitere Informationen zu Arbeits Warteschlangen in Windows 8 finden Sie unter [Verbesserungen der Arbeits Warteschlange und Threading](media-foundation-work-queue-and-threading-improvements.md)


```C++
DWORD idWorkQueue = 0;
HRESULT hr = S_OK;

// Create a new work queue.
hr = MFAllocateWorkQueue(&idWorkQueue);

// Put an item on the queue.
if (SUCCEEDED(hr))
{
    hr = MFPutWorkItem(idWorkQueue, pCallback, NULL);
}

// Wait for the callback to be invoked.
if (SUCCEEDED(hr))
{
    WaitForSingleObject(hEvent, INFINITE);
}

// Release the work queue.
if (SUCCEEDED(hr))
{
    hr = MFUnlockWorkQueue(idWorkQueue);
}
```



In diesem Beispiel wird davon ausgegangen, dass *pCallback* ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle der Anwendung ist. Außerdem wird davon ausgegangen, dass der Rückruf das *hevent* -Ereignis handle festlegt. Der Code wartet, bis dieses Ereignis festgelegt wird, bevor [**mfunlockworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue)aufgerufen wird.

Arbeitswarteschlangen-Threads werden immer im Prozess des Aufrufers erstellt. Innerhalb der einzelnen Arbeits Warteschlangen werden die Rückrufe serialisiert. Wenn Sie [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) zweimal mit derselben Arbeits Warteschlange aufrufen, wird der zweite Rückruf erst aufgerufen, wenn der erste Rückruf zurückgegeben wurde.

## <a name="shutting-down-work-queues"></a>Herunterfahren von Arbeits Warteschlangen

Geben Sie vor dem Aufrufen von [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)alle Ressourcen frei, die von Arbeitsthreads verwendet werden. Um diesen Prozess zu synchronisieren, können Sie die Media Foundation Plattform sperren, wodurch verhindert wird, dass die **mfshutdown** -Funktion alle Arbeitswarteschlangen-Threads schließt. Wenn **mfshutdown** aufgerufen wird, während die Plattform gesperrt ist, wartet **mfshutdown** einige hundert Millisekunden, bis die Plattform entsperrt wird. Wenn Sie nicht innerhalb dieser Zeit entsperrt wird, schließt **MF Shutdown** die Arbeitswarteschlangen-Threads.

Die Standard Implementierung von [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) sperrt die Media Foundation Plattform automatisch, wenn das Ergebnis Objekt erstellt wird. Das Freigeben der-Schnittstelle entsperrt die-Plattform. Daher müssen Sie die Plattform fast niemals direkt sperren. Wenn Sie jedoch eine eigene benutzerdefinierte Implementierung von **imfasynkresult** schreiben, sollten Sie die Plattform manuell sperren und entsperren. Um die Plattform zu sperren, nennen Sie [**mflockplatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform). Um die Plattform zu entsperren, nennen Sie [**mfunlockplatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform). Ein Beispiel finden Sie unter [benutzerdefinierte asynchrone Ergebnis Objekte](custom-asynchronous-result-objects.md).

Nachdem Sie [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)aufgerufen haben, müssen Sie sicherstellen, dass die Plattform innerhalb des 5-Sekunden-Timeout Zeitraums entsperrt wird. Veröffentlichen Sie dazu alle [**imfasyncresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Zeiger, und rufen Sie [**mfunlockplatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) auf, wenn Sie die Plattform manuell gesperrt haben. Stellen Sie sicher, dass alle Ressourcen freigegeben werden, die von Arbeitswarteschlangen-Threads verwendet werden, oder die Anwendung kann Speicher Verluste.

Wenn Ihre Anwendung in der Regel vor dem Aufruf von [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)alle Media Foundation Objekte herunterfährt und freigibt, müssen Sie sich keine Gedanken über das Sperren machen. Mit dem Sperrmechanismus können Arbeitswarteschlangen-Threads einfach ordnungsgemäß beendet werden, nachdem Sie **mfshutdown** aufgerufen haben.

## <a name="using-scheduled-work-items"></a>Verwenden geplanter Arbeitselemente

Sie können einen Rückruf so planen, dass er nach einer festgelegten Zeitspanne durch Aufrufen von [**mfscheduleworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) oder [**mfscheduleworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex)auftritt.

-   [**Mfscheduleworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) nimmt einen Zeiger auf Ihren Rückruf, ein optionales Zustands Objekt und ein Timeout Intervall an.
-   [**Mfscheduleworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex) übernimmt einen Zeiger auf ein asynchrones Ergebnis Objekt und einen Timeout Wert.

Geben Sie das Timeout als negativen Wert in Millisekunden an. Wenn Sie z. b. einen Rückruf innerhalb von 5 Sekunden planen möchten, verwenden Sie den Wert − 5000. Beide Funktionen geben einen **mfworkitem- \_ Schlüssel** Wert zurück, den Sie verwenden können, um den Rückruf abzubrechen, indem Sie ihn an die [**mfcancelworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfcancelworkitem) -Funktion übergeben.

Für geplante Arbeitsaufgaben wird immer die Arbeits Warteschlange "mfasync- \_ Rückruf Warteschlange" verwendet \_ \_ .

## <a name="using-periodic-callbacks"></a>Verwenden regelmäßiger Rückrufe

Die [**mfaddperiodiccallback**](/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback) -Funktion plant, dass ein Rückruf regelmäßig aufgerufen wird, bis Sie ihn abbrechen. Das Rückruf Intervall ist korrigiert. Anwendungen können diese nicht ändern. Um das exakte Intervall zu ermitteln, müssen Sie [**mfgettimerperiodicity**](/windows/desktop/api/mfapi/nf-mfapi-mfgettimerperiodicity)aufrufen. Das Intervall liegt in der Reihenfolge von 10 Millisekunden. diese Funktion ist daher für Situationen gedacht, in denen Sie einen häufigen "Tick" benötigen, z. b. die Implementierung einer Präsentations Uhr. Wenn Sie planen möchten, dass ein Vorgang seltener auftritt, verwenden Sie ein geplantes Arbeits Element, wie zuvor beschrieben.

Im Gegensatz zu den anderen in diesem Thema beschriebenen Rückrufe verwendet der periodische Rückruf nicht die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle. Stattdessen wird ein Funktionszeiger verwendet. Weitere Informationen finden Sie unter [**MF-Rückruf**](/windows/win32/api/mfapi/nc-mfapi-mfperiodiccallback).

Um den periodischen Rückruf abzubrechen, rufen Sie [**mfremoveperiodiccallback**](/windows/desktop/api/mfapi/nf-mfapi-mfremoveperiodiccallback)auf.

Periodische Rückrufe verwenden die mfasync-Rückruf Warteschlange für die Zeit Geber \_ \_ \_ Plattform.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeits Warteschlangen](work-queues.md)
</dt> <dt>

[**Mfasynkresult**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult)
</dt> <dt>

[Arbeits Warteschlangen und Threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 
