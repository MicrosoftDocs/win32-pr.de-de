---
title: Single-Threaded Apartment
description: Single-Threaded Apartment
ms.assetid: 2f345ae2-8314-4067-a6d6-5a0275941ed4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f9b969a48fd83ac82307c42bf4e801168bcf97f83536045fc078b19e3eb77d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129822"
---
# <a name="single-threaded-apartments"></a>Single-Threaded Apartment

Die Verwendung von Singlethread-Apartments (der Apartmentmodellprozess) bietet ein nachrichtenbasiertes Paradigma für den gleichzeitigen Umgang mit mehreren Objekten. Sie ermöglicht es Ihnen, effizienteren Code zu schreiben, indem ein Thread zugelassen wird, während er auf den Abschluss eines zeitaufwändigen Vorgangs wartet, um die Ausführung eines anderen Threads zuzulassen.

Jeder Thread in einem Prozess, der als Apartmentmodellprozess initialisiert wird und Fenstermeldungen abruft und verteilt, ist ein Singlethread-Apartmentthread. Jeder Thread befindet sich in seinem eigenen Apartment. Innerhalb eines Apartments können Schnittstellenzeiger ohne Marshalling übergeben werden. Daher kommunizieren alle Objekte in einem Singlethread-Apartmentthread direkt.

Eine logische Gruppierung verwandter Objekte, die alle in demselben Thread ausgeführt werden und daher eine synchrone Ausführung aufweisen müssen, kann sich auf demselben Singlethread-Apartmentthread befinden. Ein Apartmentmodellobjekt darf sich jedoch nicht auf mehr als einem Thread befinden. Aufrufe von Objekten in anderen Threads müssen im Kontext des besitzenden Threads erfolgen, sodass verteilte COM-Threads automatisch für Sie wechseln, wenn Sie für einen Proxy aufrufen.

Die Interprocess- und Interthread-Modelle sind ähnlich. Wenn es erforderlich ist, einen Schnittstellenzeiger an ein Objekt in einem anderen Apartment (in einem anderen Thread) innerhalb desselben Prozesses zu übergeben, verwenden Sie dasselbe Marshallingmodell, mit dem Objekte in verschiedenen Prozessen Zeiger über Prozessgrenzen hinweg übergeben. Indem Sie einen Zeiger auf das Standardmäßige Marshallingobjekt abrufen, können Sie Schnittstellenzeiger über Threadgrenzen (zwischen Apartments) auf die gleiche Weise marshallen wie zwischen Prozessen. (Schnittstellenzeiger müssen gemarshallt werden, wenn sie zwischen Apartments übergeben werden.)

Regeln für Singlethread-Apartments sind einfach, aber es ist wichtig, sie sorgfältig zu befolgen:

-   Jedes Objekt sollte sich nur in einem Thread (innerhalb eines Singlethread-Apartment) befinden.
-   Initialisieren Sie die COM-Bibliothek für jeden Thread.
-   Marshallen Sie alle Zeiger auf Objekte, wenn sie zwischen Apartments übergeben werden.
-   Jedes Singlethread-Apartment muss über eine Nachrichtenschleife verfügen, um Aufrufe von anderen Prozessen und Apartments innerhalb desselben Prozesses zu verarbeiten. Singlethread-Apartments ohne Objekte (nur Client) benötigen auch eine Nachrichtenschleife, um die Von einigen Anwendungen verwendeten Broadcastnachrichten zu senden.
-   DLL-basierte oder prozessbezogene Objekte rufen die COM-Initialisierungsfunktionen nicht auf. Stattdessen registrieren sie ihr Threadingmodell mit dem **ThreadingModel** named-value unter dem [InprocServer32-Schlüssel](inprocserver32.md) in der Registrierung. Apartmentfähige Objekte müssen auch SORGFÄLTIG DLL-Einstiegspunkte schreiben. Es gibt besondere Überlegungen, die für threading in-process-Server gelten. Weitere Informationen finden Sie unter [In-Process Server Threading Issues](in-process-server-threading-issues.md).

Mehrere Objekte können sich zwar in einem einzelnen Thread befinden, aber kein Apartmentmodellobjekt kann sich in mehr als einem Thread befinden.

Jeder Thread eines Clientprozesses oder Out-of-Process-Servers muss [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize)oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen und COINIT \_ APARTMENTTHREADED für den *dwCoInit-Parameter* angeben. Das Hauptapartment ist der Thread, der **Zuerst CoInitializeEx aufruft.** Informationen zu In-Process-Servern finden Sie unter [Threadingprobleme bei In-Process-Servern.](in-process-server-threading-issues.md)

Alle Aufrufe eines Objekts müssen in seinem Thread (innerhalb des Apartment) erfolgen. Es ist nicht zulässig, ein Objekt direkt aus einem anderen Thread aufzurufen. Die Verwendung von -Objekten auf diese Freethread-Weise kann zu Problemen für Anwendungen führen. Die Folge dieser Regel ist, dass alle Zeiger auf Objekte gemarshallt werden müssen, wenn sie zwischen Apartments übergeben werden. COM stellt zu diesem Zweck die folgenden beiden Funktionen bereit:

-   [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) marshallt eine Schnittstelle in ein Streamobjekt, das an den Aufrufer zurückgegeben wird.
-   [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) entfernt einen Schnittstellenzeiger aus einem Streamobjekt und gibt ihn frei.

Diese Funktionen umschließen Aufrufe der Funktionen [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) und [**CoUnmarshalInterface,**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) die die Verwendung des MSHCTX \_ INPROC-Flags erfordern.

Im Allgemeinen erfolgt das Marshalling automatisch durch COM. Wenn z. B. ein Schnittstellenzeiger als Parameter in einem Methodenaufruf für einen Proxy an ein Objekt in einem anderen Apartment übergeben wird oder [**wenn CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)aufgerufen wird, führt COM das Marshalling automatisch durch. In einigen besonderen Fällen, in denen der Anwendungswriter Schnittstellenzeiger zwischen Apartments übergibt, ohne die normalen COM-Mechanismen zu verwenden, muss der Writer das Marshalling jedoch manuell verarbeiten.

Wenn ein Apartment (Apartment 1) in einem Prozess über einen Schnittstellenzeiger verfügt und ein anderes Apartment (Apartment 2) seine Verwendung erfordert, muss Apartment 1 [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) aufrufen, um die Schnittstelle zu marshallen. Der von dieser Funktion erstellte Stream ist threadsicher und muss in einer Variablen gespeichert werden, auf die Apartment 2 zugreifen kann. Apartment 2 muss diesen Stream an [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) übergeben, um denMarshal der Schnittstelle zu aufheben, und erhält einen Zeiger auf einen Proxy zurück, über den es auf die Schnittstelle zugreifen kann. Das Hauptapartment muss aktiv bleiben, bis der Client alle COM-Arbeiten abgeschlossen hat (da einige in-process-Objekte im Hauptapartment geladen werden, wie unter [In-Process Server Threading Issues (In-Process-Serverthreadingprobleme)](in-process-server-threading-issues.md)beschrieben). Nachdem ein Objekt auf diese Weise zwischen Threads übergeben wurde, ist es sehr einfach, Schnittstellenzeiger als Parameter zu übergeben. Auf diese Weise führt verteiltes COM das Marshalling und Threadwechsel für die Anwendung durch.

Um Aufrufe von anderen Prozessen und Apartments innerhalb desselben Prozesses verarbeiten zu können, muss jedes Singlethread-Apartment über eine Nachrichtenschleife verfügen. Dies bedeutet, dass die Arbeitsfunktion des Threads über eine GetMessage/DispatchMessage-Schleife verfügen muss. Wenn andere Synchronisierungsprimitiven für die Kommunikation zwischen Threads verwendet werden, kann die [**MsgWaitForMultipleObjects-Funktion**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) verwendet werden, um sowohl auf Nachrichten als auch auf Threadsynchronisierungsereignisse zu warten. Die Dokumentation für diese Funktion enthält ein Beispiel für diese Art von Kombinationsschleife.

COM erstellt ein ausgeblendetes Fenster mithilfe der Windows -Klasse "OleMainThreadWndClass" in jedem Singlethread-Apartment. Ein Aufruf eines -Objekts wird als Fensternachricht an dieses ausgeblendete Fenster empfangen. Wenn das Apartment des Objekts die Nachricht abruft und weiterleitet, empfängt das ausgeblendete Fenster sie. Die Fensterprozedur ruft dann die entsprechende Schnittstellenmethode des -Objekts auf.

Wenn mehrere Clients ein Objekt aufrufen, werden die Aufrufe in der Nachrichtenwarteschlange in die Warteschlange eingereiht, und das Objekt empfängt jedes Mal einen Aufruf, wenn sein Apartment Nachrichten abruft und verteilt. Da die Aufrufe von COM synchronisiert werden und die Aufrufe immer vom Thread übermittelt werden, der zum Apartment des Objekts gehört, müssen die Schnittstellenimplementierungen des Objekts keine Synchronisierung bereitstellen. Singlethread-Apartments können [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) implementieren, damit sie Bei Bedarf Aufrufe abbrechen oder Fenstermeldungen empfangen können.

Das Objekt kann erneut gesendet werden, wenn eine seiner Schnittstellenmethodenimplementierungen Nachrichten abruft und weiterleitet oder einen ORPC-Aufruf an einen anderen Thread vornimmt, wodurch ein anderer Aufruf an das Objekt übermittelt wird (durch dasselbe Apartment). OLE verhindert nicht die Wiederinvarianz im selben Thread, kann aber zur Sicherheit von Threads beitragen. Dies ist identisch mit der Art und Weise, wie eine Fensterprozedur erneut eingelesen werden kann, wenn sie Nachrichten abruft und während der Verarbeitung einer Nachricht weiterleitet. Wenn Sie jedoch einen out-of-process-Singlethread-Apartmentserver aufrufen, der einen anderen Singlethread-Apartmentserver aufruft, kann der erste Server erneut aufgerufen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Schnittstellen zwischen Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Auswählen des Threadingmodells](choosing-the-threading-model.md)
</dt> <dt>

[Multithread-Apartment](multithreaded-apartments.md)
</dt> <dt>

[Threadingprobleme beim In-Process-Server](in-process-server-threading-issues.md)
</dt> <dt>

[Prozesse, Threads und Apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Singlethread- und Multithreadkommunikation](single-threaded-and-multithreaded-communication.md)
</dt> </dl>

 

 