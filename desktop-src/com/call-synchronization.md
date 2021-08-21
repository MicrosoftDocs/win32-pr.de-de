---
title: Aufrufsynchronisierung
description: Aufrufsynchronisierung
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9969c968294a3dfdbfbc4cb78d40e64ad65c17392bf3b9fd09fc7a5f99b9049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048738"
---
# <a name="call-synchronization"></a>Aufrufsynchronisierung

COM-Anwendungen müssen in der Lage sein, benutzereingaben ordnungsgemäß zu verarbeiten, während mindestens ein Aufruf von COM oder dem Betriebssystem verarbeitet wird. COM ermöglicht die Aufrufsynchronisierung nur für Singlethread-Apartments. Multithread-Apartments (die Freethreadthreads enthalten) empfangen keine Aufrufe, während Sie Aufrufe (im gleichen Thread) durchführen. Multithread-Apartments können keine synchronisierten Eingabeaufrufe durchführen. Asynchrone Aufrufe werden in synchrone Aufrufe in Multithread-Apartments konvertiert. Der Nachrichtenfilter wird für keinen Thread in einem Multithread-Apartment aufgerufen. Weitere Informationen zu Threadingproblemen finden Sie unter [Prozesse, Threads und Apartment.](processes--threads--and-apartments.md)

COM-Aufrufe zwischen Prozessen lassen sich wie folgt in drei Kategorien unterteilen:

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Synchrone Aufrufe*
</dt> <dd>

Der Großteil der Kommunikation, die innerhalb von COM stattfindet, ist synchron. Wenn synchrone Aufrufe erfolgen, wartet der Aufrufer vor dem Fortfahren auf die Antwort und kann eingehende Nachrichten während des Wartens empfangen. COM wechselt in eine modale Schleife, um auf die Antwort zu warten und andere Nachrichten kontrolliert zu empfangen und zu senden.

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Asynchrone Benachrichtigungen*
</dt> <dd>

Beim Senden asynchroner Benachrichtigungen wartet der Aufrufer nicht auf die Antwort. COM verwendet Je nach Plattform [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) oder Ereignisse auf hoher Ebene, um asynchrone Benachrichtigungen zu senden. COM definiert fünf asynchrone Methoden von [**IAdviseSink:**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)

-   [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**Onsave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> Während COM einen asynchronen Aufruf verarbeitet, können keine synchronen Aufrufe erfolgen. Beispielsweise kann die Implementierung von [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) einer Containeranwendung keinen Aufruf von [**IPersistStorage::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save)enthalten. Diese Aufrufe sind die einzigen asynchronen Aufrufe, die von COM unterstützt werden. Es gibt keine Möglichkeit, eine benutzerdefinierte Schnittstelle zu erstellen, die zu diesem Zeitpunkt asynchron ist.

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Mit Eingabe synchronisierte Aufrufe*
</dt> <dd>

Wenn Eingabesynchronisierungsaufrufe ausgeführt werden, muss das aufgerufene Objekt den Aufruf abschließen, bevor das Steuerelement ausgegeben wird. Dadurch wird sichergestellt, dass die Fokusverwaltung ordnungsgemäß funktioniert und dass die vom Benutzer eingegebenen Daten ordnungsgemäß verarbeitet werden. Diese Aufrufe werden von COM über die [**SendMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessage) ausgeführt, ohne eine modale Schleife zu durchlaufen. Bei der Verarbeitung eines eingabesynchronisierten Aufrufs darf das aufgerufene Objekt keine Funktion oder Methode (einschließlich synchroner Methoden) aufrufen, die möglicherweise die Kontrolle liefern. Die folgenden Methoden sind eingabesynchronisiert.

-   [**IOleWindow::GetWindow**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**IOleInPlaceActiveObject::OnFrameWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**IOleInPlaceActiveObject::OnDocWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**IOleInPlaceActiveObject::ResizeBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**IOleInPlaceUIWindow::GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**IOleInPlaceUIWindow::RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**IOleInPlaceUIWindow::SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**IOleInPlaceFrame::SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**IOleInPlaceFrame::SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

Um Probleme zu minimieren, die bei der asynchronen Nachrichtenverarbeitung auftreten können, sind die meisten COM-Methodenaufrufe synchron. Bei der synchronen Kommunikation ist kein spezieller Code erforderlich, um eingehende Nachrichten zu senden und zu verarbeiten. Wenn eine Anwendung einen synchronen Methodenaufruf vornimmt, wechselt COM in eine modale Warteschleife, die die erforderlichen Antworten verarbeitet und eingehende Nachrichten an Anwendungen weiterleitet, die diese verarbeiten können.

COM verwaltet Methodenaufrufe, indem ein Bezeichner zugewiesen wird, der als *logische Thread-ID* bezeichnet wird. Ein neuer Befehl wird zugewiesen, wenn ein Benutzer einen Menübefehl auswählt oder wenn die Anwendung einen neuen COM-Vorgang initiiert. Nachfolgenden Aufrufen, die sich auf den ersten COM-Aufruf beziehen, wird die gleiche logische Thread-ID wie dem ersten Aufruf zugewiesen.

 

 