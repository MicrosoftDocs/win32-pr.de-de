---
title: Hilfshilfsprogramme für die Out-of-Process-Server Implementierung
description: Hilfshilfsprogramme für die Out-of-Process-Server Implementierung
ms.assetid: 18641a84-56f8-4d27-9ddb-fa64011ac8ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 264d3f26b179b3ecb659ef93785c8c223b6c524e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391072"
---
# <a name="out-of-process-server-implementation-helpers"></a>Hilfshilfsprogramme für die Out-of-Process-Server Implementierung

Vier Hilfsfunktionen, die von Out-of-Process-Servern aufgerufen werden können, sind verfügbar, um das Schreiben von Servercode zu vereinfachen. Com-Clients und com-in-Process-Server werden Sie in der Regel nicht aufzurufen. Diese Funktionen sind so konzipiert, dass Racebedingungen bei der Server Aktivierung vermieden werden, wenn die Server über mehrere oder mehrere Klassen Objekte verfügen. Sie können jedoch auch für Single Thread-und Single Class-Objekt Server verwendet werden. Die Funktionen lauten wie folgt:

-   [**Coadref Server Process**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess)
-   [**Coreleaseserverprocess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)
-   [**Cosuspendclassobjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects)
-   [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)

Um ordnungsgemäß herunterzufahren, muss ein com-Server nachverfolgen, wie viele Objektinstanzen er instanziiert hat und wie oft die [**IClassFactory:: LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) -Methode aufgerufen wurde. Nur wenn die beiden Zahlen Null erreichen, kann ein Server heruntergefahren werden. Bei Single Thread-com-Servern wurde die Entscheidung für das Herunterfahren mit eingehenden Aktivierungs Anforderungen koordiniert, die von der Nachrichten Warteschlange serialisiert wurden. Der Server würde nach dem Empfang einer Freigabe auf der endgültigen Objektinstanz und der Entscheidung, dass er heruntergefahren wird, seine Klassen Objekte widerrufen, bevor weitere Aktivierungs Anforderungen gesendet werden. Wenn nach diesem Punkt eine Aktivierungs Anforderung aufgetreten ist, erkennt com, dass die Klassen Objekte widerrufen wurden, und gibt einen Fehler an den Dienststeuerungs-Manager (SCM) zurück, der dann eine neue Instanz des lokalen Server Prozesses ausführen würde.

Bei einem Apartment Modell Server, bei dem unterschiedliche Klassen Objekte in unterschiedlichen Apartments registriert sind, und bei allen frei Thread Servern, muss diese Entscheidung für das Herunterfahren mit Aktivierungs Anforderungen über mehrere Threads koordiniert werden, damit ein Thread des Servers nicht heruntergefahren wird, während ein anderer Thread des Servers mit der Ausgabe von Klassen Objekten oder Objektinstanzen beschäftigt ist. Ein klassischer, aber mühsamer Ansatz zur Lösung dieses Problems besteht darin, dass der Server, nachdem er seine Klassen Objekte widerrufen hat, seine Instanzanzahl erneut überprüft und aktiv bleibt, bis alle Instanzen freigegeben wurden.

Um es den Server Entwicklern zu erleichtern, diese Arten von Racebedingungen zu verarbeiten, bietet com zwei Verweis Zähl Funktionen:

-   " [**Coadresssserver Process**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) " erhöht einen globalen Verweis Zähler pro Prozess.
-   [**Coreleaseserverprocess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) Dekremente den globalen Verweis Zähler pro Prozess.

Wenn der globale Verweis Zähler pro Prozess den Wert Null erreicht, ruft com automatisch [**cosuspendclassobjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects)auf, wodurch verhindert wird, dass neue Aktivierungs Anforderungen eingehen. Der Server kann dann seine verschiedenen Klassen Objekte aus den verschiedenen Threads in der Freizeit aufheben, ohne dass eine andere Aktivierungs Anforderung eingehen kann. Alle neuen Aktivierungs Anforderungen werden von dem SCM verarbeitet, der eine neue Instanz des lokalen Server Prozesses startet.

Die einfachste Möglichkeit für eine lokale Serveranwendung, diese Funktionen zu nutzen, besteht darin, im Konstruktor für die einzelnen Instanzobjekte und in jeder der [**IClassFactory:: LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) -Methoden " [**coadressfserverprocess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) " aufzurufen, wenn der " *fLock* "-Parameter " **true**" ist. Die Serveranwendung sollte auch [**coreleaseserverprocess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) im debugtor der einzelnen Instanzobjekte und in jeder ihrer IClassFactory::**LockServer** -Methoden aufrufen, wenn der *fLock* -Parameter **false** ist.

Schließlich sollte die Serveranwendung auf den Rückgabecode von [**coreleaseserverprocess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)achten. Wenn Sie 0 zurückgibt, sollte die Serveranwendung die Bereinigung initiieren, die für einen Server mit mehreren Threads in der Regel bedeutet, dass Sie die verschiedenen Threads zum Beenden Ihrer Nachrichten Schleifen signalisieren und [**coadressfserverprocess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) und [**coreleaseserverprocess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)aufruft. Wenn die Verwaltungsfunktionen für die Server Prozess Lebensdauer verwendet werden, müssen Sie in den Objektinstanzen und in der [**Lock Server**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) -Methode verwendet werden. Andernfalls wird die Serveranwendung möglicherweise vorzeitig heruntergefahren.

Wenn eine [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) -Anforderung erfolgt, kontaktiert com den Server, marshüßt die [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle des Class-Objekts, kehrt zum Client Prozess zurück, entmarshunkt die **IClassFactory** -Schnittstelle und gibt Sie an den Client zurück. An diesem Punkt wird [**Lock Server**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) in der Regel mit " **true** " aufgerufen, um zu verhindern, dass der Server Prozess heruntergefahren wird. Es gibt jedoch ein Zeitfenster zwischen dem Marshalling des Klassen Objekts und dem Aufruf von **Lock Server** , bei dem ein anderer Client eine Verbindung mit dem gleichen Server herstellen kann, eine Instanz erhält und diese Instanz freigibt. auf diese Weise wird der Server heruntergefahren, und der erste Client kann mit einem getrennten **IClassFactory** -Zeiger hoch und trocken gelassen werden. Um diese Racebedingung zu vermeiden, fügt com einen impliziten **aufruflockserver** mit **true** dem Klassenobjekt hinzu, wenn es die **IClassFactory** -Schnittstelle Marshalls und einen impliziten Rückruf von **Lock Server** mit **false** hinzufügt, wenn der Client die **IClassFactory** -Schnittstelle freigibt. Aus diesem Grund ist es nicht notwendig, die Remote Aufrufe von **Lock Server** an den Server zurückzusetzen, und der Proxy für **LockServer** gibt einfach OK zurück, \_ ohne den Aufruf tatsächlich zu entfernen.

Während der Initialisierung eines Prozess internen Server Prozesses gibt es eine weitere Aktivierungs bezogene Racebedingung. Ein com-Server, der mehrere Klassen registriert, ruft in der Regel [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) mit dem lokalen REGCLS- \_ \_ Server für jede unterstützte CLSID auf. Nachdem dies für alle Klassen abgeschlossen ist, wechselt der Server in seine Nachrichten Schleife. Bei einem Single Thread-com-Server werden alle Aktivierungs Anforderungen blockiert, bis der Server in die Nachrichten Schleife eintritt. Bei einem Apartment Modell Server, der verschiedene Klassen Objekte in unterschiedlichen Apartments und für alle frei Thread Server registriert, können Aktivierungs Anforderungen jedoch früher eintreffen. Im Fall von Apartment Modell Servern können Aktivierungs Anforderungen eintreffen, sobald ein Thread eine Nachrichten Schleife eingegeben hat. Im Fall von kostenlosen Thread Servern kann eine Aktivierungs Anforderung eintreffen, sobald das erste Klassenobjekt registriert ist. Da eine Aktivierung zu einem frühen Zeitpunkt durchgeführt werden kann, ist es auch möglich, dass das endgültige Release stattfindet (und daher das Herunterfahren des Servers bewirken sollte), bevor der Rest des Servers die Initialisierung abschließen konnte.

Um diese Racebedingungen auszuschließen und die Aufgabe des serverwriters zu vereinfachen, sollte jeder Server, der mehrere Klassen Objekte mit com registrieren möchte, [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) mit REGCLS \_ local \_ Server \| REGCLS aufrufen, \_ die für jede andere vom Server unterstützte CLSID angehalten werden. Nachdem alle Klassen registriert wurden und der Server Prozess bereit ist, eingehende Aktivierungs Anforderungen zu akzeptieren, sollte der Server einen [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)-Befehl erstellen. Diese Funktion teilt com mit, den SCM über alle registrierten Klassen zu informieren, und beginnt damit, Aktivierungs Anforderungen an den Server Prozess zu übermitteln. Die Verwendung dieser Funktionen bietet die folgenden Vorteile:

-   Nur ein Aufruf wird an den SCM gerichtet, unabhängig davon, wie viele CLSIDs registriert sind. Dadurch wird die Gesamt Registrierungs Zeit (und damit auch die Startzeit der Serveranwendung) verringert.
-   Wenn der Server über mehrere Apartments verfügt und verschiedene CLSIDs in unterschiedlichen Apartments registriert sind, oder wenn es sich bei dem Server um einen frei Thread Server handelt, treten keine Aktivierungs Anforderungen ein, bis der Server [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)aufruft. Dadurch erhält der Server die Möglichkeit, alle seine CLSIDs zu registrieren und ordnungsgemäß einzurichten, bevor Sie Aktivierungs Anforderungen und mögliche Herunterfahren benötigen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuständigkeiten von com-Servern](com-server-responsibilities.md)
</dt> </dl>

 

 