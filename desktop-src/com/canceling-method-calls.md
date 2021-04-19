---
title: Abbrechen von Methoden aufrufen
description: Mit der Einführung verteilter und webbasierter Anwendungen können einige Methodenaufrufe für die Rückgabe sehr viel Zeit in Anspruch nehmen.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337263"
---
# <a name="canceling-method-calls"></a>Abbrechen von Methoden aufrufen

Mit der Einführung verteilter und webbasierter Anwendungen können einige Methodenaufrufe für die Rückgabe sehr viel Zeit in Anspruch nehmen. Die Latenz der Netzwerkverbindung kann hoch sein, der Server Computer kann viele Clients betreuen, oder die Serverkomponente übergibt möglicherweise eine große Datenmenge, z. b. eine Multimedia-Datei. Benutzer sollten in der Lage sein, eine Anforderung abzubrechen, die zu lange dauert, und die Anwendung sollte in der Lage sein, Abbruch Anforderungen zu verarbeiten und mit der anderen Arbeit fortzufahren. In com können Sie die [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) -Schnittstelle verwenden, um einen ausstehenden Anruf abzubrechen, der aus einem Single Thread-Apartment stammt.

Wenn ein Aufruf gemarshallt wird, erstellt der Proxy ein Cancel-Objekt, das die [**icancelmethodcalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) -Schnittstelle implementiert. Das Cancel-Objekt ist sowohl dem-Rückruf als auch dem Thread zugeordnet, für den der-Vorgang aussteht.

Um den ausstehenden-Befehl abzubrechen, übergibt der Client eine Abbruch Anforderung über das Cancel-Objekt, das die Details der Benachrichtigung des Server Objekts behandelt, dass der Rückruf abgebrochen wurde. Wenn die aufgerufene Methode nicht zurückgegeben hat, bereinigt das Server Objekt beim Erkennen der Abbruch Anforderung alle Programmressourcen, die Sie zugeordnet hat, und benachrichtigt den Client, indem er einen entsprechenden **HRESULT** -Wert zurückgibt, der die Ausführung des Aufrufs abgebrochen hat. Wenn die aufgerufene Methode bereits zurückgegeben wurde, benachrichtigt das Cancel-Objekt den Client. In beiden Fällen wird die Blockierung des Client Threads aufgehoben, und die Verarbeitung kann fortgesetzt werden.

Wie das Server Objekt auf eine Abbruch Anforderung antwortet, liegt im Ermessen des Implementierers des Servers, aber der aufrufende Thread auf dem Client wird immer die Blockierung aufgehoben und ignoriert alle Ergebnisse, die vom Server an ihn übergeben werden. Mithilfe von Cancel-Objekten können Sie anfordern, dass eine derzeit laufende Methode abgebrochen wird, aber es gibt keine Garantie dafür, dass das Server Objekt die Verarbeitung des Aufrufes beendet. Beispielsweise kann der-Rückruf bereits zurückgegeben worden sein, oder das Server Objekt unterstützt keine Cancel-Objekte.

COM stellt automatisch eine Standard Implementierung von Cancel-Objekten für Client Objekte und Schnittstellen bereit, die Standardmäßiges Marshalling verwenden. Für Objekte und Schnittstellen, die benutzerdefiniertes Marshalling verwenden, müssen Sie ein eigenes Cancel-Objekt implementieren.

Zu diesem Zeitpunkt werden bei Cancel-Objekten nur synchrone Aufrufe behandelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abbrechen eines asynchronen Aufrufes](canceling-an-asynchronous-call.md)
</dt> <dt>

[**Cogetcancelobject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[**Cosetcancelobject**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[**Cotestcancel**](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 