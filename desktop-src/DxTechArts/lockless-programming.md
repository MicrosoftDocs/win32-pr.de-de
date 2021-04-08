---
title: Überlegungen zur blockierfreien Programmierung für Xbox 360 und Microsoft Windows
description: In diesem Artikel erhalten Sie einen Überblick über einige der Probleme, die bei der Verwendung von lockless-Programmiertechniken zu beachten sind.
ms.assetid: 44700352-a791-7ef7-0858-146214b0e3da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23bf8d66cada8aff00735fe6d6ac2d4f1369bc32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "103949214"
---
# <a name="lockless-programming-considerations-for-xbox-360-and-microsoft-windows"></a>Überlegungen zur blockierfreien Programmierung für Xbox 360 und Microsoft Windows

Die sperrenlose Programmierung ist eine Methode, um geänderte Daten sicher zwischen mehreren Threads freizugeben, ohne dass die Kosten für das Abrufen und Freigeben von Sperren anfallen. Das klingt wie ein Allheilmittel, aber die sperlocklose Programmierung ist komplex und sehr komplex und bietet manchmal nicht die Vorteile, die Sie verspricht. Die sperlocklose Programmierung ist auf Xbox 360 besonders komplex.

Die sperrenlose Programmierung ist ein gültiges Verfahren für die Multithreadprogrammierung, sollte jedoch nicht auf leichte Weise verwendet werden. Vor der Verwendung müssen Sie sich mit den Komplexitäten vertraut machen, und Sie sollten sorgfältig abwägen, um sicherzustellen, dass Sie die erwarteten Gewinne tatsächlich erhalten. In vielen Fällen gibt es einfachere und schnellere Lösungen, wie z. b. die seltener Freigabe von Daten, die stattdessen verwendet werden sollten.

Die korrekte und sichere Verwendung der sperlocklosen Programmierung erfordert sowohl die Hardware als auch den Compiler. In diesem Artikel erhalten Sie einen Überblick über einige der Probleme, die bei der Verwendung von lockless-Programmiertechniken zu beachten sind.

## <a name="programming-with-locks"></a>Programmieren mit Sperren

Beim Schreiben von Multithreadcode müssen häufig Daten zwischen Threads gemeinsam genutzt werden. Wenn mehrere Threads gleichzeitig die freigegebenen Datenstrukturen lesen und schreiben, kann eine Speicher Beschädigung auftreten. Die einfachste Möglichkeit, dieses Problem zu lösen, ist die Verwendung von Sperren. Wenn beispielsweise manipulateshareddata nur von einem Thread gleichzeitig ausgeführt werden soll, kann ein kritischer \_ Abschnitt verwendet werden, um dies zu gewährleisten, wie im folgenden Code:

``` syntax
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection(&cs);

// Use
void ManipulateSharedData()
{
    EnterCriticalSection(&cs);
    // Manipulate stuff...
    LeaveCriticalSection(&cs);
}

// Destroy
DeleteCriticalSection(&cs);
```

Dieser Code ist recht einfach und unkompliziert, und es ist leicht zu erkennen, dass er korrekt ist. Das Programmieren mit Sperren hat jedoch mehrere mögliche Nachteile. Wenn z. b. zwei Threads versuchen, dieselben zwei Sperren zu erhalten, Sie aber in einer anderen Reihenfolge erwerben, tritt möglicherweise ein Deadlock auf. Wenn ein Programm eine zu lange Sperre aufweist – aufgrund eines schlechten Entwurfs oder weil der Thread von einem Thread mit höherer Priorität ausgetauscht wurde – können andere Threads lange Zeit blockiert werden. Dieses Risiko eignet sich besonders gut für Xbox 360, da den Entwicklern vom Entwickler ein Hardware Thread zugewiesen wird und das Betriebssystem nicht in einen anderen Hardware Thread verschoben wird, auch wenn sich der Thread im Leerlauf befindet. Die Xbox 360 hat auch keinen Schutz vor Prioritäts-Inversion, bei der ein Thread mit hoher Priorität in einer Schleife steht, während er darauf wartet, dass ein Thread mit niedriger Priorität eine Sperre freigibt. Wenn ein verzögerter Prozedur Rückruf oder Interrupt Service Routine versucht, eine Sperre zu erhalten, erhalten Sie möglicherweise einen Deadlock.

Trotz dieser Probleme sind Synchronisierungs primitive, wie z. b. kritische Abschnitte, in der Regel die beste Methode zum Koordinieren mehrerer Threads. Wenn die Synchronisierungs primitiven zu langsam sind, besteht die beste Lösung in der Regel darin, diese seltener zu verwenden. Für diejenigen, die die zusätzliche Komplexität leisten können, ist eine andere Option die sperlocklose Programmierung.

## <a name="lockless-programming"></a>Sperlocklose Programmierung

Die sperrenlose Programmierung, wie der Name vermuten lässt, ist eine Reihe von Techniken zur sicheren Bearbeitung von freigegebenen Daten ohne Verwendung von Sperren. Es gibt Sperr lose Algorithmen für das Übergeben von Nachrichten, Freigabe Listen und Warteschlangen von Daten sowie andere Tasks.

Bei der sperlocklosen Programmierung gibt es zwei Herausforderungen, die Sie behandeln müssen: nicht atomarische Vorgänge und Neuanordnen.

## <a name="non-atomic-operations"></a>Nicht atomarische Vorgänge

Eine atomarische Operation ist eine unteilbare Operation – eine, bei der der Vorgang bei der Hälfte abgeschlossen wird. Atomarische Vorgänge sind für die sperlocklose Programmierung wichtig, da andere Threads möglicherweise halbgeschriebene Werte oder einen anderweitig inkonsistenten Zustand sehen.

Bei allen modernen Prozessoren können Sie davon ausgehen, dass Lese-und Schreibvorgänge von natürlich ausgerichteten systemeigenen Typen atomar sind. Solange der Speicherbus mindestens so breit ist wie der gelesene oder geschriebene Typ, liest und schreibt die CPU diese Typen in eine einzelne bustransaktion, sodass andere Threads Sie nicht in einem halb abgeschlossenen Zustand sehen können. Auf x86 und x64 gibt es keine Garantie, dass Lese-und Schreibvorgänge, die größer als acht Bytes sind, atomarisch sind. Dies bedeutet, dass 16-Byte-Lese-und-Schreibvorgänge von SSE-Registern (Streaming SIMD Extension) und Zeichen folgen Operationen möglicherweise nicht atomarisch sind.

Lese-und Schreibvorgänge von Typen, die nicht auf natürliche Weise ausgerichtet sind, z. –. das Schreiben von DWords, die vier-Byte-Begrenzungen überschreiten – sind nicht unbedingt atomarisch. Die CPU muss möglicherweise diese Lese-und Schreibvorgänge als mehrere bustransaktionen ausführen, sodass ein anderer Thread die Daten in der Mitte des Lese-oder Schreibzugriffs ändern oder anzeigen kann.

Zusammengesetzte Vorgänge, wie z. b. die Sequenz für Lese-und Schreibvorgänge, die beim Inkrement einer freigegebenen Variablen auftritt, sind nicht atomarisch. Auf Xbox 360 werden diese Vorgänge als mehrere Anweisungen (LWZ, ADDI und STW) implementiert, und der Thread kann durch die Sequenz durchlaufen werden. Bei x86 und x64 gibt es eine einzige Anweisung (Inc), mit der eine Variable im Arbeitsspeicher erhöht werden kann. Wenn Sie diese Anweisung verwenden, ist das Inkrementieren einer Variablen für Systeme mit nur einem Prozessor atomarisch, aber auf Systemen mit mehreren Prozessoren ist Sie immer noch nicht atomar. Das Erstellen von Inc Atomic auf x86-und x64-basierten Multiprozessorsystemen erfordert die Verwendung des Sperr Präfixes, das verhindert, dass ein anderer Prozessor eine eigene Lese-/Schreib-Schreibsequenz zwischen dem Lese-und dem Schreibvorgang der Inc-Anweisung durchführen kann.

Der folgende Code zeigt einige Beispiele:

``` syntax
// This write is not atomic because it is not natively aligned.
DWORD* pData = (DWORD*)(pChar + 1);
*pData = 0;

// This is not atomic because it is three separate operations.
++g_globalCounter;

// This write is atomic.
g_alignedGlobal = 0;

// This read is atomic.
DWORD local = g_alignedGlobal;
```

## <a name="guaranteeing-atomicity"></a>Gewährleisten der Atomizität

Sie können mit einer Kombination der folgenden atomischen Vorgänge sicher sein:

-   Natürlich atomarische Vorgänge
-   Sperren zum Einschließen von zusammengesetzten Vorgängen
-   Betriebssystemfunktionen, die atomarische Versionen beliebter zusammengesetzter Vorgänge implementieren

Das Inkrementieren einer Variablen ist kein atomarer Vorgang, und das Inkrementieren kann zu Daten Beschädigungen führen, wenn Sie in mehreren Threads ausgeführt werden.

``` syntax
// This will be atomic.
g_globalCounter = 0;

// This is not atomic and gives undefined behavior
// if executed on multiple threads
++g_globalCounter;
```

Win32 verfügt über eine Reihe von Funktionen, die atomarische Lese-und Schreibvorgänge für verschiedene gängige Vorgänge bieten. Dabei handelt es sich um die interlockedxxx-Funktions Familie. Wenn alle Änderungen der freigegebenen Variablen diese Funktionen verwenden, sind die Änderungen Thread sicher.

``` syntax
// Incrementing our variable in a safe lockless way.
InterlockedIncrement(&g_globalCounter);
```

## <a name="reordering"></a>Neuanordnung

Ein feineres Problem ist die Neuanordnung. Lese-und Schreibvorgänge erfolgen nicht immer in der Reihenfolge, in der Sie Sie in Ihren Code geschrieben haben, und dies kann zu sehr verwirrenden Problemen führen. In vielen multithreadalgorithmen schreibt ein Thread einige Daten und schreibt dann in ein Flag, das anderen Threads mitteilt, dass die Daten bereit sind. Dies wird als "Write-Release" bezeichnet. Wenn die Schreibvorgänge neu angeordnet werden, sehen andere Threads möglicherweise, dass das Flag festgelegt ist, bevor die geschriebenen Daten angezeigt werden.

Ebenso liest ein Thread in vielen Fällen aus einem Flag und liest dann einige freigegebene Daten, wenn das Flag besagt, dass der Thread Zugriff auf die freigegebenen Daten erlangt hat. Dies wird als Lesezugriff bezeichnet. Wenn Lesevorgänge neu angeordnet werden, werden die Daten möglicherweise vor dem-Flag aus dem freigegebenen Speicher gelesen, und die angezeigten Werte sind möglicherweise nicht auf dem neuesten Stand.

Die Neuanordnung von Lese-und Schreibvorgängen kann sowohl vom Compiler als auch vom Prozessor durchgeführt werden. Compiler und Prozessoren haben diese Neuanordnung seit Jahren ausgeführt, aber auf Computern mit nur einem Prozessor war es weniger ein Problem. Dies liegt daran, dass die CPU-Neuanordnung von Lese-und Schreibvorgängen auf Computern mit nur einem Prozessor unsichtbar ist (für nicht-Gerätetreiber Code, der nicht Teil eines Gerätetreibers ist), und die Neuanordnung von Lese-und Schreibvorgängen durch den Compiler weniger wahrscheinlich Probleme auf Computern mit einem Prozessor verursacht.

Wenn der Compiler oder die CPU die im folgenden Code gezeigten Schreibvorgänge neu anordnet, kann ein anderer Thread feststellen, dass das Alive-Flag festgelegt ist, während die alten Werte für x oder y weiterhin angezeigt werden. Ähnliche Neuanordnung kann beim Lesen auftreten.

In diesem Code fügt ein Thread einen neuen Eintrag zum Sprite-Array hinzu:

``` syntax
// Create a new sprite by writing its position into an empty
// entry and then setting the ‘alive' flag. If ‘alive' is
// written before x or y then errors may occur.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
g_sprites[nextSprite].alive = true;
```

Im nächsten Codeblock liest ein weiterer Thread aus dem Sprite-Array:

``` syntax
// Draw all sprites. If the reads of x and y are moved ahead of
// the read of ‘alive' then errors may occur.
for( int i = 0; i < numSprites; ++i )
{
    if( g_sprites[nextSprite].alive )
    {
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

Um dieses Sprite-System sicher zu machen, müssen wir sowohl die Compilerfunktion als auch die CPU-Neuanordnung von Lese-und Schreibvorgängen verhindern

### <a name="understanding-cpu-rearrangement-of-writes"></a>Grundlegendes zur CPU-Umgestaltung von Schreibvorgängen

Einige CPUs ordnen Schreibvorgänge neu an, sodass Sie extern für andere Prozessoren oder Geräte in nicht-Programm Reihenfolge sichtbar sind. Diese Neuanordnung ist für Single Thread-nicht-Treibercode nie sichtbar, kann jedoch Probleme im Multithread-Code verursachen.

### <a name="xbox-360"></a>Xbox 360

Während die Xbox 360-CPU keine Neuanordnung von Anweisungen durchführt, werden Schreibvorgänge, die nach den Anweisungen selbst ausgeführt werden, neu angeordnet. Diese Neuanordnung von Schreibvorgängen ist durch das PowerPC-Speichermodell ausdrücklich zulässig.

Schreibvorgänge auf Xbox 360 gelangen nicht direkt in den L2-Cache. Zum Verbessern der Schreib Bandbreite des L2-Caches durchlaufen Sie stattdessen Speicher Warteschlangen und dann Speicher-Gather-Puffer. Die Speicher-Gather-Puffer ermöglichen es, dass 64-Byte-Blöcke in einem Vorgang in den L2-Cache geschrieben werden. Es gibt acht Speicher-Gather-Puffer, die effizientes Schreiben in verschiedene Bereiche des Arbeitsspeichers ermöglichen.

Die Speicher-Gather-Puffer werden normalerweise in FIFO-Reihenfolge (First-in-First-Out) in den L2-Cache geschrieben. Wenn sich die Ziel Cache Zeile eines Schreibzugriffs jedoch nicht im L2-Cache befindet, kann dieser Schreibvorgang verzögert werden, während die Cache Zeile aus dem Arbeitsspeicher abgerufen wird.

Auch wenn die Speicher Sammel Puffer in strenger FIFO-Reihenfolge in den L2-Cache geschrieben werden, gewährleistet dies nicht, dass einzelne Schreibvorgänge in der richtigen Reihenfolge in den L2-Cache geschrieben werden. Stellen Sie sich beispielsweise vor, dass die CPU an Speicherort 0x1000, dann an Speicherort 0x2000 und dann an Speicherort 0x1004 schreibt. Beim ersten Schreibvorgang wird ein Speicher Sammel Puffer zugewiesen und an der Vorderseite der Warteschlange abgelegt. Der zweite Schreibvorgang ordnet einen anderen Store-Gather-Puffer zu und fügt ihn als nächstes in die Warteschlange ein. Der dritte Schreibvorgang fügt seine Daten zum ersten Store-Gather-Puffer hinzu, der am Anfang der Warteschlange verbleibt. Daher wird der dritte Schreibvorgang vor dem zweiten Schreibvorgang in den L2-Cache überlaufen.

Die Neuanordnung durch Speicher Sammel Puffer ist grundsätzlich unvorhersehbar, insbesondere weil beide Threads auf einem Kern die Speicher Sammel Puffer gemeinsam nutzen, sodass die Speicher Sammel Puffer stark variabel werden.

Dies ist ein Beispiel dafür, wie Schreibvorgänge neu angeordnet werden können. Möglicherweise gibt es weitere Möglichkeiten.

### <a name="x86-and-x64"></a>x86 und x64

Obwohl x86-und x64-CPUs Anweisungen neu anordnen, ordnen Sie Schreibvorgänge im Vergleich zu anderen Schreibvorgängen in der Regel nicht neu an. Es gibt einige Ausnahmen für den Schreib kombinierten Arbeitsspeicher. Außerdem können Zeichen folgen Vorgänge (muvs und STOS) und 16-Byte-SSE-Schreibvorgänge intern neu angeordnet werden. andernfalls werden Schreibvorgänge relativ zueinander nicht neu angeordnet.

### <a name="understanding-cpu-rearrangement-of-reads"></a>Grundlegendes zur CPU-Umgestaltung von Lesevorgängen

Einige CPUs ordnen Lesevorgänge neu an, sodass Sie tatsächlich aus dem freigegebenen Speicher in nicht-Programm Reihenfolge stammen. Diese Neuanordnung ist für Single Thread-nicht-Treibercode nie sichtbar, kann jedoch Probleme im Multithread-Code verursachen.

### <a name="xbox-360"></a>Xbox 360

Cache Fehler können dazu führen, dass einige Lesevorgänge verzögert werden, was dazu führt, dass Lesevorgänge nicht in der richtigen Reihenfolge aus dem freigegebenen Speicher stammen und die zeitliche Steuerung dieser Cache Fehler grundsätzlich unvorhersehbar ist. Ein Vorabruf und eine Verzweigungs Vorhersage können auch bewirken, dass Daten aus dem freigegebenen Speicher entfernt werden. Dies sind nur einige Beispiele dafür, wie Lesevorgänge neu angeordnet werden können. Möglicherweise gibt es weitere Möglichkeiten. Diese Neuanordnung von Lesevorgängen ist durch das PowerPC-Speichermodell ausdrücklich zulässig.

### <a name="x86-and-x64"></a>x86 und x64

Obwohl x86-und x64-CPUs Anweisungen neu anordnen, ordnen Sie Lesevorgänge im Vergleich zu anderen Lesevorgängen in der Regel nicht neu an. Zeichen folgen Operationen (muvs und STOS) und 16-Byte-SSE-Lesevorgänge können intern neu angeordnet werden. andernfalls werden Lesevorgänge relativ zueinander nicht neu angeordnet.

### <a name="other-reordering"></a>Andere Neuanordnen

Obwohl x86-und x64-CPUs Schreibvorgänge relativ zu anderen Schreibvorgängen nicht neu anordnen oder Lesevorgänge in Bezug auf andere Lesevorgänge neu anordnen, können Sie die Lesevorgänge relativ zu Schreibvorgängen umordnen. Insbesondere, wenn ein Programm auf einen Speicherort schreibt, gefolgt von einem Lesevorgang von einem anderen Speicherort, können die gelesenen Daten aus dem gemeinsam genutzten Speicher stammen, bevor Sie von den geschriebenen Daten erstellt werden. Diese Neuanordnung kann einige Algorithmen unterbrechen, wie z. b. die gegenseitigen Ausschluss Algorithmen von Dekker. In dem-Algorithmus von Dekker legt jeder Thread ein Flag fest, um anzugeben, dass der kritische Bereich eingegeben werden soll. Anschließend wird das Flag des anderen Threads überprüft, um festzustellen, ob sich der andere Thread in der kritischen Region befindet oder zu versuchen, ihn einzugeben. Der anfängliche Code folgt.

``` syntax
volatile bool f0 = false;
volatile bool f1 = false;

void P0Acquire()
{
    // Indicate intention to enter critical region
    f0 = true;
    // Check for other thread in or entering critical region
    while (f1)
    {
        // Handle contention.
    }
    // critical region
    ...
}


void P1Acquire()
{
    // Indicate intention to enter critical region
    f1 = true;
    // Check for other thread in or entering critical region
    while (f0)
    {
        // Handle contention.
    }
    // critical region
    ...
}
```

Das Problem besteht darin, dass der Lesevorgang von F1 in P0Acquire aus dem freigegebenen Speicher lesen kann, bevor der Schreibvorgang in F0 den freigegebenen Speicher ermöglicht. In der Zwischenzeit kann der Lesevorgang von F0 in P1Acquire aus dem freigegebenen Speicher lesen, bevor der Schreibvorgang in F1 den freigegebenen Speicher ermöglicht. Im Endeffekt legen beide Threads ihre Flags auf true fest, und beide Threads sehen das Flag des anderen Threads als false, sodass beide Threads in den kritischen Bereich gelangen. Obwohl Probleme mit der Neuanordnung von x86-und x64-Systemen weniger häufig sind als auf Xbox 360, können Sie auf jeden Fall weiterhin auftreten. Der-Algorithmus von Dekker funktioniert nicht ohne Hardware Speicherbarrieren auf diesen Plattformen.

x86-und x64-CPUs ordnen einen Schreibvorgang nicht vor einem vorherigen Lesevorgang neu an. x86-und x64-CPUs ordnen Lesevorgänge nur vor vorherigen Schreibvorgängen neu an, wenn Sie an unterschiedliche Positionen abzielen

PowerPC-CPUs können Lesevorgänge vor Schreibvorgängen neu anordnen und Schreibvorgänge vor Lesevorgängen neu anordnen, sofern Sie zu unterschiedlichen Adressen gehören.

### <a name="reordering-summary"></a>Zusammenfassung der Neuanordnung

Die Xbox 360-CPU ordnet Arbeitsspeicher Vorgänge weitaus aggressiver als x86-und x64-CPUs an, wie in der folgenden Tabelle dargestellt. Weitere Informationen finden Sie in der Prozessor Dokumentation.



| Neuanordnen von Aktivitäten           | x86 und x64 | Xbox 360 |
|-------------------------------|-------------|----------|
| Lesevorgänge vor Lesevorgängen   | Nein          | Ja      |
| Schreibvorgänge vor Schreibvorgängen | Nein          | Ja      |
| Schreibvorgänge vor Lesevorgängen  | Nein          | Ja      |
| Lesevorgänge vor Schreibvorgängen  | Ja         | Ja      |



 

## <a name="read-acquire-and-write-release-barriers"></a>Read-Acquire und Write-Release Barrieren

Die Hauptkonstrukte, die verwendet werden, um die Neuanordnung von Lese-und Schreibvorgängen zu verhindern, werden als Lese-und Freigabe Barrieren bezeichnet. Ein Lese-und Abruf Vorgang ist ein Lesevorgang eines Flags oder einer anderen Variablen, um den Besitz einer Ressource zu erhalten, gekoppelt mit einer Barriere gegen Neuanordnen. Ebenso ist ein Schreib Release ein Schreibvorgang eines Flags oder einer anderen Variablen, um den Besitz einer Ressource zu verkoppeln, gekoppelt mit einer Barriere gegen Neuanordnen.

Die formalen Definitionen (Courtesy of Herb Sutter) lauten wie folgt:

-   Ein Lese-/Abruf wird vor allen Lese-und Schreibvorgängen durch denselben Thread ausgeführt, der in der Programm Reihenfolge befolgt wird.
-   Ein Schreib Release wird ausgeführt, nachdem alle Lese-und Schreibvorgänge durch denselben Thread in der Programm Reihenfolge ausgeführt wurden.

Wenn Ihr Code den Besitz eines Speichers erhält, indem er entweder eine Sperre erhält oder ein Element aus einer freigegebenen verknüpften Liste (ohne Sperre) abruft, ist immer ein Lesevorgang beteiligt – das Testen eines Flags oder Zeigers, um festzustellen, ob der Besitz des Speichers abgerufen wurde. Dieser Lesevorgang kann Teil eines **interlockedxxx** -Vorgangs sein. in diesem Fall umfasst er sowohl einen Lese-als auch einen Schreibvorgang. er ist jedoch der Lesevorgang, der angibt, ob der Besitz gewonnen wurde. Nachdem der Besitz des Speichers abgerufen wurde, werden die Werte in der Regel aus dem Speicher gelesen oder in diesen geschrieben. es ist sehr wichtig, dass diese Lese-und Schreibvorgänge nach dem Erwerb des Besitzes ausgeführt werden. Dies wird durch eine Sperrgrenze gewährleistet.

Wenn der Besitz eines Speichers freigegeben wird, indem entweder eine Sperre freigegeben oder ein Element auf eine freigegebene verknüpfte Liste übertragen wird, ist immer ein Schreibvorgang beteiligt, der andere Threads benachrichtigt, dass Ihnen der Arbeitsspeicher jetzt zur Verfügung steht. Während Ihr Code den Besitz des Speichers besaß, wurde er wahrscheinlich von gelesen oder geschrieben, und es ist sehr wichtig, dass diese Lese-und Schreibvorgänge ausgeführt werden, bevor Sie den Besitz freigeben. Dies wird durch eine Barriere zum Schreiben von Releases sichergestellt.

Es ist am einfachsten, die Sperren von Lese-und Schreib Freigaben als einzelne Vorgänge zu betrachten. Manchmal müssen Sie jedoch aus zwei Teilen erstellt werden: ein Lese-oder Schreibvorgang und eine Barriere, bei der keine Lese-oder Schreibvorgänge über diese hinweg durchlaufen werden können. In diesem Fall ist die Platzierung der Barriere von entscheidender Bedeutung. Bei einer Barriere mit Lesezugriff wird zuerst der Lesevorgang des Flags, dann die Barriere und dann die Lese-und Schreibvorgänge für die freigegebenen Daten durchläuft. Bei einer Barriere mit Schreib Freigabe werden zunächst die Lese-und Schreibvorgänge der freigegebenen Daten, dann die Barriere und der Schreibvorgang des Flags angezeigt.

``` syntax
// Read that acquires the data.
if( g_flag )
{
    // Guarantee that the read of the flag executes before
    // all reads and writes that follow in program order.
    BarrierOfSomeSort();

    // Now we can read and write the shared data.
    int localVariable = sharedData.y;
    sharedData.x = 0;

    // Guarantee that the write to the flag executes after all
    // reads and writes that precede it in program order.
    BarrierOfSomeSort();
    
    // Write that releases the data.
    g_flag = false;
}
```

Der einzige Unterschied zwischen einem Lese-und einem Schreib Release ist der Speicherort der Arbeitsspeicher Barriere. Ein Lese-/Abruf weist die Barriere nach dem Sperr Vorgang auf, und ein Schreib Release weist die Barriere vor. In beiden Fällen befindet sich die Barriere zwischen den verweisen auf den gesperrten Arbeitsspeicher und den verweisen auf die Sperre.

Um zu verstehen, warum Barrieren sowohl beim Abrufen als auch beim Freigeben von Daten erforderlich sind, ist es am besten (und genauesten), diese Barrieren so zu betrachten, dass die Synchronisierung mit frei gegebenem Speicher, nicht mit anderen Prozessoren gewährleistet ist Wenn ein Prozessor ein Schreib Release verwendet, um eine Datenstruktur für den freigegebenen Arbeitsspeicher freizugeben, und ein anderer Prozessor einen Lese-/Abruf verwendet, um auf diese Datenstruktur aus dem freigegebenen Speicher zuzugreifen, funktioniert der Code ordnungsgemäß. Wenn einer der beiden Prozessoren nicht die geeignete Barriere verwendet, kann die Datenfreigabe fehlschlagen.

Die Verwendung der rechten Barriere, um zu verhindern, dass die kompieration von Compiler und CPU für Ihre Plattform entscheidend ist.

Einer der Vorteile der Verwendung der vom Betriebssystem bereitgestellten Synchronisierungs primitiven besteht darin, dass alle die entsprechenden Speicherbarrieren enthalten.

## <a name="preventing-compiler-reordering"></a>Verhindern der Neuanordnung von Compilers

Der Auftrag eines Compilers besteht darin, den Code aggressiv zu optimieren, um die Leistung zu verbessern. Dies umfasst auch das Anordnen von Anweisungen, wenn dies hilfreich ist und immer dann, wenn das Verhalten nicht geändert wird. Da der C++-Standard nie Multithreading erwähnt und der Compiler nicht weiß, welcher Code Thread sicher sein muss, geht der Compiler davon aus, dass der Code mit einem einzigen Thread versehen wird, wenn er entscheidet, welche Neuanordnungen er sicher ausführen kann. Daher müssen Sie den Compiler informieren, wenn es nicht zulässig ist, Lese-und Schreibvorgänge neu anzuordnen.

Mit Visual C++ Sie die Neuanordnung von Compilers mithilfe der systeminternen [**\_ compilerbarriere**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx)von "Compiler" verhindern. Wenn Sie "read- **\_ tebarrier** " in den Code einfügen, verschiebt der Compiler Lese-und Schreibvorgänge nicht über diesen.

``` syntax
#if _MSC_VER < 1400
    // With VC++ 2003 you need to declare _ReadWriteBarrier
    extern "C" void _ReadWriteBarrier();
#else
    // With VC++ 2005 you can get the declaration from intrin.h
#include <intrin.h>
#endif
// Tell the compiler that this is an intrinsic, not a function.
#pragma intrinsic(_ReadWriteBarrier)

// Create a new sprite by filling in a previously empty entry.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
// Write-release, barrier followed by write.
// Guarantee that the compiler leaves the write to the flag
// after all reads and writes that precede it in program order.
_ReadWriteBarrier();
g_sprites[nextSprite].alive = true;
```

Im folgenden Code liest ein anderer Thread aus dem Sprite-Array:

``` syntax
// Draw all sprites.
for( int i = 0; i < numSprites; ++i )
{

    // Read-acquire, read followed by barrier.
    if( g_sprites[nextSprite].alive )
    {
    
        // Guarantee that the compiler leaves the read of the flag
        // before all reads and writes that follow in program order.
        _ReadWriteBarrier();
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

Es ist wichtig zu verstehen, dass "read- [**\_ tebarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) " keine weiteren Anweisungen einfügt und nicht verhindert, dass die CPU Lese-und Schreibvorgänge neu anordnet – es wird lediglich verhindert, dass der Compiler Sie neu anordnet. Daher ist "Read-Write- **\_ Barriere** " ausreichend, wenn Sie eine Sperre für die Schreib Freigabe auf x86 und x64 implementieren (da x86 und x64 Schreibvorgänge nicht neu anordnen und ein normaler Schreibvorgang für die Freigabe einer Sperre ausreicht), aber in den meisten anderen Fällen ist es auch erforderlich, dass die CPU die Neuanordnung von Lese-und Schreibvorgängen verhindert.

Sie können auch "Read-Write- [**\_ Barrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) " verwenden, wenn Sie in einen nicht zwischen speicherbaren Schreib kombinierten Arbeitsspeicher schreiben, um die Neuanordnung von Schreibvorgängen zu verhindern In diesem Fall hilft "read **\_ Write** Items", die Leistung zu verbessern, indem sichergestellt wird, dass die Schreibvorgänge in der bevorzugten linearen Reihenfolge des Prozessors erfolgen

Es ist auch möglich, die Funktionen "read [**\_ Barrier**](https://msdn.microsoft.com/library/z055s48f(v=VS.80).aspx) " und " [**\_ Write Barrier**](https://msdn.microsoft.com/library/65tt87y8(v=VS.80).aspx) " zu verwenden, um die Neuanordnung des Compilers genauer zu steuern. Der Compiler verschiebt Lesevorgänge nicht über eine Read- **\_ Barriere**, und die Schreibvorgänge werden nicht über eine **\_ beschreibbare Barriere** verschoben.

## <a name="preventing-cpu-reordering"></a>Verhindern der CPU-Neuanordnung

Die erneute Reihenfolge der CPU-Reihenfolge ist besser als die erneute Reihenfolge Sie können nicht jemals sehen, dass es direkt passiert, Sie sehen nur unerklärliche Fehler. Um die CPU-Neuanordnung von Lese-und Schreibvorgängen zu verhindern, müssen Sie bei manchen Prozessoren arbeitsspeicherabgrenzungsanweisungen verwenden. Der Name der vollständig verwendbare Speicher Absperr Anweisung auf Xbox 360 und unter Windows ist [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier). Dieses Makro wird für jede Plattform Ordnungs entsprechend implementiert.

Auf Xbox 360 ist [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) als **lwsync** (Lightweight Sync) definiert, das auch über die systeminterne Funktion **\_ \_ lwsync** verfügbar ist, die in ppcintrinsics. h definiert ist. **\_ \_ lwsync** dient auch als compilerarbeitsspeicherbarriere, die das erneute Anordnen von Lese-und Schreibvorgängen durch den Compiler verhindert.

Die **lwsync** -Anweisung ist eine Arbeitsspeicher Barriere auf Xbox 360, die einen Prozessorkern mit dem L2-Cache synchronisiert. Dadurch wird sichergestellt, dass alle Schreibvorgänge vor **lwsync** vor den nachfolgenden Schreibvorgängen in den L2-Cache gestellt werden. Außerdem wird sichergestellt, dass bei Lesevorgängen, die **lwsync** folgen, keine älteren Daten von L2 als vorherige Lesevorgänge erhalten werden. Der einzige Typ der Neuanordnung, der nicht verhindert wird, ist ein Lesevorgang vor einem Schreibvorgang in eine andere Adresse. Folglich erzwingt **lwsync** eine Speicher Anordnung, die der Standard Arbeitsspeicher-Reihenfolge auf x86-und x64-Prozessoren entspricht. Um die vollständige Arbeitsspeicher-Reihenfolge zu erhalten, ist die kostengünstigere Synchronisierungs Anweisung (auch als "schwere Synchronisierung" bezeichnet) erforderlich In der folgenden Tabelle sind die Optionen für die Speicher Neuanordnung auf Xbox 360 aufgeführt.



| Neuanordnung von Xbox 360           | Keine Synchronisierung | lwsync | sync |
|-------------------------------|---------|--------|------|
| Lesevorgänge vor Lesevorgängen   | Ja     | Nein     | Nein   |
| Schreibvorgänge vor Schreibvorgängen | Ja     | Nein     | Nein   |
| Schreibvorgänge vor Lesevorgängen  | Ja     | Nein     | Nein   |
| Lesevorgänge vor Schreibvorgängen  | Ja     | Ja    | Nein   |



 

PowerPC verfügt auch über die Synchronisierungs Anweisungen **iSync** und **eieio** (die zum Steuern der Neuanordnen von zwischen speichertem Speicher verwendet werden). Diese Synchronisierungs Anweisungen sollten nicht für normale Synchronisierungs Zwecke benötigt werden.

Unter Windows ist [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) in "Winnt. h" definiert und gibt eine andere Speicher Absperr Anweisung aus, je nachdem, ob Sie für x86 oder x64 kompilieren. Die Speicher Abgrenzungs Anweisung dient als vollständige Barriere und verhindert die erneute Anordnung von Lese-und Schreibvorgängen über die Barriere hinweg. Daher bietet **MemoryBarrier** unter Windows eine stärkere neubestell Garantie als auf Xbox 360.

Auf Xbox 360 und vielen anderen CPUs gibt es eine zusätzliche Möglichkeit, dass die Lese-und Neuanordnung durch die CPU verhindert werden kann. Wenn Sie einen Zeiger lesen und dann diesen Zeiger zum Laden anderer Daten verwenden, gewährleistet die CPU, dass die Lesevorgänge des Zeigers nicht älter sind als das Lesen des Zeigers. Wenn das sperrenflag ein Zeiger ist und alle Lesevorgänge von freigegebenen Daten vom Zeiger entfernt sind, kann [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) weggelassen werden, um geringfügige Leistungs Einsparungen zu erzielen.

``` syntax
Data* localPointer = g_sharedPointer;
if( localPointer )
{
    // No import barrier is needed--all reads off of localPointer
    // are guaranteed to not be reordered past the read of
    // localPointer.
    int localVariable = localPointer->y;
    // A memory barrier is needed to stop the read of g_global
    // from being speculatively moved ahead of the read of
    // g_sharedPointer.
    int localVariable2 = g_global;
}
```

Die [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) -Anweisung verhindert nur das Neuanordnen von Lese-und Schreibvorgängen in den zwischen speicherbaren Speicher. Wenn Sie Arbeitsspeicher als "page \_ NoCache" oder "page \_ Beschreib tecombine" zuweisen, ist dies ein gängiges Verfahren für Gerätetreiber Autoren und Spieleentwickler auf Xbox 360. **MemoryBarrier** hat keine Auswirkung auf den Zugriff auf diesen Arbeitsspeicher. Die meisten Entwickler benötigen keine Synchronisierung des nicht zwischen speicherbaren Speichers. Dies geht jedoch über den Rahmen dieses Artikels hinaus.

## <a name="interlocked-functions-and-cpu-reordering"></a>Interlocked-Funktionen und CPU-Neuanordnung

Manchmal wird der Lese-oder Schreibvorgang, der eine Ressource übernimmt oder freigibt, mit einer der **interlockedxxx** -Funktionen durchgeführt. Unter Windows vereinfacht dies die Dinge. Da unter Windows die **interlockedxxx** -Funktionen alle vollständig im Arbeitsspeicher sind. Sie verfügen praktisch über eine CPU-Arbeitsspeicher Barriere vor und nach dem Arbeitsspeicher, was bedeutet, dass Sie eine vollständige Lese-oder Schreib Freigabe Barriere allein darstellen.

Auf Xbox 360 enthalten die **interlockedxxx** -Funktionen keine CPU-Speicherbarrieren. Sie verhindern die Neuanordnung von Lese-und Schreibvorgängen durch den Compiler, aber keine CPU-Neuanordnung Daher sollten Sie in den meisten Fällen, wenn Sie die Funktionen von **interlockedxxx** auf Xbox 360 verwenden, eine **\_ \_ lwsync** voranstellen oder diesen folgen, um Sie als Sperre für Lese-oder Schreib Freigabe festzulegen. Zur Vereinfachung und zur einfacheren **Lesbarkeit gibt es die Abruf-** und **Releaseversionen** vieler der **interlockedxxx** -Funktionen. Diese verfügen über eine integrierte Speicherbarriere. Beispielsweise führt [**interlockedinanmentabruf**](/previous-versions/windows/desktop/legacy/ms683618(v=vs.85)) eine Interlocked-Inkrement gefolgt von einer **\_ \_ lwsync** -Arbeitsspeicher Barriere aus, um die vollständige Funktionalität für den Lesezugriff zu erhalten.

Es wird empfohlen, dass Sie die **Abruf-und** **Releaseversionen** der **interlockedxxx** -Funktionen verwenden (die meisten unter Windows verfügbar sind, ohne Leistungseinbußen), um ihre Absicht deutlicher zu machen und die erforderlichen Speicher Absperr Anweisungen an der richtigen Stelle zu vereinfachen. Jede Verwendung von **interlockedxxx** auf Xbox 360 ohne eine Arbeitsspeicher Barriere sollte sehr sorgfältig untersucht werden, da es sich häufig um einen Fehler handelt.

In diesem Beispiel wird veranschaulicht, wie ein Thread Tasks oder andere Daten mithilfe der Erstellungs **-** und **Releaseversionen** der **interlockedxxxslist** -Funktionen an einen anderen Thread übergeben kann. Die **interlockedxxxslist** -Funktionen sind eine Reihe von Funktionen, mit denen eine freigegebene, einzeln verknüpfte Liste ohne Sperre verwaltet werden können. Beachten Sie **, dass die** Abruf-und **releasevarianten** dieser Funktionen unter Windows nicht verfügbar sind, aber die regulären Versionen dieser Funktionen sind unter Windows eine vollständige Arbeitsspeicher Barriere.

``` syntax
// Declarations for the Task class go here.

// Add a new task to the list using lockless programming.
void AddTask( DWORD ID, DWORD data )
{
    Task* newItem = new Task( ID, data );
    InterlockedPushEntrySListRelease( g_taskList, newItem );
}

// Remove a task from the list, using lockless programming.
// This will return NULL if there are no items in the list.
Task* GetTask()
{
    Task* result = (Task*)
        InterlockedPopEntrySListAcquire( g_taskList );
    return result;
}
```

## <a name="volatile-variables-and-reordering"></a>Flüchtige Variablen und Neuanordnen

Der C++-Standard besagt, dass Lesevorgänge flüchtiger Variablen nicht zwischengespeichert werden können, flüchtige Schreibvorgänge nicht verzögert werden können und flüchtige Lese-und Schreibvorgänge nicht aufeinander hin verschoben werden können. Dies ist für die Kommunikation mit Hardware Geräten ausreichend, was der Zweck des volatile-Schlüssel Worts im C++-Standard ist.

Allerdings reichen die Garantien des Standards nicht aus, um volatile für das Multithreading zu verwenden. Der C++-Standard hindert den Compiler nicht daran, nicht flüchtige Lese-und Schreibvorgänge relativ zu flüchtigen Lese-und Schreibvorgängen neu anzuordnen, und es wird nichts angezeigt, um die CPU-Neuanordnung zu verhindern.

Visual C++ 2005 überschreitet Standard C++, um Multithreading-freundliche Semantik für den flüchtigen Variablen Zugriff zu definieren. Ab Visual C++ 2005 werden Lesevorgänge aus flüchtigen Variablen als Semantik für den Lesezugriff definiert, und Schreibvorgänge in flüchtige Variablen sind so definiert, dass Sie über eine Semantik zur Schreib Freigabe verfügen. Dies bedeutet, dass der Compiler Lese-und Schreibvorgänge nicht neu anordnet und unter Windows sicherstellt, dass die CPU dies auch nicht tut.

Es ist wichtig zu verstehen, dass diese neuen Garantien nur für Visual C++ 2005 und zukünftige Versionen von Visual C++ gelten. Compiler von anderen Anbietern implementieren in der Regel eine andere Semantik, ohne dass die zusätzlichen Garantien Visual C++ 2005. Außerdem fügt der Compiler auf Xbox 360 keine Anweisungen ein, um zu verhindern, dass die CPU Lese-und Schreibvorgänge neu anordnet.

## <a name="example-of-a-lock-free-data-pipe"></a>Beispiel für eine Lock-Free Data Pipe

Eine Pipe ist ein Konstrukt, mit dem ein oder mehrere Threads Daten schreiben können, die dann von anderen Threads gelesen werden. Eine sperrenlose Version einer Pipe kann eine elegante und effiziente Möglichkeit sein, die Arbeit vom Thread an den Thread zu übergeben. Das DirectX SDK bietet **lockfrepipe**, eine locker-Sperre mit einem einzigen Lesezeichen, die in dxutlockfrepipe. h verfügbar ist. Die gleiche **lockfrepipe** ist im Xbox 360 SDK in atglockfrepipe. h verfügbar.

**Lockfrepipe** kann verwendet werden, wenn zwei Threads eine Producer/Consumer-Beziehung haben. Der Producer-Thread kann Daten in die Pipe schreiben, damit der Consumerthread zu einem späteren Zeitpunkt verarbeitet werden kann, ohne jemals blockieren zu müssen. Wenn die Pipe aufgefüllt wird, können Schreibvorgänge fehlschlagen, und der Producer-Thread muss den Vorgang später wiederholen. Dies geschieht jedoch nur, wenn der Producer-Thread voraus ist. Wenn der senkrechter Strich angezeigt wird, treten bei Lesevorgängen Fehler auf, und der Consumerthread muss den Vorgang später wiederholen. Dies geschieht jedoch nur dann, wenn es keine Arbeit für den Consumerthread gibt. Wenn die beiden Threads ausgeglichen sind und die Pipe groß genug ist, können Sie mit der Pipe problemlos Daten zusammen mit keinen Verzögerungen oder Blöcken übergeben.

## <a name="xbox-360-performance"></a>Leistung von Xbox 360

Die Leistung der Synchronisierungs Anweisungen und-Funktionen auf Xbox 360 variiert in Abhängigkeit davon, welche anderen Codes ausgeführt werden. Das Abrufen von Sperren dauert deutlich länger, wenn ein anderer Thread die Sperre zurzeit besitzt. [**Interlockedinkrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) -und Critical-Abschnitts Vorgänge dauern erheblich länger, wenn andere Threads in dieselbe Cache Zeile schreiben. Der Inhalt der Speicher Warteschlangen kann sich auch auf die Leistung auswirken. Daher sind all diese Zahlen nur Näherungen, die aus sehr einfachen Tests generiert werden:

-   **lwsync** wurde als 33-48 Zyklen gemessen.
-   Die [**interlockedinkrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) wurde als 225-260 Zyklen gemessen.
-   Das Abrufen oder Freigeben eines kritischen Abschnitts wurde als "ungefähr 345 Zyklen" gemessen.
-   Das Abrufen oder Freigeben eines Mutex wurde als Wert von ungefähr 2350 Zyklen gemessen.

## <a name="windows-performance"></a>Windows-Leistung

Die Leistung der Synchronisierungs Anweisungen und-Funktionen unter Windows variiert in Abhängigkeit vom Prozessortyp und der Konfiguration sowie davon, welcher anderer Code ausgeführt wird. Multicore-und multisocketsysteme beanspruchen häufig die Ausführung von Synchronisierungs Anweisungen länger, und das Abrufen von Sperren nimmt viel mehr Zeit in Anspruch, wenn ein anderer Thread die Sperre zurzeit besitzt.

Allerdings sind sogar einige von sehr einfachen Tests generierte Messungen hilfreich:

-   " [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) " wurde als 20-90 Zyklen gemessen.
-   Die [**interlockedinkrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) wurde als 36-90 Zyklen gemessen.
-   Das Abrufen oder Freigeben eines kritischen Abschnitts wurde als 40-100 Zyklen gemessen.
-   Das Abrufen oder Freigeben eines Mutex wurde als Wert von ungefähr 750-2500 Zyklen gemessen.

Diese Tests wurden unter Windows XP für eine Reihe von verschiedenen Prozessoren ausgeführt. Die kurzen Zeiten befanden sich auf einem Computer mit einem Prozessor, und die längeren Zeiten waren auf einem Computer mit mehreren Prozessoren.

Das Abrufen und Freigeben von Sperren ist zwar kostengünstiger als die Verwendung der sperrenlosen Programmierung, aber es ist noch besser, Daten seltener freizugeben und so die Kosten vollständig zu vermeiden.

## <a name="performance-thoughts"></a>Leistungsgedanken

Das Abrufen oder Freigeben eines kritischen Abschnitts besteht aus einer Speicherbarriere, einem **interlockedxxx** -Vorgang und einigen zusätzlichen Überprüfungen, um die Rekursion zu verarbeiten und ggf. auf einen Mutex zurückzugreifen. Sie sollten sich mit der Implementierung Ihres eigenen kritischen Abschnitts aushüten, da das Drehen in einer Schleife, die auf eine Sperre wartet, ohne zurück auf einen Mutex, eine beträchtliche Leistung verschwendet. Bei kritischen Abschnitten, die stark in Konflikt stehen, aber nicht lange aufbewahrt werden, sollten Sie die Verwendung von " [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) " in Erwägung gezogen, damit das Betriebssystem für einen spinnt, während darauf gewartet wird, dass der kritische Abschnitt verfügbar ist, und wenn der kritische Abschnitt im Besitz des Versuchs ist. Um wichtige Abschnitte zu identifizieren, die von einer Spin-Anzahl profitieren können, ist es erforderlich, die Länge der typischen Wartezeit auf eine bestimmte Sperre zu messen.

Wenn ein frei gegebener Heap für Speicher Belegungen verwendet wird – das Standardverhalten – erfordert jede Speicher Belegung und jede freie Sperre das Abrufen einer Sperre. Wenn die Anzahl der Threads und die Anzahl der Zuordnungen zunimmt, wird die Leistungsstufe deaktiviert und schließlich verringert. Durch die Verwendung von Thread spezifischen Heaps oder das Verringern der Anzahl von Zuordnungen kann dieser Sperr Engpass vermieden werden.

Wenn ein Thread Daten erzeugt und ein anderer Thread Daten beansprucht, werden diese möglicherweise häufig Daten gemeinsam nutzen. Dies kann vorkommen, wenn ein Thread Ressourcen lädt und ein anderer Thread die Szene rendert. Wenn der Renderingthread auf die freigegebenen Daten bei jedem Zeichnen-Befehl verweist, ist der Sperr Aufwand hoch. Eine viel bessere Leistung kann erreicht werden, wenn jeder Thread über private Datenstrukturen verfügt, die dann einmal pro Frame oder weniger synchronisiert werden.

Sperr lose Algorithmen sind nicht garantiert schneller als Algorithmen, die Sperren verwenden. Sie sollten überprüfen, ob Sperren tatsächlich Probleme verursachen, bevor Sie versuchen, Sie zu vermeiden, und Sie sollten Messen, ob der sperrenfreie Code tatsächlich die Leistung verbessert.

## <a name="platform-differences-summary"></a>Übersicht über Platt Form Unterschiede

-   **Interlockedxxx** -Funktionen verhindern eine Neuanordnung der CPU-Lese-/Schreibvorgänge unter Windows, nicht jedoch auf Xbox 360.
-   Das Lesen und Schreiben von flüchtigen Variablen mithilfe von Visual Studio C++ 2005 verhindert eine Neuanordnung der CPU-Lese-/Schreibvorgänge unter 360 Windows
-   Schreibvorgänge werden auf Xbox 360 neu angeordnet, jedoch nicht auf x86 oder x64.
-   Lesevorgänge werden auf Xbox 360 neu angeordnet, aber auf x86-oder x64-Daten werden Sie nur relativ zu Schreibvorgängen neu angeordnet, und nur, wenn die Lese-und Schreibvorgänge an unterschiedliche Speicherorte richten

## <a name="recommendations"></a>Empfehlungen

-   Verwenden Sie sperren, wenn möglich, da Sie leichter zu verwenden sind.
-   Vermeiden Sie eine zu häufige Sperre, sodass Sperrkosten nicht signifikant werden.
-   Vermeiden Sie eine zu lange Sperre, um lange Stände zu vermeiden.
-   Verwenden Sie ggf. die unlocklose Programmierung, aber stellen Sie sicher, dass die Vorteile die Komplexität rechtfertigen.
-   Verwenden Sie lockless Programming oder Spin Locks in Situationen, in denen andere Sperren nicht zulässig sind, z. b. bei der Freigabe von Daten zwischen verzögerten Prozedur aufrufen und normalem Code.
-   Verwenden Sie nur die standardmäßigen Sperr losen Programmierungs Algorithmen, die als richtig erwiesen wurden.
-   Achten Sie bei der sperlocklosen Programmierung darauf, dass Sie bei Bedarf flüchtige Flagvariablen und Speicher Abgrenzungs Anweisungen verwenden.
-   Wenn Sie **interlockedxxx** auf Xbox 360 verwenden, verwenden **Sie die Abruf** -und **releasevarianten** .

## <a name="references"></a>References

-   MSDN Library. "[**volatile (C++)**](https://msdn.microsoft.com/library/12a04hfd(v=VS.71).aspx)". C++-Sprachreferenz.
-   Vance Morrison. "[Verstehen der Auswirkungen von Low-Lock Techniken in Multithread-apps](/archive/msdn-magazine/2005/october/understanding-low-lock-techniques-in-multithreaded-apps)." MSDN Magazine, Oktober 2005.
-   Lyons, Michael. "[PowerPC-Speichermodell und AIX-Programmierung](https://www-128.ibm.com/developerworks/eserver/articles/powerpc.mdl)". IBM developerworks, 16. Nov., 2005.
-   McKenney, Paul E. "Arbeits[Speicher Anordnung in modernen Mikroprozessoren, Teil II](https://www.linuxjournal.com/article/8212)." Linux-Journal, September 2005. \[In diesem Artikel sind einige x86-Details aufgeführt.\]
-   Intel Corporation. "[Intel® 64-Architektur Arbeitsspeicher-Reihen](https://www.cs.cmu.edu/~410-f10/doc/Intel_Reordering_318147.pdf)Folge." 2007. August. \[Gilt sowohl für IA-32-als auch für Intel 64-Prozessoren.\]
-   Niebler, Eric. "[Trip Report: Ad-hoc Meeting on Threads in C++](https://www.artima.com/cppsource/threads_meeting.html)". Die C++-Quelle, 17. Okt, 2006.
-   Hart, Thomas E. 2006. "[Schnelles Sperren der Synchronisierung: Leistungseinbußen bei der Arbeitsspeicher Rückgewinnung](https://www.cs.toronto.edu/~tomhart/papers/hart_ipdps06.pdf)". Der Prozess des 2006 International Parallel and verteilte processing-Symposiums (IPDPS 2006), der Rhodos-Insel, Griechenland, April 2006.

 

 