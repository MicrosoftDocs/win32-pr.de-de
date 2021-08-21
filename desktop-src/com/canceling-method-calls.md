---
title: Abbrechen von Methodenaufrufen
description: Mit der Einführung verteilter und webbasierter Anwendungen kann die Rückgabe einiger Methodenaufrufe inakzeptabel lange dauern.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ea089f257527dfd31d7120170c8749a2d1b4d60ba006843c7ff5d43403b352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311084"
---
# <a name="canceling-method-calls"></a>Abbrechen von Methodenaufrufen

Mit der Einführung verteilter und webbasierter Anwendungen kann die Rückgabe einiger Methodenaufrufe inakzeptabel lange dauern. Die Latenz der Netzwerkverbindung kann hoch sein, der Servercomputer kann viele Clients bedienen, oder die Serverkomponente überträgt möglicherweise eine große Menge an Daten, z. B. eine Multimediadatei. Benutzer sollten in der Lage sein, eine Anforderung abzubruchen, die zu lange dauern, und die Anwendung sollte In der Lage sein, Abbruchanforderungen zu verarbeiten und die anderen Arbeiten fortzufahren. In COM können Sie die [**IMessageFilter-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) verwenden, um einen ausstehenden Aufruf abzubricht, der aus einem Singlethread-Apartment stammt.

Wenn ein Aufruf gemarshallt wird, erstellt der Proxy ein Cancel-Objekt, das die [**ICancelMethodCalls-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) implementiert. Das cancel-Objekt ist sowohl dem Aufruf als auch dem Thread zugeordnet, für den der Aufruf aussteht.

Um den ausstehenden Aufruf abzubruchen, übergibt der Client eine Abbruchanforderung über das Cancel-Objekt, das die Details zur Benachrichtigung des Serverobjekts verarbeitet, dass der Aufruf abgebrochen wurde. Wenn die aufgerufene Methode nicht zurückgegeben hat, bereinigt das Serverobjekt bei der Erkennung der Abbruchanforderung alle zugeordneten Programmressourcen und benachrichtigt seinen Client, indem es einen entsprechenden **HRESULT-Wert** zurückgibt, dass die Ausführung des Aufrufs abgebrochen wurde. Wenn die aufgerufene Methode bereits zurückgegeben hat, benachrichtigt das Cancel-Objekt den Client. In beiden Fällen wird die Blockierung des Clientthreads aufgehoben, und die Verarbeitung kann fortgesetzt werden.

Wie das Serverobjekt auf eine Abbruchanforderung reagiert, liegt im Ermessen des Server implementers. Der aufrufende Thread auf dem Client wird jedoch immer entsperrt und ignoriert alle Ergebnisse, die der Server an ihn zu übergeben versucht. Cancel-Objekte stellen eine Möglichkeit dar, um anzuhalten, dass eine derzeit ausgeführte Methode abgebrochen wird. Es gibt jedoch keine Garantie, dass das Serverobjekt die Verarbeitung des Aufrufs beenden wird. Beispielsweise kann der Aufruf bereits zurückgegeben worden sein, oder das Serverobjekt unterstützt cancel-Objekte möglicherweise nicht.

COM stellt automatisch eine Standardimplementierung von Cancel-Objekten für Clientobjekte und Schnittstellen bereit, die standardmäßiges Marshalling verwenden. Für Objekte und Schnittstellen, die benutzerdefiniertes Marshalling verwenden, müssen Sie Ihr eigenes Cancel-Objekt implementieren.

Derzeit verarbeiten Cancel-Objekte nur synchrone Aufrufe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abbrechen eines asynchronen Aufrufs](canceling-an-asynchronous-call.md)
</dt> <dt>

[**CoGetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[**CoSetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[**CoTestCancel**](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 