---
title: Ausführen eines asynchronen Aufrufes
description: Die Vorgehensweise zum Ausführen eines synchronen Aufrufs besteht darin, dass der Client einen Schnittstellen Zeiger auf das Server Objekt erhält und Methoden über diesen Zeiger aufruft. Der asynchrone Aufruf umfasst ein Call-Objekt und umfasst daher einige weitere Schritte.
ms.assetid: ab65d38d-836a-48d4-87c1-8812cbc8ff92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22dcd7a6509cd07e12357a96222baa04f9e4c942
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391083"
---
# <a name="making-an-asynchronous-call"></a>Ausführen eines asynchronen Aufrufes

Die Vorgehensweise zum Ausführen eines synchronen Aufrufs ist unkompliziert: der Client ruft einen Schnittstellen Zeiger auf das Server Objekt ab und ruft Methoden über diesen Zeiger auf. Der asynchrone Aufruf umfasst ein Call-Objekt und umfasst daher einige weitere Schritte.

Für jede Methode in einer synchronen Schnittstelle implementiert die zugehörige asynchrone Schnittstelle zwei Methoden. Diese Methoden fügen die Präfixe "BEGIN" \_ und "Finish" \_ an den Namen der synchronen Methode an. Wenn eine Schnittstelle mit dem Namen isimplestream z. b. über eine Read-Methode verfügt, verfügt die asyncisimplestream-Schnittstelle über die Read \_ -Methode Begin und Finish Read \_ . Zum Starten eines asynchronen Aufrufs ruft der Client die BEGIN- \_ Methode auf.

**So beginnen Sie einen asynchronen Aufrufvorgang**

1.  Fragen Sie das Server Objekt für die [**icallfactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) -Schnittstelle ab. Wenn [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) E \_ nointerface zurückgibt, unterstützt das Server Objekt keinen asynchronen Aufruf.

2.  Rufen Sie [**icallfactory:: kreatecall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) auf, um ein Aufruf Objekt zu erstellen, das der gewünschten Schnittstelle entspricht, und geben Sie dann den Zeiger auf [**icallfactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory)frei.

3.  Wenn Sie keinen Zeiger auf die asynchrone Schnittstelle aus dem Aufrufen von " [**anatecall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall)" angefordert haben, Fragen Sie das calljekt für die asynchrone Schnittstelle ab.

4.  Ruft die entsprechende BEGIN- \_ Methode auf.

Das Server Objekt verarbeitet nun den asynchronen-Befehl, und der Client kann andere Aufgaben ausführen, bis die Ergebnisse des Aufrufes benötigt werden.

Ein Aufruf Objekt kann jeweils nur einen asynchronen Aufruf verarbeiten. Wenn derselbe oder ein zweiter Client eine BEGIN- \_ Methode aufruft, bevor ein ausstehender asynchroner Aufruf abgeschlossen ist, gibt die BEGIN- \_ Methode einen ausstehenden RPC-E- \_ \_ Aufruf \_ aus.

Wenn der Client die Ergebnisse der Begin-Methode nicht benötigt \_ , kann er das-Rückruf Objekt am Ende dieses Verfahrens freigeben. COM erkennt diese Bedingung und bereinigt den-Befehl. Die Finish \_ -Methode wird nicht aufgerufen, und der Client ruft keine out-Parameter oder einen Rückgabewert ab.

Wenn das Server Objekt bereit ist, von der BEGIN- \_ Methode zurückzukehren, signalisiert es dem aufzurufenden-Objekt. Wenn der Client bereit ist, wird überprüft, ob das Objekt des Aufrufes signalisiert wurde. Wenn dies der Fall ist, kann der Client den asynchronen-Aufrufvorgang beenden.

Der Mechanismus für diese Signalisierung und Prüfung zwischen Client und Server ist die [**isynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) -Schnittstelle für das calljekt. Das callsobjekt implementiert diese Schnittstelle normalerweise durch aggregierten eines vom System bereitgestellten Synchronisierungs Objekts. Das Synchronisierungs Objekt umschließt ein Ereignis handle, das der Server unmittelbar vor der Rückgabe von der Begin-Methode anzeigt, \_ indem [**isynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal)aufgerufen wird.

**So vervollständigen Sie einen asynchronen-Befehl**

1.  Fragen Sie das calltobjekt für die [**isynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) -Schnittstelle ab.

2.  Nennen Sie [**isynchronize:: Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait).

3.  Wenn der [**warte**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) Vorgang RPC \_ E Timeout zurückgibt \_ , ist die Verarbeitung der BEGIN- \_ Methode noch nicht abgeschlossen. Der Client kann mit anderen Arbeiten fortfahren und später erneut auf den **warte Vorgang warten** . Die "Finish"-Methode kann erst aufgerufen werden, \_ Wenn der **warte** Vorgang OK zurückgibt \_

    Wenn [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) den Wert S OK zurückgibt \_ , hat die BEGIN- \_ Methode zurückgegeben. Ruft die entsprechende Finish- \_ Methode auf.

Die \_ Methode Finish übergibt den Client alle out-Parameter. Das Verhalten der asynchronen Methoden, einschließlich des Rückgabewerts der Finish- \_ Methode, sollte genau mit der der entsprechenden synchronen Methode übereinstimmen.

Der Client kann das Aufruf Objekt freigeben, sobald die Methode "Finish" \_ zurückgibt, oder es kann einen Zeiger auf das Aufruf Objekt enthalten, um zusätzliche Aufrufe durchführen zu können. In beiden Fällen ist der Client für die Freigabe des calljektobjekts verantwortlich, wenn das Objekt nicht mehr benötigt wird.

Wenn Sie eine Finish- \_ Methode aufgerufen werden, wenn kein Aufruf ausgeführt wird, gibt die Methode den RPC- \_ E- \_ Aufruf \_ Complete zurück.

> [!Note]  
> Wenn sich die Client-und Server Objekte im selben Apartment befinden, ist der Aufruf von [**icallfactory:: | atecall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) nicht garantiert. Wenn das Server Objekt keinen asynchronen Aufruf für eine bestimmte Schnittstelle unterstützt, schlägt der Versuch, ein Call-Objekt zu erstellen, fehl, und der Client muss die synchrone-Schnittstelle verwenden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abbrechen eines asynchronen Aufrufes](canceling-an-asynchronous-call.md)
</dt> <dt>

[Client Sicherheit während eines asynchronen Aufrufes](client-security-during-an-asynchronous-call.md)
</dt> <dt>

[Identitätswechsel und asynchrone Aufrufe](impersonation-and-asynchronous-calls.md)
</dt> </dl>

 

 