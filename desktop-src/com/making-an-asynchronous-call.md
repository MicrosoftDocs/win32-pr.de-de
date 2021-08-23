---
title: Ausführen eines asynchronen Aufrufs
description: Das Verfahren zum Ausführen eines synchronen Aufrufs ist einfach. Der Client ruft einen Schnittstellenzeiger für das Serverobjekt ab und ruft Methoden über diesen Zeiger auf. Der asynchrone Aufruf umfasst ein Aufrufobjekt, sodass es einige weitere Schritte umfasst.
ms.assetid: ab65d38d-836a-48d4-87c1-8812cbc8ff92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a153b826e570920fca2a92f5b53ed2079c561cbcda899b793cef1f39473bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755990"
---
# <a name="making-an-asynchronous-call"></a>Ausführen eines asynchronen Aufrufs

Das Verfahren zum Ausführen eines synchronen Aufrufs ist einfach: Der Client ruft einen Schnittstellenzeiger auf das Serverobjekt ab und ruft Methoden über diesen Zeiger auf. Der asynchrone Aufruf umfasst ein Aufrufobjekt, sodass es einige weitere Schritte umfasst.

Für jede Methode auf einer synchronen Schnittstelle implementiert die entsprechende asynchrone Schnittstelle zwei Methoden. Diese Methoden fügen die Präfixe Begin \_ und Finish an den Namen der \_ synchronen Methode an. Wenn beispielsweise eine Schnittstelle mit dem Namen ISimpleStream über eine Read-Methode verfügt, verfügt die AsyncISimpleStream-Schnittstelle über eine Begin Read- und \_ eine Finish \_ Read-Methode. Um einen asynchronen Aufruf zu starten, ruft der Client die Begin-Methode \_ auf.

**So starten Sie einen asynchronen Aufruf**

1.  Fragen Sie das Serverobjekt für die [**ICallFactory-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) ab. Wenn [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) E \_ NOINTERFACE zurückgibt, unterstützt das Serverobjekt keinen asynchronen Aufruf.

2.  Rufen [**Sie ICallFactory::CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) auf, um ein Aufrufobjekt zu erstellen, das der von Ihnen erstellten Schnittstelle entspricht, und geben Sie dann den Zeiger auf [**ICallFactory frei.**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory)

3.  Wenn Sie keinen Zeiger auf die asynchrone Schnittstelle aus dem Aufruf von [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall)anfordern, fragen Sie das Aufrufobjekt für die asynchrone Schnittstelle ab.

4.  Rufen Sie die entsprechende \_ Begin-Methode auf.

Das Serverobjekt verarbeitet nun den asynchronen Aufruf, und der Client kann andere Aufgaben ausführen, bis er die Ergebnisse des Aufrufs benötigt.

Ein Aufrufobjekt kann nur einen asynchronen Aufruf gleichzeitig verarbeiten. Wenn derselbe oder ein zweiter Client eine Begin-Methode aufruft, bevor ein ausstehender asynchroner Aufruf abgeschlossen ist, gibt die \_ Begin-Methode RPC E CALL PENDING \_ \_ \_ \_ zurück.

Wenn der Client die Ergebnisse der Begin-Methode nicht benötigt, kann er das Aufrufobjekt am Ende \_ dieser Prozedur veröffentlichen. COM erkennt diese Bedingung und bereinigt den Aufruf. Die Finish-Methode wird nicht aufgerufen, und der Client bekommt keine \_ Out-Parameter oder einen Rückgabewert.

Wenn das Serverobjekt bereit ist, von der Begin-Methode zurückzukehren, signalisiert es dem \_ Aufrufobjekt, dass es fertig ist. Wenn der Client bereit ist, überprüft er, ob das Aufrufobjekt signalisiert wurde. In diesem Zustand kann der Client den asynchronen Aufruf abschließen.

Der Mechanismus für diese Signalisierung und Überprüfung zwischen Client und Server ist die [**ISynchronize-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) für das Aufrufobjekt. Das Aufrufobjekt implementiert diese Schnittstelle normalerweise durch Aggregieren eines vom System bereitgestellten Synchronisierungsobjekts. Das Synchronisierungsobjekt umschließt ein Ereignishand handle, das der Server direkt vor der Rückgabe von der Begin-Methode durch Aufrufen von \_ [**ISynchronize::Signal signalisiert.**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal)

**So schließen Sie einen asynchronen Aufruf ab**

1.  Fragen Sie das Aufrufobjekt für die [**ISynchronize-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) ab.

2.  Rufen Sie [**ISynchronize::Wait auf.**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait)

3.  Wenn [**Wait RPC**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) E \_ \_ TIMEOUT zurückgibt, wird die Verarbeitung \_ der Begin-Methode nicht beendet. Der Client kann mit anderen Arbeiten fortfahren und **später erneut warten** aufrufen. Sie kann die Finish-Methode \_ erst aufrufen, wenn **Wait** S \_ OK zurückgibt.

    Wenn [**Wait S**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) OK \_ zurückgibt, wurde die \_ Begin-Methode zurückgegeben. Rufen Sie die entsprechende \_ Finish-Methode auf.

Die \_ Finish-Methode übergibt alle out-Parameter an den Client. Das Verhalten der asynchronen Methoden, einschließlich des Rückgabewerts der Finish-Methode, sollte genau mit dem der \_ entsprechenden synchronen Methode übereinstimmen.

Der Client kann das Aufrufobjekt veröffentlichen, sobald die Finish-Methode zurückgegeben wird, oder er kann einen Zeiger auf das Aufrufobjekt halten, um \_ weitere Aufrufe zu tätigen. In beiden Fällen ist der Client für die Freigabe des Aufrufobjekts verantwortlich, wenn das Objekt nicht mehr benötigt wird.

Wenn Sie eine Finish-Methode aufrufen, wenn kein Aufruf ausgeführt wird, gibt die Methode \_ RPC E CALL COMPLETE \_ \_ \_ zurück.

> [!Note]  
> Wenn sich die Client- und Serverobjekte im selben Apartment befinden, wird nicht garantiert, dass Aufrufe von [**ICallFactory::CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) erfolgreich sind. Wenn das Serverobjekt keinen asynchronen Aufruf für eine bestimmte Schnittstelle unterstützt, ist der Versuch, ein Aufrufobjekt zu erstellen, nicht möglich, und der Client muss die synchrone Schnittstelle verwenden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abbrechen eines asynchronen Aufrufs](canceling-an-asynchronous-call.md)
</dt> <dt>

[Clientsicherheit während eines asynchronen Aufrufs](client-security-during-an-asynchronous-call.md)
</dt> <dt>

[Identitätswechsel und asynchrone Aufrufe](impersonation-and-asynchronous-calls.md)
</dt> </dl>

 

 