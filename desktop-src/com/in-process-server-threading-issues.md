---
title: Threading Probleme bei In-Process Server
description: Threading Probleme bei In-Process Server
ms.assetid: 7bd6f62f-8c91-44bd-9a7f-d47988180eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d02af739eac11a6adae62de76be9078ee8e32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104391211"
---
# <a name="in-process-server-threading-issues"></a>Threading Probleme bei In-Process Server

Ein Prozess interner Server ruft nicht [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize), [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)oder [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) auf, um sein Threading Modell zu markieren. Bei Thread fähigen dll-basierten oder Prozess internen Objekten müssen Sie das Threading Modell in der Registrierung festlegen. Das Standardmodell, wenn Sie kein Threading Modell angeben, ist ein Single Thread pro Prozess. Wenn Sie ein Modell angeben möchten, fügen Sie den Wert **ThreadingModel** dem [InProcServer32](inprocserver32.md) -Schlüssel in der Registrierung hinzu.

DLLs, die die Instanziierung eines Klassen Objekts unterstützen, müssen die Funktionen [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) und [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)implementieren und exportieren. Wenn ein Client eine Instanz der Klasse wünscht, die die DLL unterstützt, Ruft ein Aufruf von [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (entweder direkt oder durch einen Aufruf von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) **DllGetClassObject** auf, um einen Zeiger auf das zugehörige Klassenobjekt zu erhalten, wenn das Objekt in einer DLL implementiert wird. **DllGetClassObject** sollte daher in der Lage sein, mehrere Klassen Objekte oder ein einzelnes Thread sicheres Objekt zu vertreiben (in der Regel nur mit [**interlockedinkrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) / [**InterlockedDecrement**](/windows/desktop/api/winbase/nf-winbase-interlockeddecrement) für Ihre internen Verweis Zähler).

Wie der Name schon sagt, wird [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow) aufgerufen, um zu bestimmen, ob die dll, die Sie implementiert, verwendet wird, sodass der Aufrufer ihn sicher entladen kann, wenn dies nicht der Fall ist. Aufrufe von [**cofreunusedlibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) von einem beliebigen Thread durchlaufen immer den Thread der Hauptwohnung, um **DllCanUnloadNow** aufzurufen.

Ebenso wie andere Server können Prozess interne Server einen Single Thread, Apartment Thread oder einen freien Thread aufweisen. Diese Server können von jedem OLE-Client verwendet werden, unabhängig vom Threading Modell, das von diesem Client verwendet wird.

Alle Kombinationen der Thread Modell Interoperabilität sind zwischen Clients und in-Process-Objekten zulässig. Die Interaktion zwischen einem Client und einem in-Process-Objekt, das verschiedene Threading Modelle verwendet, ähnelt der Interaktion zwischen Clients und Prozess internen Servern. Bei einem in-Process-Server, bei dem sich das Threading Modell des Clients und des in-Process-Servers unterscheidet, muss com sich zwischen dem Client und dem Objekt selbst positionieren.

Wenn ein in-Process-Objekt, das das Single Thread-Modell unterstützt, gleichzeitig von mehreren Threads eines Clients aufgerufen wird, kann com den Clientthreads nicht erlauben, direkt auf die Schnittpunkte des Objekts zuzugreifen. das Objekt wurde nicht für diesen Zugriff entworfen. Stattdessen muss com sicherstellen, dass Aufrufe synchronisiert werden und nur durch den Client Thread erstellt werden, von dem das Objekt erstellt wurde. Daher erstellt com das Objekt im Haupt Apartment des Clients und erfordert, dass alle anderen Client-Apartments mithilfe von Proxys auf das Objekt zugreifen.

Wenn ein frei Thread-Apartment (Multithreadapartment-Modell) in einem Client einen Apartment Thread-Prozess internen Server erstellt, startet com einen Single Thread-Apartment Modell-Host Thread im Client. Dieser Host Thread erstellt das Objekt, und der Schnittstellen Zeiger wird zurück an das frei Hand Thread-Apartment des Clients gemarshallt. Wenn ein Single Thread-Apartment in einem Apartment-Modell Client einen frei Hand Thread-Prozess internen Server erstellt, startet com einen frei Thread-Host Thread (Multithreadapartment), auf dem das Objekt erstellt und dann zurück an das Client-Single Thread-Apartment gemarshallt wird.

> [!Note]  
> Im Allgemeinen sollten Sie, wenn Sie eine benutzerdefinierte Schnittstelle auf einem in-Process-Server entwerfen, auch den Marshallingcode dafür bereitstellen, sodass com die Schnittstelle zwischen Client-Apartments Mars Hallen kann.

 

COM schützt den Zugriff auf Objekte, die von einer Single Thread-dll bereitgestellt werden, indem der Zugriff über das gleiche Client Apartment erforderlich ist, in dem Sie erstellt wurden. Außerdem sollte auf alle DLL-Einstiegspunkte (z. [**b. DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) und [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) und globale Daten immer durch dasselbe Apartment zugegriffen werden. COM erstellt solche Objekte im Haupt Apartment des Clients und gewährt dem Haupt Apartment direkt Zugriff auf die Zeiger des Objekts. Bei Aufrufen aus den anderen-Apartments wird das Thread-Marshalling verwendet, um vom Proxy zum Stub im Haupt Apartment und dann zum Objekt zu wechseln. Dies ermöglicht com das Synchronisieren von Aufrufen des Objekts. Interthreadaufrufe sind langsam, daher wird empfohlen, dass diese Server umgeschrieben werden, um mehrere Apartments zu unterstützen.

Wie bei einem in-Process-Single Thread-Server muss auf ein Objekt, das von einer Apartment-Modell-dll bereitgestellt wird, über das gleiche Client Apartment zugegriffen werden, von dem es erstellt wurde. Objekte, die von diesem Server bereitgestellt werden, können jedoch in mehreren Apartments des Clients erstellt werden, sodass der Server seine Einstiegspunkte (z. [**b. DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) und [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) für die Multithread-Verwendung implementieren muss. Wenn beispielsweise zwei Apartments eines Clients versuchen, zwei Instanzen des in-Process-Objekts gleichzeitig zu erstellen, kann **DllGetClassObject** gleichzeitig von beiden Apartments aufgerufen werden. **DllCanUnloadNow** muss so geschrieben werden, dass die dll nicht entladen wird, während der Code noch in der DLL ausgeführt wird.

Wenn die dll nur eine Instanz der Klassenfactory bereitstellt, um alle Objekte zu erstellen, muss die Klassenfactoryimplementierung auch für die Multithread-Verwendung entworfen werden, da Sie von mehreren Client-Apartments aufgerufen wird. Wenn die dll jedes Mal, wenn [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) aufgerufen wird, eine neue Instanz der Klassenfactory erstellt, muss die Klassenfactory nicht Thread sicher sein.

Von der Klassenfactory erstellte Objekte müssen nicht Thread sicher sein. Nach der Erstellung durch einen Thread erfolgt der Zugriff auf das Objekt immer über diesen Thread, und alle Aufrufe des Objekts werden durch com synchronisiert. Das Apartment Modell Apartment eines Clients, der dieses Objekt erstellt, erhält einen direkten Zeiger auf das-Objekt. Client-Apartments, die sich von dem Apartment unterscheiden, in dem das Objekt erstellt wurde, müssen über Proxys auf das Objekt zugreifen. Diese Proxys werden erstellt, wenn der Client die Schnittstelle zwischen seinen Apartments Marshalls.

Wenn ein in-Process-DLL- **ThreadingModel** -Wert auf "both" festgelegt ist, kann ein von dieser DLL bereitgestelltes Objekt in Single Thread-oder Multithread-Client-Apartments direkt erstellt und verwendet werden. Sie kann jedoch nur direkt in dem Apartment verwendet werden, in dem Sie erstellt wurde. Das Objekt muss gemarshallt werden, damit es einem anderen Apartment zugewiesen werden kann. Das dll-Objekt muss eine eigene Synchronisierung implementieren, und es kann gleichzeitig von mehreren Client-Apartments aufgerufen werden.

Um die Leistung für den Free-Thread-Zugriff auf in-Process-DLL-Objekte zu beschleunigen, stellt com die [**cofroatefreethreadedmarshaler**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) -Funktion bereit. Diese Funktion erstellt ein Freethread-Mars Haller-Objekt, das mit einem in-Process-Server Objekt aggregiert werden kann. Wenn ein Client Apartment im gleichen Prozess Zugriff auf ein Objekt in einem anderen Apartment benötigt, stellt das aggregierten Marshalling des frei Thread-Mars Haller dem Client einen direkten Zeiger auf das Server Objekt bereit, anstatt auf einen Proxy, wenn der Client die Schnittstelle des Objekts an ein anderes Apartment marshallelt. Der Client muss keine Synchronisierung durchführen. Dies funktioniert nur innerhalb desselben Prozesses. Standardmäßiges Marshalling wird für einen Verweis auf das Objekt verwendet, das an einen anderen Prozess gesendet wird.

Ein Objekt, das von einer Prozess internen dll bereitgestellt wird, die nur das kostenlose Threading unterstützt, ist ein Freethread-Objekt. Es implementiert eine eigene Synchronisierung, und es kann gleichzeitig von mehreren Clientthreads darauf zugegriffen werden. Dieser Server marshallt keine Schnittstellen zwischen Threads, sodass dieser Server direkt erstellt und (ohne Proxy) nur von multithreadwohnungen in einem Client verwendet werden kann. Single Thread-Apartments, die Sie erstellen, werden über einen Proxy darauf zugreifen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Schnittstellen über mehrere Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Auswählen des Threading Modells](choosing-the-threading-model.md)
</dt> <dt>

[Multithread-Apartments](multithreaded-apartments.md)
</dt> <dt>

[Prozesse, Threads und Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Single Thread-und Multithread-Kommunikation](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Single Thread-Apartments](single-threaded-apartments.md)
</dt> </dl>

 

 