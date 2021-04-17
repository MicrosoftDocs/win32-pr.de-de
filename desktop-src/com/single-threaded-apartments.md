---
title: Single-Threaded-Apartments
description: Single-Threaded-Apartments
ms.assetid: 2f345ae2-8314-4067-a6d6-5a0275941ed4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0a8cb1422b6866d9e0d043fdd46c895e6d335b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391053"
---
# <a name="single-threaded-apartments"></a>Single-Threaded-Apartments

Die Verwendung von Single Thread-Apartments (der Apartment modellprozess) bietet ein Nachrichten basiertes Paradigma für den Umgang mit mehreren Objekten, die gleichzeitig ausgeführt werden. Damit können Sie effizienteren Code schreiben, indem Sie einen Thread zulassen, während er auf den Abschluss eines zeitaufwändigen Vorgangs wartet, damit ein anderer Thread ausgeführt werden kann.

Jeder Thread in einem Prozess, der als Apartment modellprozess initialisiert wird und Fenster Nachrichten abruft und sendet, ist ein Single Thread-Apartment Thread. Jeder Thread befindet sich in einem eigenen Apartment. In einem Apartment können Schnittstellen Zeiger ohne Marshalling übermittelt werden, sodass alle Objekte in einem Single Thread-Apartment Thread direkt kommunizieren.

Eine logische Gruppierung von verknüpften Objekten, die alle im gleichen Thread ausgeführt werden und daher über eine synchrone Ausführung verfügen müssen, kann im gleichen Single Thread-Apartment Thread Leben. Ein Apartment Modell Objekt kann sich jedoch nicht in mehr als einem Thread befinden. Aufrufe von Objekten in anderen Threads müssen innerhalb des Kontexts des besitzenden Threads erfolgen. daher schaltet der verteilte com automatisch Threads für Sie ein, wenn Sie auf einem Proxy aufrufen.

Die prozessübergreifenden und interthreadmodelle ähneln einander. Wenn es erforderlich ist, einen Schnittstellen Zeiger an ein Objekt in einem anderen Apartment (in einem anderen Thread) innerhalb desselben Prozesses zu übergeben, verwenden Sie das gleiche marshallingmodell, das von Objekten in verschiedenen Prozessen verwendet wird, um Zeiger über Prozess Grenzen hinweg zu übergeben. Wenn Sie einen Zeiger auf das marshallingobjekt "Standard" erhalten, können Sie Schnittstellen Zeiger über Thread Grenzen hinweg (zwischen Apartments) auf die gleiche Weise wie zwischen Prozessen Mars Hallen. (Schnittstellen Zeiger müssen gemarshallt werden, wenn Sie zwischen Apartments übermittelt werden.)

Regeln für Single Thread-Apartments sind einfach, aber es ist wichtig, Sie sorgfältig zu befolgen:

-   Jedes Objekt sollte nur in einem Thread (in einem Single Thread-Apartment) Leben.
-   Initialisieren Sie die com-Bibliothek für jeden Thread.
-   Marshallt alle Zeiger auf Objekte, wenn Sie zwischen den Apartments übergeben werden.
-   Jedes Single Thread-Apartment muss über eine Nachrichten Schleife zum Verarbeiten von Aufrufen von anderen Prozessen und Apartments innerhalb desselben Prozesses verfügen. Single Thread-Apartments ohne Objekte (nur Client) benötigen auch eine Nachrichten Schleife, um die Broadcast Nachrichten zu verteilen, die von einigen Anwendungen verwendet werden.
-   DLL-basierte oder in-Process-Objekte werden die com-Initialisierungs Funktionen nicht aufzurufen. Stattdessen registrieren Sie Ihr Threading Modell mit dem Wert " **ThreadingModel** " mit dem Namen "-Value" unter dem Schlüssel " [InProcServer32](inprocserver32.md) " in der Registrierung. Apartment fähige Objekte müssen auch DLL-Einstiegspunkte sorgfältig schreiben. Für das Threading in-Process-Server gelten besondere Überlegungen. Weitere Informationen finden Sie unter [Prozess interne Server Threading Probleme](in-process-server-threading-issues.md).

Während mehrere-Objekte in einem einzelnen Thread Live sein können, kann kein Apartment Modell Objekt in mehr als einem Thread Leben.

Jeder Thread eines Client Prozesses oder out-of-Process-Servers muss [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize)aufrufen, oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen und coinit \_ Apartmentthreaded für den *dwcoinit* -Parameter angeben. Das Haupt Apartment ist der Thread, der zuerst **CoInitializeEx** aufruft. Informationen zu Prozess internen Servern finden Sie unter [Prozess interne Server Threading Probleme](in-process-server-threading-issues.md).

Alle Aufrufe an ein Objekt müssen in seinem Thread (in seinem Apartment) vorgenommen werden. Es ist unzulässig, ein Objekt direkt von einem anderen Thread aus aufzurufen. die Verwendung von Objekten in dieser frei Thread Weise kann zu Problemen bei Anwendungen führen. Diese Regel impliziert, dass alle Zeiger auf Objekte gemarshallt werden müssen, wenn Sie zwischen den Apartments übermittelt werden. COM stellt für diesen Zweck die folgenden zwei Funktionen bereit:

-   [**Comarshalinterthreadinterfakeinstream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) marshalltet eine Schnittstelle in ein Streamobjekt, das an den Aufrufer zurückgegeben wird.
-   [**Cogetinterfaceandreleasestream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) entfernt einen Schnittstellen Zeiger von einem Stream-Objekt und gibt diesen frei.

Diese Funktionen wrappen Aufrufe an die Funktionen [**comarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) und [**countrymarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) , die die Verwendung des mshctx \_ INPROC-Flags erfordern.

Im Allgemeinen wird das Marshalling automatisch durch com erreicht. Wenn z. b. ein Schnittstellen Zeiger als Parameter in einem Methodenaufruf eines Proxys für ein Objekt in einem anderen Apartment oder beim Aufrufen von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)übergeben wird, führt com das Marshalling automatisch durch. In einigen besonderen Fällen, in denen der anwendungswriter Schnittstellen Zeiger zwischen den Apartments übergibt, ohne die normalen com-Mechanismen zu verwenden, muss der Writer das Marshalling manuell verarbeiten.

Wenn ein Apartment (Apartment 1) in einem Prozess über einen Schnittstellen Zeiger verfügt und ein anderes Apartment (Apartment 2) seine Verwendung erfordert, muss Apartment 1 [**comarshalinterthreadinterfakeinstream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) aufrufen, um die Schnittstelle zu Mars Hallen. Der Stream, der von dieser Funktion erstellt wird, ist Thread sicher und muss in einer Variablen gespeichert werden, auf die von Apartment 2 aus zugegriffen werden kann. Apartment 2 muss diesen Datenstrom an [**cogetinterfaceandreleasestream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) übergeben, um das Marshalling der Schnittstelle zu entsperren, und erhält einen Zeiger auf einen Proxy, über den Sie auf die Schnittstelle zugreifen kann. Das Haupt Apartment muss aktiv bleiben, bis der Client alle com-Aufgaben abgeschlossen hat (da einige in-Process-Objekte in das Haupt Apartment geladen werden, wie unter [Prozess Server-Threading Probleme](in-process-server-threading-issues.md)beschrieben). Nachdem ein Objekt auf diese Weise zwischen Threads übergeben wurde, ist es sehr einfach, Schnittstellen Zeiger als Parameter zu übergeben. Auf diese Weise führt der verteilte com das Marshalling und den Thread Wechsel für die Anwendung aus.

Zum Verarbeiten von Aufrufen von anderen Prozessen und Apartments innerhalb desselben Prozesses muss jedes Single Thread-Apartment über eine Nachrichten Schleife verfügen. Dies bedeutet, dass die Arbeitsfunktion des Threads eine GetMessage/DispatchMessage-Schleife aufweisen muss. Wenn für die Kommunikation zwischen Threads andere Synchronisierungs primitiven verwendet werden, kann die [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) -Funktion verwendet werden, um sowohl auf Nachrichten als auch auf Thread Synchronisierungs Ereignisse zu warten. Die Dokumentation für diese Funktion enthält ein Beispiel für diese Art von Kombinations Schleife.

COM erstellt ein ausgeblendetes Fenster mithilfe der Windows-Klasse "olemainthreadwndclass" in jedem Single Thread-Apartment. Ein-Objekt wird als Fenster Meldung für dieses verborgene Fenster empfangen. Wenn das Apartment des Objekts die Nachricht abruft und sendet, empfängt das verborgene Fenster es. Die Fenster Prozedur ruft dann die entsprechende Schnittstellen Methode des-Objekts auf.

Wenn mehrere Clients ein Objekt aufrufen, werden die Aufrufe in der Nachrichten Warteschlange eingereiht, und das Objekt erhält jedes Mal einen Aufruf, wenn das Apartment Nachrichten abruft und sendet. Da die Aufrufe durch com synchronisiert werden und die Aufrufe immer durch den Thread übermittelt werden, der zum Apartment des Objekts gehört, müssen die Schnittstellen Implementierungen des Objekts keine Synchronisierung bereitstellen. Single Thread-Apartments können [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) implementieren, damit Sie bei Bedarf Aufrufe abbrechen oder Fenster Meldungen empfangen können.

Das Objekt kann erneut eingegeben werden, wenn eine seiner Schnittstellen Methoden Implementierungen Nachrichten abruft und sendet oder einen ORPC-Rückruf an einen anderen Thread sendet. Dadurch wird ein weiterer aufzurufende Befehl an das Objekt gesendet (durch das gleiche Apartment). OLE verhindert nicht den erneuten eintreten im gleichen Thread, kann jedoch zur Bereitstellung der Thread Sicherheit beitragen. Dies ist identisch mit der Art und Weise, in der eine Fenster Prozedur erneut eingegeben werden kann, wenn beim Verarbeiten einer Nachricht Nachrichten abgerufen und gesendet werden. Wenn Sie jedoch einen Out-of-Process-Single Thread-Apartment Server aufrufen, der einen anderen Single Thread-Apartment Server aufruft, kann der erste Server erneut eingegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Schnittstellen über mehrere Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Auswählen des Threading Modells](choosing-the-threading-model.md)
</dt> <dt>

[Multithread-Apartments](multithreaded-apartments.md)
</dt> <dt>

[Threading Probleme im Prozess internen Server](in-process-server-threading-issues.md)
</dt> <dt>

[Prozesse, Threads und Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Single Thread-und Multithread-Kommunikation](single-threaded-and-multithreaded-communication.md)
</dt> </dl>

 

 