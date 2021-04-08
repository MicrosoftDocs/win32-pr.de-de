---
description: In diesem Thema werden die Verbesserungen in Windows 8 für Arbeits Warteschlangen und Threading in der Microsoft Media Foundation Plattform beschrieben.
ms.assetid: 9E2A1D94-BF82-488E-8297-D524683ABE17
title: Arbeits Warteschlangen und Threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b307cb00316696e075e9e9cc2a138e98e149be
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050714"
---
# <a name="work-queue-and-threading-improvements"></a>Arbeits Warteschlangen und Threading

In diesem Thema werden die Verbesserungen in Windows 8 für Arbeits Warteschlangen und Threading in der Microsoft Media Foundation Plattform beschrieben.

-   [Windows 7-Verhalten](#windows-7-behavior)
    -   [Arbeits Warteschlangen](#work-queues)
    -   [MMCSS-Unterstützung](#mmcss-support)
    -   [Imfrealtimeclient](#imfrealtimeclientex)
-   [Verbesserte Windows 8](#windows-8-improvements)
    -   [Multithread-Arbeits Warteschlangen](#multithreaded-work-queues)
    -   [Arbeits Warteschlangen für freigegebene Aufgaben](#shared-task-work-queues)
    -   [Warteschlange](#wait-queue)
    -   [Erweiterungen der MMCSS-Unterstützung](#enhancements-to-mmcss-support)
    -   [Imfrealtimecliumtex](#imfrealtimeclientex)
    -   [Topologiebranches](#topology-branches)
-   [Empfehlungen](#recommendations)
-   [Zusammenfassung](#summary)
-   [Zugehörige Themen](#related-topics)

## <a name="windows-7-behavior"></a>Windows 7-Verhalten

In diesem Abschnitt wird das Verhalten Media Foundation Arbeits Warteschlangen in Windows 7 zusammengefasst.

### <a name="work-queues"></a>Arbeits Warteschlangen

Die Media Foundation Plattform erstellt mehrere standardmäßige Arbeits Warteschlangen. Nur zwei werden als für die allgemeine Anwendungs Verwendung dokumentiert:

-   **mfasync- \_ Rückruf \_ Warteschlangen \_ Standard**
-   **lange Funktion der mfasync- \_ Rückruf \_ Warteschlange \_ \_**

Eine Anwendung oder Komponente kann neue Arbeits Warteschlangen zuweisen, indem Sie [**mfallocateworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) oder [**mfallocateworkqueueex**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex)aufrufen. Die Funktion " **MF belegcateworkqueueex** " definiert zwei Typen von Arbeits Warteschlangen:

-   **MF \_ Standard \_ Arbeits Warteschlange** erstellt eine Arbeits Warteschlange ohne Nachrichten Schleife.
-   **MF \_ Fenster \_ Arbeits Warteschlange** erstellt eine Arbeits Warteschlange mit einer Nachrichten Schleife.

Um ein Arbeits Element in die Warteschlange zu stellen, nennen Sie [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) oder [**mfputworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). Die Plattform führt das Arbeits Element durch Aufrufen der vom Aufrufer bereitgestellten Implementierung von [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)aus. In Windows 7 und früheren Versionen erstellt die Plattform einen Thread pro Arbeits Warteschlange.

### <a name="mmcss-support"></a>MMCSS-Unterstützung

Der [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) verwaltet Thread Prioritäten, sodass Multimediaanwendungen regelmäßige Slices der CPU-Zeit erhalten, ohne dass CPU-Ressourcen Anwendungen mit niedrigerer Priorität verweigert werden. MMCSS definiert eine Reihe von *Tasks* , die über unterschiedliche CPU-Auslastungs Profile verfügen. Wenn ein Thread einem MMCSS-Task Beitritt, legt MMCSS die Priorität des Threads auf der Grundlage verschiedener Faktoren fest:

-   Die Basis Priorität der Aufgabe, die in der Registrierung festgelegt wird.
-   Die relative Thread Priorität, die zur Laufzeit durch Aufrufen von [**avsetmmthreadpriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority)festgelegt wird.
-   Verschiedene Lauf Zeitmerkmale, wie z. b. ob die Anwendung im Vordergrund steht und wie viel CPU-Zeit von den Threads in den einzelnen MMCSS-Klassen verbraucht wird.

Eine Anwendung kann eine Arbeits Warteschlange mit MMCSS registrieren, indem [**mfbeginregisterworkqueuewithmmcss**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss)aufgerufen wird. Diese Funktion nimmt eine Arbeits Warteschlangen-ID, eine MMCSS-Klasse (Taskname) und den MMCSS-Task Bezeichner an. Intern wird [**avsetmmthreadcharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) mit dem Aufgaben Namen und der Task-ID aufgerufen. Nachdem eine Arbeits Warteschlange mit MMCSS registriert wurde, können Sie die Klasse und die Task-ID abrufen, indem Sie [**mfgetworkqueuemmcssclass**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcssclass) und [**mfgetworkqueuemmcsstaskid**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsstaskid)aufrufen.

Die [Medien Sitzung](media-session.md) bietet über die [**imfworkqueueservices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices) -Schnittstelle einen etwas höheren Zugriff auf diese APIs. Diese Schnittstelle stellt zwei primäre Methoden bereit:

| Methode                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Beginregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss)   | Registriert eine Arbeits Warteschlange bei einem MMCSS-Task. Bei dieser Methode handelt es sich im Grunde um einen schmalen Wrapper um [**mfbeginregisterworkqueuewithmmcss**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss), aber Sie können den Wert " **mfasync \_ Callback \_ Queue \_ all** " übergeben, um alle Platt Form Arbeitswarteschlangen gleichzeitig zu registrieren. |
| [**Beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) | Registriert einen Branch der Topologie bei einer Arbeits Warteschlange.                                                                                                                                                                                                                                         |



 

Gehen Sie folgendermaßen vor, um eine topologieverzweigung zu registrieren.

1.  Legen Sie das Attribut für die [MF- \_ toponode- \_ workqueue- \_ ID](mf-toponode-workqueue-id-attribute.md) auf dem Quellknoten für den Branch fest. Verwenden Sie einen beliebigen von der Anwendung definierten Wert.
2.  Legen Sie optional die **\_ \_ \_ MMCSS- \_ Klasse "MF toponode workqueue** " fest, um die Arbeits Warteschlange einem MMCSS-Task beizutreten.
3.  Aufrufen von [**beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) in der aufgelösten Topologie.

Die Medien Sitzung ordnet eine neue Arbeits Warteschlange für jeden eindeutigen Wert der [MF- \_ toponode- \_ workqueue- \_ ID](mf-toponode-workqueue-id-attribute.md)zu. Für jeden topologiebranch werden asynchrone Pipeline Vorgänge in der Arbeits Warteschlange durchgeführt, die der Verzweigung zugewiesen ist.

### <a name="imfrealtimeclient"></a>Imfrealtimeclient

Die [**imfrealtimeclient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient) -Schnittstelle ist für Pipeline Komponenten vorgesehen, die entweder eigene Threads erstellen oder Arbeits Warteschlangen für asynchrone Vorgänge verwenden. Die Medien Sitzung verwendet diese Schnittstelle, um die Pipeline Komponente über das korrekte Verhalten wie folgt zu benachrichtigen:

-   Wenn die Pipeline Komponente einen Arbeits Thread erstellt, benachrichtigt die [**imfrealtimeclient:: registerthreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads) -Methode die Komponente, welcher MMCSS-Klasse beitreten soll.
-   Wenn die Pipeline Komponente eine Arbeits Warteschlange verwendet, teilt die [**imfrealtimeclient:: setworkqueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue) -Methode der Komponente mit, welche Arbeits Warteschlange verwendet werden soll.

In der Regel verwendet eine Pipeline Komponente entweder einen Thread oder eine Arbeits Warteschlange, um asynchrone Aufgaben auszuführen, aber nicht beides.

## <a name="windows-8-improvements"></a>Verbesserte Windows 8

### <a name="multithreaded-work-queues"></a>Multithread-Arbeits Warteschlangen

In Windows 8 unterstützt Media Foundation einen neuen Arbeits Aufgabentyp, der als *Multithread-Warteschlange* bezeichnet wird. Eine multithreadwarteschlange verwendet einen System Thread Pool, um Arbeitselemente zu verteilen. Die Multithread-Warteschlange skaliert besser als die vorherigen Single Thread-Warteschlangen. Beispiel:

-   Mehrere Komponenten können eine multithreadwarteschlange freigeben, ohne eine andere zu blockieren, sodass weniger Threads erstellt werden müssen.

-   Arbeitselemente werden optimiert, um Kontextwechsel zu vermeiden, wenn ein Ereignis bereits festgelegt ist. Dies ist effizienter als das Erstellen eigener Threads, um auf Ereignisse zu warten.

Bei der Verwendung von [**imfrealtimeclientex**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)sollten Anwendungen das Einrichten von Threads vermeiden und stattdessen die Arbeits Warteschlangen verwenden. Um dies zu erreichen, sollten die Anwendungen [**setworkqueueex**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex) implementieren und nicht [**registerthreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) und [**unregisterthreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads)verwenden.

Wenn die Media Foundation Plattform initialisiert wird, erstellt Sie eine Multithread-Warteschlange mit dem Bezeichner **mfasync- \_ Rückruf \_ Warteschlange \_ Multithread**.

Arbeitselemente werden von der Multithread-Warteschlange nicht serialisiert. Wenn ein Thread aus dem Thread Pool verfügbar wird, wird das nächste Arbeits Element in der Warteschlange weitergeleitet. Der Aufrufer muss sicherstellen, dass die Arbeit richtig serialisiert wird. Um dies zu vereinfachen, Media Foundation eine *serielle Arbeits Warteschlange* definiert. Eine serielle Warteschlange schließt eine andere Arbeits Warteschlange ein Das nächste Element in der Warteschlange wird erst gesendet, wenn das vorherige Element abgeschlossen ist.

Der folgende Code erstellt eine warteschlangenwarteschlange über die Multithread-Multithread-Warteschlange.


```C++
DWORD workQueueID;
hr = MFAllocateSerialWorkQueue(MFASYNC_CALLBACK_QUEUE_MULTITHREADED, &workQueueID); 
```



Mehrere serielle Warteschlangen können eine Multithread-Warteschlange einschließen. Die seriellen Warteschlangen verwenden dann denselben Thread Pool, und die serialisierte Ausführung wird innerhalb jeder Warteschlange erzwungen.

Die Standard Arbeits Warteschlangen, die vor Windows 8 vorhanden waren, werden nun als serielle Arbeits Warteschlangen implementiert, die die Multithread-Multithread-Warteschlange Durch diese Änderung wird die Abwärtskompatibilität beibehalten.

### <a name="shared-task-work-queues"></a>Arbeits Warteschlangen für freigegebene Aufgaben

Wenn Sie mit dem Kernel Planer ordnungsgemäß arbeiten möchten, sollte für jede von Ihnen verwendete MMCSS-Aufgabe eine Multithread-Arbeits Warteschlange vorhanden sein. Die Media Foundation Plattform ordnet diese nach Bedarf zu, bis zu einer pro MMCSS-Aufgabe pro Prozess. Um die freigegebene Arbeits Warteschlange für eine bestimmte MMCSS-Aufgabe abzurufen, nennen Sie [**mflocksharedworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) , und geben Sie den Aufgaben Namen an. Die-Funktion sucht den Aufgaben Namen in einer Tabelle. Wenn eine Arbeits Warteschlange für diese Aufgabe nicht bereits vorhanden ist, ordnet die Funktion eine neue Master-Arbeits Warteschlange zu und fügt Sie sofort mit der MMCSS-Aufgabe an. Wenn bereits eine Arbeits Warteschlange für diese Aufgabe vorhanden ist, gibt die Funktion den Bezeichner der vorhandenen Arbeits Warteschlange zurück.

### <a name="wait-queue"></a>Warteschlange

Die *Warteschlange* ist eine besondere Plattform-Arbeits Warteschlange, die darauf wartet, dass Ereignisse signalisiert werden. Wenn eine Komponente auf die Signalisierung eines Ereignisses warten muss, kann Sie die Warteschlange verwenden, anstatt einen Arbeits Thread zu erstellen, der auf das Ereignis wartet.

Um die Warteschlange zu verwenden, nennen Sie [**mfputwaitingworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem). Zu den Parametern gehören das Ereignis Handle und ein [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Zeiger. Wenn das Ereignis signalisiert wird, ruft die Warteschlange ihren Rückruf auf. Es gibt eine Warteschlange für eine einzelne Plattform. Anwendungen können keine eigenen Warteschlangen für Warteschlangen erstellen.

### <a name="enhancements-to-mmcss-support"></a>Erweiterungen der MMCSS-Unterstützung

Die folgenden neuen Media Foundation-Plattformfunktionen beziehen sich auf MMCSS.



| Funktion                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex) | Registriert eine Arbeits Warteschlange mit MMCSS. Diese Funktion enthält einen Parameter zum Angeben der relativen Thread Priorität. Intern wird dieser Wert in einen-Aufrufen von [**avsetmmthreadpriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority)übersetzt.                                                                                                                                                                               |
| [**MF getworkqueuemmcsspriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)                 | Fragt die Priorität einer Arbeits Warteschlange ab.                                                                                                                                                                                                                                                                                                                                                                 |
| [**MF registerplatformwithmmcss**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)                 | Registriert alle Platt Form Arbeitswarteschlangen bei einer MMCSS-Aufgabe. Diese Funktion ähnelt der [**imfworkqueueservices:: beginregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) -Methode, kann aber ohne Erstellen einer Instanz der Medien Sitzung verwendet werden. Darüber hinaus enthält die-Funktion einen-Parameter, um die Basis Thread Priorität anzugeben. |



 

Anwendungen, die die Medien Sitzung verwenden, sollten für den audiorenderingbranch das Attribut " [MF \_ toponode \_ workqueue" der \_ MMCSS- \_ Klasse](mf-toponode-workqueue-mmcss-class-attribute.md) auf "Audiodaten" festlegen. Legen Sie das-Attribut für den videorenderingbranch auf "Wiedergabe" fest.

### <a name="imfrealtimeclientex"></a>Imfrealtimecliumtex

Die [**imfrealtimecliumtex**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex) -Schnittstelle zum Ersetzen von imfrealtimeclient für Pipeline Komponenten, die asynchrone Vorgänge ausführen.



| Methode                                                             | BESCHREIBUNG                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Registerthreadsex**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) | Benachrichtigt die Komponente, ihre Threads bei MMCSS zu registrieren. Diese Methode entspricht [**imfrealtimeclient:: registerthreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads), fügt aber einen Parameter für die Basis Thread Priorität hinzu. |
| [**Setworkqueueex**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex)       | Benachrichtigt die Komponente, eine bestimmte Arbeits Warteschlange zu verwenden. Diese Methode entspricht [**imfreadtimeclient:: setworkqueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue), fügt aber einen Parameter für die Arbeits Element Priorität hinzu.               |
| [**Unregisterthreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads) | Benachrichtigt die Komponente, dass die Registrierung Ihrer Threads bei MMCSS aufgehoben werden soll. Diese Methode ist identisch mit der [**imfrealtimeclient:: unregisterthreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-unregisterthreads) -Methode.                                       |



 

Pipeline Komponenten sollten aus den folgenden Gründen Arbeits Warteschlangen verwenden und keine Arbeitsthreads erstellen:

-   Die Skalierung von Arbeits Warteschlangen ist besser, da Sie die Betriebssystem-Thread Pools
-   Die Plattform behandelt die Details zum Registrieren von Arbeits Warteschlangen mit MMCSS.
-   Ein Arbeits Thread kann problemlos einen Deadlock verursachen, der schwer zu Debuggen ist.

Sie sollten auch die Arbeits Warteschlange des Serialisierungsprogramms verwenden, wenn Sie Ihre asynchronen Vorgänge serialisieren müssen.

### <a name="topology-branches"></a>Topologiebranches

Wenn das Attribut " [MF \_ toponode \_ workqueue" der \_ MMCSS- \_ Klasse](mf-toponode-workqueue-mmcss-class-attribute.md) eine topologieverzweigung mit MMCSS registriert, verwendet die Medien Sitzung in Windows 8 die freigegebenen MT-Arbeits Warteschlangen. In früheren Versionen von Windows hat die Medien Sitzung eine neue Arbeits Warteschlange zugeordnet.

Zwei neue Attribute werden für die Registrierung einer topologieverzweigung mit MMCSS definiert.



| Attribut                                                                            | BESCHREIBUNG                         |
|--------------------------------------------------------------------------------------|-------------------------------------|
| [MMCSS-Priorität der MF- \_ toponode- \_ workqueue \_ \_](mf-toponode-workqueue-mmcss-priority.md) | Gibt die Basis Thread Priorität an. |
| [Element Priorität für MF- \_ toponode- \_ workqueue \_ \_](mf-toponode-workqueue-item-priority.md)   | Gibt die Arbeits Element Priorität an.   |



 

## <a name="recommendations"></a>Empfehlungen

-   Anwendungen, die die Medien Sitzung verwenden, sollten die [MF- \_ toponode- \_ workqueue- \_ MMCSS- \_ Klasse](mf-toponode-workqueue-mmcss-class-attribute.md) für den audiorenderingbranch auf "Audiodatei" festlegen und für den videorenderingbranch "Wiedergabe"
-   Anwendungen, die die Medien Sitzung verwenden, sollten [**imfworkqueueservices:: beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) in der Topologie aufrufen.
-   Für Pipeline Komponenten werden Arbeits Warteschlangen anstelle von Arbeitsthreads empfohlen. Wenn die Komponente entweder Arbeits Warteschlangen oder Arbeitsthreads verwendet, implementieren Sie [**imfrealtimeclientex**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex).
-   Erstellen Sie keine privaten Arbeits Warteschlangen, da dadurch der Zweck der Platt Form Arbeitswarteschlangen nicht mehr möglich ist. Verwenden Sie die Multithread-Multithread-Warteschlange oder eine serielle Warteschlange, die die Multithread-Multithread-Warteschlange
-   Wenn Sie asynchrone Vorgänge serialisieren müssen, verwenden Sie eine serielle Warteschlange.

## <a name="summary"></a>Zusammenfassung

Die folgenden Media Foundation Plattform-APIs, die sich auf Threads und Arbeits Warteschlangen beziehen, sind neu in Windows 8.

-   [Element Priorität für MF- \_ toponode- \_ workqueue \_ \_](mf-toponode-workqueue-item-priority.md)
-   [MMCSS-Priorität der MF- \_ toponode- \_ workqueue \_ \_](mf-toponode-workqueue-mmcss-priority.md)
-   [**MF-Dienst Warteschlange**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue)
-   [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex)
-   [**MF getworkqueuemmcsspriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)
-   [**Mfputwaitingworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem)
-   [**MFPutWorkItem2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem2)
-   [**MFPutWorkItemEx2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex2)
-   [**MF registerplatformwithmmcss**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)
-   [**Mfunregisterplatformfrommmcss**](/windows/desktop/api/mfapi/nf-mfapi-mfunregisterplatformfrommmcss)
-   [**Mflocksharedworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue)
-   [**Imfrealtimecliumtex**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeits Warteschlangen](work-queues.md)
</dt> </dl>

 

 
