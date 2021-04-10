---
title: Rückruf Synchronisierung
description: Rückruf Synchronisierung
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9254aceaaa8a6fa26d56d4a86987cc955b90dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039673"
---
# <a name="call-synchronization"></a>Rückruf Synchronisierung

COM-Anwendungen müssen in der Lage sein, bei der Verarbeitung eines oder mehrerer Aufrufe von com oder des Betriebssystems ordnungsgemäß mit Benutzereingaben umzugehen. COM bietet nur eine Synchronisierung für Single Thread-Apartments. Multithreadwohnungen (die frei Thread-Threads enthalten) empfangen beim Aufrufen von aufrufen (im gleichen Thread) keine Aufrufe. Multithread-Apartments können keine Synchronisierungs Aufrufe durchführen. Asynchrone Aufrufe werden in Multithread-Apartments in synchrone Aufrufe konvertiert. Der Nachrichtenfilter wird nicht für einen Thread in einem Multithread-Apartment aufgerufen. Weitere Informationen zu Threading Problemen finden Sie unter [Prozesse, Threads und Apartments](processes--threads--and-apartments.md).

COM-Aufrufe zwischen Prozessen können wie folgt in drei Kategorien unterteilt werden:

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Synchrone Aufrufe*
</dt> <dd>

Der größte Teil der Kommunikation, die innerhalb von com stattfindet, ist synchron. Beim Ausführen synchroner Aufrufe wartet der Aufrufer auf die Antwort, bevor er fortgesetzt wird, und kann eingehende Nachrichten empfangen. COM gibt eine modale Schleife für das warten auf die Antwort, das empfangen und weiterleiten anderer Nachrichten in einer kontrollierten Weise ein.

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Asynchrone Benachrichtigungen*
</dt> <dd>

Beim Senden von asynchronen Benachrichtigungen wartet der Aufrufer nicht auf die Antwort. COM verwendet [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) oder Ereignisse auf hoher Ebene, um asynchrone Benachrichtigungen zu senden, abhängig von der Plattform. COM definiert fünf asynchrone Methoden von [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink):

-   [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**Onrename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> Während com einen asynchronen Aufruf verarbeitet, können keine synchronen Aufrufe durchgeführt werden. Beispielsweise kann die Implementierung von [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) einer Containeranwendung keinen [**IPersistStorage:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save)-Rückruf enthalten. Diese Aufrufe sind die einzigen asynchronen Aufrufe, die von com unterstützt werden. Es gibt keine Möglichkeit, eine benutzerdefinierte Schnittstelle zu erstellen, die zu diesem Zeitpunkt asynchron ist.

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Eingabe synchronisierte Aufrufe*
</dt> <dd>

Beim Durchführen von Eingabe synchronisierten aufrufen muss das Objekt, das aufgerufen wird, den Aufruf vor der Rückgabe der Steuerung vervollständigen. Dadurch wird sichergestellt, dass die Fokus Verwaltung ordnungsgemäß funktioniert und dass die vom Benutzer eingegebenen Daten entsprechend verarbeitet werden. Diese Aufrufe werden von com über die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion durchgeführt, ohne dass eine modale Schleife eingegeben wird. Beim Verarbeiten eines Eingabe synchronisierten Aufrufs darf das aufgerufene Objekt keine Funktion oder Methode (einschließlich synchroner Methoden) aufrufen, die möglicherweise die Kontrolle übertragen. Die folgenden Methoden sind für die Eingabe synchronisiert.

-   [**IOleWindow:: GetWindow**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**IOleInPlaceActiveObject:: onframewindowaktivierungs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**IOleInPlaceActiveObject:: ondocwindowaktivierungs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**IOleInPlaceActiveObject:: resizeborder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**Ioleingeplaceuiwindow:: GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**Ioleingeplaceuiwindow:: RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**Ioleingeplaceuiwindow:: SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**IOleInPlaceFrame:: setMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**IOleInPlaceFrame:: SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**IOleInPlaceObject:: SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

Um Probleme zu minimieren, die bei der asynchronen Nachrichtenverarbeitung auftreten können, sind die meisten com-Methodenaufrufe synchron. Bei synchroner Kommunikation ist kein spezieller Code erforderlich, um eingehende Nachrichten zu verteilen und zu verarbeiten. Wenn eine Anwendung einen synchronen Methoden Aufrufvorgang durchführt, wechselt com in eine modale Warteschleife, die die erforderlichen Antworten verarbeitet und eingehende Nachrichten an Anwendungen sendet, die Sie verarbeiten können.

COM verwaltet Methodenaufrufe durch Zuweisen eines Bezeichners, der als *logische Thread-ID* bezeichnet wird. Ein neues wird zugewiesen, wenn ein Benutzer einen Menübefehl auswählt oder wenn die Anwendung einen neuen com-Vorgang initiiert. Nachfolgenden Aufrufen, die sich auf den anfänglichen com-Aufruf beziehen, wird dieselbe logische Thread-ID wie der erste Aufruf zugewiesen.

 

 