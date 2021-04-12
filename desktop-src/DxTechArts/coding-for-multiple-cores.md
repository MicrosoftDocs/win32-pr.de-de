---
title: Codierung für Multicore auf Xbox 360 und Windows
description: Dieses Thema enthält eine Anleitung für die ersten Schritte bei der Multithreadprogrammierung.
ms.assetid: 661f13a6-c73d-8513-2bad-0ef9d1a361a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75899dacdfba829fc1a83e9393e6aa58574c9f30
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104391206"
---
# <a name="coding-for-multicore-on-xbox-360-and-windows"></a>Codierung für Multicore auf Xbox 360 und Windows

Seit Jahren hat sich die Leistung von Prozessoren stetig gesteigert, und Spiele und andere Programme haben die Vorteile dieser zunehmenden Leistung wiederholt, ohne dass Sie etwas Besonderes tun müssen.

Die Regeln wurden geändert. Die Leistung einzelner Prozessorkerne steigt jetzt sehr langsam, wenn überhaupt. Die computeleistung, die auf einem typischen Computer oder einer typischen Konsole verfügbar ist, wächst jedoch weiter. Der Unterschied besteht darin, dass der größte Teil dieses Leistungs Gewinns nun von mehreren Prozessorkernen auf einem einzelnen Computer (häufig in einem einzigen Chip) stammt. Die Xbox 360-CPU verfügt über drei Prozessorkerne auf einem Chip, und ungefähr 70 Prozent der 2006 verkauften PC-Prozessoren waren mehrere Kerne.

Die Zunahme der verfügbaren Verarbeitungsleistung ist genauso dramatisch wie in der Vergangenheit, aber jetzt müssen Entwickler Multithread-Code schreiben, um diese Leistungsfähigkeit zu nutzen. Die Multithreadprogrammierung bringt neue Entwurfs-und Programmierungs Herausforderungen mit sich. Dieses Thema enthält eine Anleitung für die ersten Schritte bei der Multithreadprogrammierung.

## <a name="the-importance-of-good-design"></a>Die Wichtigkeit eines guten Entwurfs

Ein guter Multithread-Programmentwurf ist wichtig, kann aber sehr schwierig sein. Wenn Sie Ihre großen Spielsysteme willkürlich in verschiedene Threads verschieben, werden Sie wahrscheinlich feststellen, dass jeder Thread die meiste Zeit mit dem warten auf die anderen Threads verbringt. Diese Art von Entwurf führt zu einer verbesserten Komplexität und einem erheblichen debuggingaufwand, ohne Leistungssteigerung.

Jedes Mal, wenn Threads Daten synchronisieren oder freigeben müssen, besteht die Möglichkeit, Daten zu beschädigen, den Synchronisierungs Aufwand, Deadlocks und Komplexität zu reduzieren. Daher muss der Multithread-Entwurf alle Synchronisierungs-und Kommunikationspunkte eindeutig dokumentieren, und diese Punkte sollten so weit wie möglich minimiert werden. Wenn Threads kommunizieren müssen, erhöht sich der Codierungsaufwand, was die Produktivität verringern kann, wenn sich dieser zu stark auf den Quellcode auswirkt.

Das einfachste Entwurfs Ziel für Multithreading besteht darin, den Code in große unabhängige Elemente aufzuteilen. Wenn Sie diese Teile dann so beschränken, dass Sie nur wenige Male pro Frame kommunizieren, wird eine deutliche Beschleunigung von Multithreading ohne unnötige Komplexität angezeigt.

## <a name="typical-threaded-tasks"></a>Typische Thread Aufgaben

Einige Arten von Aufgaben haben sich für das Platzieren von besser eher in separaten Threads bewährt. Die folgende Liste ist nicht als vollständig gedacht, sollte jedoch einige Ideen enthalten.

### <a name="rendering"></a>Darstellung

Rendering – Dies kann das Durchlaufen des Szenen Diagramms oder möglicherweise nur das Aufrufen von D3D-Funktionen umfassen – zählt häufig 50 Prozent oder mehr CPU-Zeit. Daher kann das Verschieben von Rendering in einen anderen Thread bedeutende Vorteile haben. Der Aktualisierungs Thread kann eine Art von renderbeschreibungs-Puffer ausfüllen, den der renderinglothread verarbeiten kann.

Der spielaktualisierungs Thread ist immer ein Frame vor dem Renderthread, d. h., es werden zwei Frames benötigt, bevor Benutzeraktionen auf dem Bildschirm angezeigt werden. Obwohl diese zunehmende Latenz ein Problem darstellen kann, wird durch die gestiegene Framerate beim Aufteilen der Arbeitsauslastung in der Regel die gesamte Latenzzeit akzeptabel.

In den meisten Fällen werden alle Renderingvorgänge weiterhin in einem einzelnen Thread ausgeführt, aber es handelt sich um einen anderen Thread aus dem Spiel Update.

Das D3DCREATE \_ -multithreadflag wird manchmal verwendet, um das Rendering in einer Thread-und Ressourcen Erstellung auf anderen Threads zuzulassen. dieses Flag wird auf Xbox 360 ignoriert, und Sie sollten es nicht unter Windows verwenden. Unter Windows zwingt die Angabe dieses Flags, dass D3D eine beträchtliche Zeit für die Synchronisierung verbringt und somit den Renderthread verlangsamt.

### <a name="file-decompression"></a>Datei Dekomprimierung

Ladezeiten sind immer zu lang, und das Streamen von Daten in den Arbeitsspeicher, ohne die Framerate zu beeinträchtigen, kann schwierig sein. Wenn alle Daten auf der Festplatte aggressiv komprimiert werden, ist die Daten Übertragungsgeschwindigkeit von der Festplatte oder der optischen Festplatte weniger wahrscheinlich ein einschränkender Faktor. Bei einem Single Thread-Prozessor ist in der Regel nicht genügend Prozessorzeit für die Komprimierung verfügbar, um das Laden von Zeiten zu unterstützen. Bei einem Multiprozessorsystem verwendet die Datei Dekomprimierung jedoch CPU-Zyklen, die andernfalls verschwendet würden. Es verbessert Ladezeiten und Streaming. und es spart Speicherplatz auf der Festplatte.

Verwenden Sie die Datei Dekomprimierung nicht als Ersatz für die Verarbeitung, die während der Produktion durchgeführt werden soll. Wenn Sie beispielsweise einen zusätzlichen Thread zum Durchlaufen von XML-Daten beim Laden der Ebene verwenden, verwenden Sie Multithreading nicht, um die Benutzeroberflächen zu verbessern.

Wenn Sie einen dateidekomprimierungsthread verwenden, sollten Sie weiterhin asynchrone Datei-e/a-Vorgänge und große Lesevorgänge verwenden, um die Daten Leseeffizienz zu maximieren.

### <a name="graphics-fluff"></a>Grafik Fluff

Es gibt viele grafische niceties, die das Aussehen des Spiels verbessern, aber nicht unbedingt notwendig sind. Dazu zählen z. b. Prozeduren mit Prozeduren, die für die prozedurale Generierung von Cloud-Animationen, Tuch-und Haar Simulationen, prozedurale Wellen, prozedurale

Da diese Auswirkungen sich nicht auf das-Spiel-Spiel auswirken, verursachen Sie keine schwierigen Synchronisierungs Probleme – Sie können einmal pro Frame oder seltener mit den anderen Threads synchronisiert werden. Außerdem können diese Effekte bei Spielen für Windows einen Mehrwert für Spieler mit Multikern-CPUs schaffen, während Sie auf Einzel Kern Computern im Hintergrund ausgelassen werden, sodass eine einfache Möglichkeit zur Skalierung über eine Vielzahl von Funktionen bietet.

### <a name="physics"></a>Physische Effekte

Die Physik kann häufig nicht in einem separaten Thread abgelegt werden, sodass Sie parallel zum Spiel Update ausgeführt werden kann, da das Spiel Update in der Regel die Ergebnisse der Physik-Berechnungen sofort erfordert. Die Alternative zum Multithreading der Physik besteht darin, Sie auf mehreren Prozessoren auszuführen. Obwohl dies möglich ist, ist es eine komplexe Aufgabe, die häufigen Zugriff auf freigegebene Datenstrukturen benötigt. Wenn Sie die Arbeitsauslastung der Physik so niedrig halten können, dass Sie in den Haupt Thread passt, ist Ihr Auftrag einfacher.

Bibliotheken, die das Ausführen von Physik in mehreren Threads unterstützen, sind verfügbar. Dies kann jedoch zu einem Problem führen: Wenn das Spiel die Physik betreibt, werden viele Threads verwendet, aber der Rest der Zeit verwendet nur wenige Threads. Das Ausführen von Physik in mehreren Threads erfordert dies, damit die Arbeitsauslastung gleichmäßig über den Frame verteilt wird. Wenn Sie eine Multithread-Physik-Engine schreiben, müssen Sie auf alle Datenstrukturen, Synchronisierungs Punkte und den Lastenausgleich achten.

## <a name="example-multithreaded-designs"></a>Beispiel für Multithread-Entwürfe

Spiele für Windows müssen auf Computern mit einer unterschiedlichen Anzahl von CPU-Kernen ausgeführt werden. Die meisten Spielcomputer haben immer noch nur einen Kern, obwohl die Anzahl der Computer mit zwei Kernen schnell zunimmt. Ein typisches Spiel für Windows kann seine Arbeitsauslastung in einem Thread für Update und Rendering unterbrechen, wobei optionale Arbeitsthreads zum Hinzufügen zusätzlicher Funktionen erforderlich sind. Außerdem werden wahrscheinlich einige Hintergrundthreads für die Datei-e/a und das Netzwerk verwendet. In Abbildung 1 werden die Threads sowie die Haupt Datenübertragungs Punkte angezeigt.

**Abbildung 1. Threading Design in einem Spiel für Windows**

![Threading Design in einem Spiel für Windows](images/coding-for-multiple-cores-1.gif)

Ein typisches Xbox 360-Spiel kann zusätzliche CPU-intensive Softwarethreads verwenden, sodass die Arbeitsauslastung möglicherweise in einen Aktualisierungs Thread, einen Renderingthread und drei Arbeitsthreads aufgeteilt wird, wie in Abbildung 2 dargestellt.

**Abbildung 2. Threading Design in einem Spiel für Xbox 360**

![Threading Design in einem Spiel für Xbox 360](images/coding-for-multiple-cores-2.gif)

Mit Ausnahme von Datei-e/a und Netzwerk können diese Aufgaben CPU-intensiv genug sein, um davon zu profitieren, dass Sie sich in einem eigenen Hardware Thread befinden. Diese Tasks können auch unabhängig voneinander unabhängig sein, dass Sie für einen gesamten Frame ausgeführt werden können, ohne zu kommunizieren.

Der spielaktualisierungs Thread verwaltet Controller Eingaben, Ki und Physik und bereitet Anweisungen für die anderen vier Threads vor. Diese Anweisungen werden in Puffer abgelegt, die sich im Besitz des Spiel Update Threads befinden, sodass keine Synchronisierung erforderlich ist, wenn die Anweisungen generiert werden.

Am Ende des Frames übergibt der Spiel Update Thread die Anweisungs Puffer an die vier anderen Threads und beginnt dann mit der Arbeit am nächsten Frame, wobei ein anderer Satz von Anweisungs Puffern ausgefüllt wird.

Da die Aktualisierungs-und renderingthreads in Gleichschritt zueinander funktionieren, werden Ihre Kommunikationspuffer einfach doppelt gepuffert: der Update Thread füllt zu jedem Zeitpunkt einen Puffer, während der Renderthread aus dem anderen liest.

Die anderen Arbeitsthreads sind nicht notwendigerweise an die Framerate gebunden. Das Entfernen eines Daten Teils kann wesentlich kleiner als ein Frame sein, oder es kann viele Frames in Anspruch nehmen. Selbst die Tuch-und Haar Simulationen müssen möglicherweise nicht exakt an der Framerate ausgeführt werden, da seltener Updates möglicherweise durchaus akzeptabel sind. Daher benötigen diese drei Threads unterschiedliche Datenstrukturen, um mit dem Aktualisierungs Thread und dem Renderthread zu kommunizieren. Beide benötigen eine Eingabe Warteschlange, die Arbeitsanforderungen aufnehmen kann, und der Renderthread benötigt eine Daten Warteschlange, die die von den Threads erzeugten Ergebnisse aufnehmen kann. Am Ende jedes Frames fügt der Update Thread einen Arbeitsspeicher Block zu den Warteschlangen von Arbeitsthreads hinzu. Wenn Sie die Liste nur einmal pro Frame hinzufügen, wird sichergestellt, dass der Synchronisierungs Aufwand durch den Update Thread minimiert Jede der Arbeitsthreads ruft so schnell wie möglich Zuweisungen aus der Arbeits Warteschlange ab, indem eine Schleife verwendet wird, die etwa wie folgt aussieht:


```C++
for(;;)
{
    while( WorkQueueNotEmpty() )
    {
        RemoveWorkItemFromWorkQueue();
        ProcessWorkItem();
        PutResultInDataQueue();
    }
    WaitForSingleObject( hWorkSemaphore ); 
}
```



Da die Daten aus den updatethreads in die Arbeitsthreads und dann in den Renderthread fließen, kann es eine Verzögerung von drei oder mehr Frames geben, bevor einige Aktionen Sie auf den Bildschirm übernehmen. Wenn Sie den Arbeitsthreads jedoch Latenz tolerante Aufgaben zuweisen, sollte dies kein Problem darstellen.

Ein alternatives Design besteht darin, mehrere Arbeitsthreads zu erstellen, die alle aus derselben Arbeits Warteschlange zeichnen. Dies würde einen automatischen Lastenausgleich ermöglichen und es wahrscheinlicher machen, dass alle Arbeitsthreads ausgelastet sind.

Der spielaktualisierungs Thread muss darauf achten, dass die Arbeitsthreads nicht zu viel Arbeit haben. andernfalls können die Arbeits Warteschlangen ständig zunehmen. Wie der Update Thread dies verwaltet, hängt von der Art der Aufgaben ab, die von den Arbeitsthreads ausgeführt werden.

## <a name="simultaneous-multithreading-and-number-of-threads"></a>Gleichzeitiges Multithreading und Anzahl von Threads

Alle Threads werden nicht gleich erstellt. Zwei Hardwarethreads befinden sich möglicherweise auf separaten Chips, auf dem gleichen Chip oder sogar auf demselben Kern. Die wichtigste Konfiguration für Spiel Programmierer ist es, zwei Hardwarethreads auf einem Kern – gleichzeitige Multithreading (SMT) oder Hyper-Threading Technologie (HT-Technologie) zu beachten.

SMT-oder HT-technologiethreads nutzen die Ressourcen des CPU-Kerns gemeinsam. Da Sie die Ausführungs Einheiten gemeinsam nutzen, liegt die maximale Beschleunigung bei der Ausführung von zwei Threads anstelle eines Werts in der Regel bei 10 bis 20 Prozent, anstatt bei 100 Prozent, die aus zwei unabhängigen Hardwarethreads möglich sind.

Noch wichtiger ist, dass SMT-oder HT-technologiethreads die L1-Anweisung und Daten Caches gemeinsam nutzen. Wenn Ihre Speicherzugriffsmuster nicht kompatibel sind, können Sie über den Cache hinaus kämpfen und viele Cache Fehler verursachen. Im schlimmsten Fall kann sich die Gesamtleistung für den CPU-Kern tatsächlich verringern, wenn ein zweiter Thread ausgeführt wird. Auf Xbox 360 ist dies ein relativ einfaches Problem. Die Konfiguration der Xbox 360 ist bekannt – drei CPU-Kerne mit jeweils zwei Hardwarethreads – und Entwickler weisen ihren Softwarethreads bestimmte CPU-Threads zu und können Messen, ob Ihr Threading Entwurf zusätzliche Leistung liefert.

Unter Windows ist die Situation komplizierter. Die Anzahl von Threads und deren Konfiguration variiert von Computer zu Computer, und das Ermitteln der Konfiguration ist kompliziert. Die Funktion [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) enthält Informationen über die Beziehung zwischen verschiedenen Hardwarethreads. diese Funktion ist unter Windows Vista, Windows 7 und Windows XP SP3 verfügbar. Daher müssen Sie derzeit die CPUID-Anweisung und die von Intel und AMD angegebenen Algorithmen verwenden, um zu entscheiden, wie viele "echte" Threads verfügbar sind. Weitere Informationen finden Sie unter "Verweise".

Das coreerkennungs-Beispiel im DirectX SDK enthält Beispielcode, der die [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) -Funktion oder die CPUID-Anweisung verwendet, um die CPU-Kern Topologie zurückzugeben. Die CPUID-Anweisung wird verwendet, wenn **GetLogicalProcessorInformation** auf der aktuellen Plattform nicht unterstützt wird. Coreerkennungen finden Sie an den folgenden Speicherorten:

<dl> <dt>

<span id="Source_"></span><span id="source_"></span><span id="SOURCE_"></span>Quelle:
</dt> <dd>

*DirectX-SDK* \\ -Stamm Beispiele \\ C++ Verschiedenes \\ \\ coreerkennung

</dd> <dt>

<span id="Executable_"></span><span id="executable_"></span><span id="EXECUTABLE_"></span>Bares
</dt> <dd>

*DirectX-SDK* \\ -Stamm Beispiele \\ C++ \\ misc \\ bin \\CoreDetection.exe

</dd> </dl>

Die sicherste Annahme besteht darin, dass nicht mehr als ein CPU-intensiver Thread pro CPU-Kern vorhanden ist. Die Verwendung von mehr CPU-intensiven Threads als CPU-Kerne bietet wenig oder keinen Vorteil und erhöht den zusätzlichen Aufwand und die Komplexität zusätzlicher Threads.

## <a name="creating-threads"></a>Erstellen von Threads

Das Erstellen von Threads ist ein relativ einfacher Vorgang, aber es gibt viele mögliche Fehler. Der folgende Code zeigt die ordnungsgemäße Methode zum Erstellen eines Threads, zum warten auf die Beendigung und zum anschließenden bereinigen.


```C++
const int stackSize = 65536;
HANDLE hThread = (HANDLE)_beginthreadex( 0, stackSize,
            ThreadFunction, 0, 0, 0 );
// Do work on main thread here.
// Wait for child thread to complete
WaitForSingleObject( hThread, INFINITE );
CloseHandle( hThread );

...

unsigned __stdcall ThreadFunction( void* data )
{
#if _XBOX_VER >= 200
    // On Xbox 360 you must explicitly assign
    // software threads to hardware threads.
    XSetThreadProcessor( GetCurrentThread(), 2 );
#endif
    // Do child thread work here.
    return 0;
}
```



Wenn Sie einen Thread erstellen, haben Sie die Möglichkeit, die Stapelgröße für den untergeordneten Thread anzugeben oder NULL anzugeben. in diesem Fall erbt der untergeordnete Thread die Stapelgröße des übergeordneten Threads. Auf Xbox 360, bei dem Stapel beim Start des Threads vollständig committet werden, kann durch die Angabe von NULL ein erheblicher Speicher verschwendet werden, da viele untergeordnete Threads nicht so viel Stapel wie das übergeordnete Element benötigen. Auf Xbox 360 ist es auch wichtig, dass die Stapelgröße ein Vielfaches von 64 KB ist.

Wenn Sie zum Erstellen von Threads die Funktion "up [**Thread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " verwenden, wird die C/C++-Laufzeit (CRT) unter Windows nicht ordnungsgemäß initialisiert. Es wird empfohlen, stattdessen die CRT [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) -Funktion zu verwenden.

Der Rückgabewert von " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " oder " [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) " ist ein Thread handle. Dieser Thread kann verwendet werden, um zu warten, bis der untergeordnete Thread beendet wird. Dies ist viel einfacher und effizienter als das Drehen in einer Schleife, die den Thread Status überprüft. Um zu warten, bis der Thread beendet wird, können Sie einfach [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) mit dem Thread handle aufzurufen.

Die Ressourcen für den Thread werden erst freigegeben, wenn der Thread beendet und das Thread Handle geschlossen wurde. Daher ist es wichtig, das Thread Handle mit [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) zu schließen, wenn Sie damit fertig sind. Wenn Sie darauf warten, dass der Thread mit [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)beendet wird, achten Sie darauf, den Handle erst zu schließen, nachdem der Warte Vorgang abgeschlossen wurde.

Auf Xbox 360 müssen Sie mithilfe von **xsetthreadprocessor** Software Threads einem bestimmten Hardware Thread explizit zuweisen. Andernfalls bleiben alle untergeordneten Threads auf demselben Hardware Thread wie das übergeordnete-Objekt. Unter Windows können Sie mit [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask) dem Betriebssystem dringend vorschlagen, auf welchen Hardwarethreads der Thread ausgeführt werden soll. Diese Technik sollte in Windows im allgemeinen vermieden werden, da Sie nicht wissen, welche anderen Prozesse möglicherweise auf dem System ausgeführt werden. Es ist in der Regel besser, den Windows-Scheduler die Zuweisung von Threads zu inaktiven Hardwarethreads zuzulassen.

Das Erstellen von Threads ist ein kostspieliger Vorgang. Threads sollten nur selten erstellt und zerstört werden. Wenn Sie erkennen möchten, dass Threads häufig erstellt und zerstört werden, verwenden Sie stattdessen einen Thread Pool, der auf die Arbeit wartet.

## <a name="synchronizing-threads"></a>Synchronisieren von Threads

Damit mehrere Threads zusammenarbeiten können, müssen Sie in der Lage sein, Threads zu synchronisieren, Nachrichten zu übergeben und exklusiven Zugriff auf Ressourcen anzufordern. Windows und Xbox 360 verfügen über einen umfangreichen Satz von Synchronisierungs primitiven. Ausführliche Informationen zu diesen Synchronisierungs primitiven finden Sie in der Dokumentation zur Plattform.

### <a name="exclusive-access"></a>Exklusiver Zugriff

Es ist eine häufige Notwendigkeit, exklusiven Zugriff auf eine Ressource, eine Datenstruktur oder einen Codepfad zu erhalten. Eine Möglichkeit, exklusiven Zugriff zu erhalten, ist ein Mutex, dessen typischer Gebrauch hier angezeigt wird.


```C++
// Initialize
HANDLE mutex = CreateMutex( 0, FALSE, 0 );

// Use
void ManipulateSharedData()
{
    WaitForSingleObject( mutex, INFINITE );
    // Manipulate stuff...
    ReleaseMutex( mutex );
}

// Destroy
CloseHandle( mutex );
The kernel guarantees that, for a particular mutex, only one thread at a time can 
acquire it.
The main disadvantage to mutexes is that they are relatively expensive to acquire 
and release. A faster alternative is a critical section.
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection( &cs );

// Use
void ManipulateSharedData()
{
    EnterCriticalSection( &cs );
    // Manipulate stuff...
    LeaveCriticalSection( &cs );
}

// Destroy
DeleteCriticalSection( &cs );
```



Kritische Abschnitte haben eine ähnliche Semantik wie Mutexen, Sie können jedoch nur innerhalb eines Prozesses und nicht zwischen Prozessen synchronisiert werden. Der Hauptvorteil besteht darin, dass Sie ungefähr zwanzig mal schneller als Mutexes ausgeführt werden.

### <a name="events"></a>Ereignisse

Wenn zwei Threads – vielleicht ein Aktualisierungs Thread und ein Renderthread – mit einem Paar von renderbeschreibungs Puffern verwendet werden, benötigen Sie eine Möglichkeit, anzugeben, wann Sie mit dem jeweiligen Puffer ausgeführt werden. Dies kann erreicht werden, indem ein Ereignis (das mit " [**forateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)" zugeordnet wird) jedem Puffer zugeordnet wird. Wenn ein Thread mit einem Puffer ausgeführt wird, kann er mithilfe von [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent) signalisiert werden, und dann kann [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) für das Ereignis des anderen Puffers aufgerufen werden. Mit dieser Methode können Sie problemlos eine dreifache Pufferung von Ressourcen durchlaufen.

### <a name="semaphores"></a>Semaphoren

Ein Semaphor wird verwendet, um zu steuern, wie viele Threads ausgeführt werden können, und wird häufig verwendet, um Arbeits Warteschlangen zu implementieren. Ein Thread fügt einer Warteschlange Arbeit hinzu und verwendet [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) , wenn der Warteschlange ein neues Element hinzugefügt wird. Dadurch kann ein Arbeits Thread aus dem Pool der wartenden Threads freigegeben werden. Die Arbeitsthreads nennen nur [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), und wenn Sie zurückgegeben wird, wissen Sie, dass ein Arbeits Element in der Warteschlange vorhanden ist. Außerdem muss ein kritischer Abschnitt oder eine andere Synchronisierungs Technik verwendet werden, um den sicheren Zugriff auf die freigegebene Arbeits Warteschlange zu gewährleisten.

### <a name="avoid-suspendthread"></a>SuspendThread vermeiden

Wenn Sie möchten, dass ein Thread den Vorgang beendet, ist es manchmal verlockend, [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) anstelle der richtigen Synchronisierungs primitiven zu verwenden. Dies ist immer eine gute Idee und kann problemlos zu Deadlocks und anderen Problemen führen. **SuspendThread** interagiert auch mit dem Visual Studio-Debugger nicht. Vermeiden Sie **SuspendThread**. Verwenden Sie stattdessen " [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) ".

### <a name="waitforsingleobject-and-waitformultipleobjects"></a>WaitForSingleObject und WaitForMultipleObjects

Die Funktion " [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) " ist die am häufigsten verwendete Synchronisierungs Funktion. Manchmal möchten Sie jedoch, dass ein Thread wartet, bis mehrere Bedingungen gleichzeitig erfüllt sind oder einer der Bedingungen erfüllt ist. In diesem Fall sollten Sie [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects)verwenden.

### <a name="interlocked-functions-and-lockless-programming"></a>Interlocked-Funktionen und Sperr lose Programmierung

Es gibt eine Reihe von Funktionen zum Ausführen einfacher Thread sicherer Vorgänge, ohne Sperren zu verwenden. Dabei handelt es sich um die Interlocked-Funktions Familie, z. b. [**interlockedinkrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement). Diese Funktionen und andere Techniken, die die sorgfältige Festlegung von Flags verwenden, werden zusammen als Lock less Programming bezeichnet. Die sperlocklose Programmierung kann sehr kompliziert sein, und Sie ist auf Xbox 360 erheblich schwieriger als unter Windows.

Weitere Informationen zum Programmieren ohne Sperren finden Sie unter [Überlegungen zur Sperr losen Programmierung für Xbox 360 und Microsoft Windows](./lockless-programming.md).

### <a name="minimizing-synchronization"></a>Minimierung der Synchronisierung

Einige Synchronisierungs Methoden sind schneller als andere. Anstatt den Code durch Auswahl der schnellsten Synchronisierungs Verfahren zu optimieren, ist es in der Regel besser, weniger häufig zu synchronisieren. Dies ist schneller als die Synchronisierung zu häufig, und vereinfacht den Code, der einfacher zu Debuggen ist.

Einige Vorgänge, z. b. Speicher Belegung, müssen möglicherweise Synchronisierungs primitive verwenden, damit Sie ordnungsgemäß funktionieren. Daher führt das Durchführen von häufigen Zuordnungen aus dem freigegebenen Standard Heap zu einer häufigen Synchronisierung, wodurch die Leistung beeinträchtigt wird. Die Vermeidung von häufigen Zuordnungen oder die Verwendung von Thread spezifischen Heaps (bei Verwendung von \_ HeapCreate mithilfe von Heap No \_ Serialize) kann diese verborgene Synchronisierung vermeiden.

Eine weitere Ursache für die verborgene Synchronisierung ist D3DCREATE \_ Multithreaded, was dazu führt, dass D3D unter Windows die Synchronisierung für viele Vorgänge verwendet. (Das Flag wird auf Xbox 360 ignoriert.)

Thread spezifische Daten, die auch als Thread lokaler Speicher bezeichnet werden, können eine wichtige Möglichkeit zum Vermeiden von Synchronisierungen sein. Visual C++ ermöglicht es Ihnen, globale Variablen mit der **\_ \_ declspec-Syntax (Thread)** als pro Thread zu deklarieren.


```C++
__declspec( thread ) int tls_i = 1;
```



Dadurch erhält jeder Thread im Prozess eine eigene Kopie von TLS \_ i, auf die sicher und effizient verwiesen werden kann, ohne dass eine Synchronisierung erforderlich ist.

Die Methode " **\_ \_ declspec (Thread)** " funktioniert nicht mit dynamisch geladenen DLLs. Wenn Sie dynamisch geladene DLLs verwenden, müssen Sie die TlsAlloc-Funktions Familie verwenden, um lokalen Thread Speicher zu implementieren.

## <a name="destroying-threads"></a>Zerstören von Threads

Der einzige sichere Weg, einen Thread zu zerstören, besteht darin, den Thread selbst zu beenden, indem er entweder von der Haupt Thread Funktion zurückgegeben wird oder der Thread [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) oder [**\_ endthreadex**](https://msdn.microsoft.com/library/hw264s73(v=VS.71).aspx)aufruft. Wenn ein Thread mit [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx)erstellt wird, sollte er **\_ endthreadex** verwenden oder von der Haupt Thread Funktion zurückkehren, da die Verwendung von **ExitThread** keine ordnungsgemäße kostenlose CRT-Ressourcen bereitstellt. Aufrufen der Funktion [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) nie, da der Thread nicht ordnungsgemäß bereinigt wird. Threads sollten immer einen Commit für Suizide durchsetzen – Sie sollten niemals ermordet werden.

## <a name="openmp"></a>OpenMP

OpenMP ist eine Spracherweiterung zum Hinzufügen von Multithreading zum Programm, indem Pragmas verwendet werden, um den Compiler in parallelisierungsschleifen zu unterstützen. OpenMP wird von Visual C++ 2005 unter Windows und Xbox 360 unterstützt und kann in Verbindung mit der manuellen Thread Verwaltung verwendet werden. OpenMP kann eine bequeme Möglichkeit zum Multithread von Teilen Ihres Codes sein, ist jedoch unwahrscheinlich, dass es sich um die ideale Lösung handelt, insbesondere bei spielen. OpenMP ist möglicherweise besser auf Produktionsaufgaben mit längerer Laufzeit wie z. b. die Verarbeitung von Grafiken und anderen Ressourcen anwendbar. Weitere Informationen finden Sie in der Visual C++-Dokumentation, oder besuchen Sie die [Website](https://www.openmp.org/)von OpenMP.

## <a name="profiling"></a>Profilerstellung

Die Multithread-Profilerstellung ist wichtig. Es ist ganz einfach, lange Zeiten zu finden, in denen Threads aufeinander warten. Diese Unterbrechungen können schwer zu finden und zu diagnostizieren sein. Um Sie leichter zu identifizieren, können Sie Ihren Synchronisierungs aufrufen Instrumentierungen hinzufügen. Ein Samplingprofiler kann auch helfen, diese Probleme zu identifizieren, da er Zeit Steuerungsinformationen aufzeichnen kann, ohne ihn erheblich zu ändern.

## <a name="timing"></a>Zeitliche Steuerung

Die RDTSC-Anweisung ist eine Möglichkeit, um genaue Zeit Steuerungsinformationen unter Windows zu erhalten. Leider weist RDTSC mehrere Probleme auf, die eine schlechte Wahl für Ihren Versand Titel machen. Die RDTSC-Leistungsindikatoren werden nicht zwangsläufig zwischen CPUs synchronisiert. Wenn also der Thread zwischen den Hardwarethreads verschoben wird, treten möglicherweise große positive oder negative Unterschiede auf. Abhängig von den Energie Verwaltungs Einstellungen kann sich die Häufigkeit, mit der die RDTSC-Leistungs-Counter-Vorgänge erhöht werden, bei der Ausführung des Spiels ändern. Um diese Probleme zu vermeiden, sollten Sie [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) für die zeitliche Steuerung mit hoher Genauigkeit in Ihrem Liefer Spiel bevorzugen. Weitere Informationen zur zeitlichen Steuerung finden Sie unter [Game Timing und Multicore-Prozessoren](./game-timing-and-multicore-processors.md).

## <a name="debugging"></a>Debuggen

Visual Studio unterstützt das Multithread-Debugging für Windows und Xbox 360 vollständig. Im Fenster "Visual Studio-Threads" können Sie zwischen Threads wechseln, um die verschiedenen Aufruf Listen und lokalen Variablen anzuzeigen. Im Fenster Threads können Sie auch bestimmte Threads fixieren und durch ein-und auslassen.

Auf Xbox 360 können Sie die **\@ hwthread** -Metavariable im Überwachungs Fenster verwenden, um den Hardware Thread anzuzeigen, in dem der derzeit ausgewählte Software Thread ausgeführt wird.

Das Fenster Threads ist einfacher zu verwenden, wenn Sie Ihre Threads als sinnvoll benennen. Mit Visual Studio und anderen Microsoft-Debuggern können Sie Ihre Threads benennen. Implementieren Sie die folgende **SetThreadName** -Funktion, und nennen Sie Sie von jedem Thread aus, während Sie gestartet wird.


```C++
typedef struct tagTHREADNAME_INFO
{
    DWORD dwType;     // must be 0x1000
    LPCSTR szName;    // pointer to name (in user address space)
    DWORD dwThreadID; // thread ID (-1 = caller thread)
    DWORD dwFlags;    // reserved for future use, must be zero
} THREADNAME_INFO;

void SetThreadName( DWORD dwThreadID, LPCSTR szThreadName )
{
    THREADNAME_INFO info;
    info.dwType = 0x1000;
    info.szName = szThreadName;
    info.dwThreadID = dwThreadID;
    info.dwFlags = 0;

    __try
    {
        RaiseException( 0x406D1388, 0,
                    sizeof(info) / sizeof(DWORD),
            (DWORD*)&info );
    }
    __except( EXCEPTION_CONTINUE_EXECUTION ) {
    }
}

// Example usage:
SetThreadName(-1, "Main thread");
```



Der Kernel Debugger (KD) und WinDbg unterstützen auch Multithread-Debuggen.

## <a name="testing"></a>Test

Die Multithreadprogrammierung kann knifflig sein, und einige multithreadfehler werden nur selten angezeigt, sodass Sie schwer zu finden und zu beheben sind. Eine der besten Möglichkeiten, Sie zu leeren, besteht darin, eine Vielzahl von Computern zu testen, insbesondere solche mit vier oder mehr Prozessoren. Multithread-Code, der auf einem Computer mit einem einzigen Thread einwandfrei funktioniert, kann auf einem Computer mit vier Prozessoren sofort fehlschlagen. Die Leistungs-und Zeit Steuerungsmerkmale von AMD-und Intel-CPUs können erheblich variieren. Achten Sie daher darauf, auf Multiprozessorcomputern auf der Grundlage von CPUs beider Hersteller zu testen.

## <a name="windows-vista-and-windows-7-improvements"></a>Verbesserungen für Windows Vista und Windows 7

Für Spiele, die auf die neueren Versionen von Windows abzielen, gibt es eine Reihe von APIs, die das Erstellen skalierbarer Multithreadanwendungen vereinfachen. Dies gilt insbesondere für die neue Thread Pool-API und einige zusätzliche syncrhonziationprimitiv (Bedingungs Variablen, schlanke Lese-/Schreibsperre und einmalige Initialisierung). Einen Überblick über diese Technologien finden Sie in den folgenden MSDN Magazine-Artikeln:

-   [Verbessern der Skalierbarkeit mit neuen Thread Pool-APIs](/archive/msdn-magazine/2007/october/pooled-threads-improve-scalability-with-new-thread-pool-apis)
-   [Neue Synchronisierungs primitive in Windows Vista](/archive/msdn-magazine/2007/june/concurrency-synchronization-primitives-new-to-windows-vista)

Anwendungen, die [Direct3D 11-Features](../direct3d11/direct3d-11-features.md) auf diesen Betriebssystemen verwenden, können auch den neuen Entwurf für die gleichzeitige Objekt Erstellung und verzögerte Kontext Befehlslisten nutzen, um eine bessere Skalierbarkeit für multithreadrendering zu erzielen.

## <a name="summary"></a>Zusammenfassung

Dank eines sorgfältigen Entwurfs, bei dem die Interaktionen zwischen Threads minimiert werden, können Sie mit der Multithreadprogrammierung beträchtliche Leistungssteigerungen erzielen, ohne Ihren Code übermäßig Komplex zu gestalten. Dadurch kann Ihr Spiel Code die nächste Generation von Prozessor Verbesserungen erreichen und immer mehr überzeugende Spiele Umgebungen bereitzustellen.

## <a name="references"></a>References

-   Jim Beveridge & Robert Weiner, *Multithreading Anwendungen in Win32*, Addison-Wesley, 1997
-   Chuck walbourn, [Game Timing und Multicore-Prozessoren](./game-timing-and-multicore-processors.md), Microsoft Corporation, 2005
-   MSDN Library: [ **GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)
-   [OpenMP](https://www.openmp.org/)

 

 