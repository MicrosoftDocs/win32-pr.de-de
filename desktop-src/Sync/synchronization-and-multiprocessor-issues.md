---
description: Anwendungen können probleme auftreten, wenn sie auf Multiprozessorsystemen ausgeführt werden, da sie Annahmen treffen, die nur für Einzelprozessorsysteme gültig sind.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Synchronisierungs- und Multiprozessorprobleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0e86a2c69cf0a0c0e56656475f73fb489f7433a94511703b3777302702bb32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886208"
---
# <a name="synchronization-and-multiprocessor-issues"></a>Synchronisierungs- und Multiprozessorprobleme

Anwendungen können probleme auftreten, wenn sie auf Multiprozessorsystemen ausgeführt werden, da sie Annahmen treffen, die nur für Einzelprozessorsysteme gültig sind.

## <a name="thread-priorities"></a>Threadprioritäten

Betrachten Sie ein Programm mit zwei Threads, eines mit einer höheren Priorität als der andere. In einem Einzelprozessorsystem gibt der Thread mit höherer Priorität die Kontrolle nicht an den Thread mit niedrigerer Priorität ab, da der Scheduler Threads mit höherer Priorität den Vorrang gibt. Auf einem Multiprozessorsystem können beide Threads gleichzeitig ausgeführt werden, jeweils auf einem eigenen Prozessor.

Anwendungen sollten den Zugriff auf Datenstrukturen synchronisieren, um Racebedingungen zu vermeiden. Code, der annimmt, dass Threads mit höherer Priorität ohne Beeinträchtigung durch Threads mit niedrigerer Priorität ausgeführt werden, schlägt auf Multiprozessorsystemen fehl.

## <a name="memory-ordering"></a>Speicherreihenfolge

Wenn ein Prozessor an eine Speicherposition schreibt, wird der Wert zwischengespeichert, um die Leistung zu verbessern. Auf ähnliche Weise versucht der Prozessor, Leseanforderungen aus dem Cache zu erfüllen, um die Leistung zu verbessern. Darüber hinaus beginnen Prozessoren damit, Werte aus dem Arbeitsspeicher abzurufen, bevor sie von der Anwendung angefordert werden. Dies kann im Rahmen der spekulativen Ausführung oder aufgrund von Cachezeilenproblemen auftreten.

CPU-Caches können in Banken partitioniert werden, auf die parallel zugegriffen werden kann. Dies bedeutet, dass Speichervorgänge in nicht ordnungsgemäßer Reihenfolge abgeschlossen werden können. Um sicherzustellen, dass Speichervorgänge in der reihenfolge abgeschlossen werden, stellen die meisten Prozessoren Anweisungen zur Speicherbarriere bereit. Eine *vollständige Speicherbarriere* stellt sicher, dass Lese- und Schreibvorgänge im Arbeitsspeicher, die vor der Speicherbarrierenanweisung auftreten, in den Arbeitsspeicher übergeben werden, bevor Speicherlese- und Schreibvorgänge ausgeführt werden, die nach der Speicherbarrierenanweisung auftreten. Eine *Lesespeicherbarriere* ordnet nur die Speicherlesevorgänge und eine *Schreibspeicherbarriere* nur die Speicherschreibvorgänge an. Diese Anweisungen stellen außerdem sicher, dass der Compiler alle Optimierungen deaktiviert, die Speichervorgänge über die Barrieren hinweg neu anordnen könnten.

Prozessoren können Anweisungen für Speicherbarrieren mit semantischer Erfassung, Freigabe und Umgrenzung unterstützen. Diese Semantik beschreibt die Reihenfolge, in der Ergebnisse eines Vorgangs verfügbar werden. Mit der Semantik "acquire" sind die Ergebnisse des Vorgangs vor den Ergebnissen eines Vorgangs verfügbar, der im Code nach ihm angezeigt wird. Mit der Releasesemantik sind die Ergebnisse des Vorgangs nach den Ergebnissen eines Vorgangs verfügbar, der im Code vor ihm angezeigt wird. Fence-Semantik kombiniert die Semantik zum Abrufen und Freigeben. Die Ergebnisse eines Vorgangs mit Fence-Semantik sind vor den Ergebnissen eines Vorgangs verfügbar, der im Code nach ihm und nach den Ergebnissen eines vorgangs vor ihm angezeigt wird.

Auf x86- und x64-Prozessoren, die SSE2 unterstützen, sind die Anweisungen **Mfence** (Speicherfäufelung), **Lfence** (Ladezaun) und **Sfence** (Store Fence). Bei ARM-Prozessoren sind die Eindringungen **dmb** und **dsb.** Weitere Informationen finden Sie in der Dokumentation für den Prozessor.

Die folgenden Synchronisierungsfunktionen verwenden die entsprechenden Barrieren, um die Speicherreihenfolge sicherzustellen:

-   Funktionen, die kritische Abschnitte eingeben oder verlassen
-   Funktionen, die SRW-Sperren abrufen oder freigeben
-   Einmaliger Initialisierungsbeginn und -abschluss
-   **EnterSynchronizationBarrier-Funktion**
-   Funktionen, die Synchronisierungsobjekte signalisieren
-   Wartefunktionen
-   Interlocked-Funktionen (mit Ausnahme von Funktionen mit _dem NoFence-Suffix_ oder systeminterne Funktionen mit _\_ nf-Suffix)_

## <a name="fixing-a-race-condition"></a>Beheben einer Racebedingung

Der folgende Code weist eine Racebedingung auf einem Multiprozessorsystem auf, da der Prozessor, der zum ersten Mal ausgeführt wird, `CacheComputedValue` möglicherweise in den Hauptspeicher schreiben kann, `fValueHasBeenComputed` bevor er in den `iValue` Hauptspeicher schreibt. Folglich liest ein zweiter Prozessor, der gleichzeitig ausgeführt wird, `FetchComputedValue` `fValueHasBeenComputed` als **TRUE,** aber der neue Wert von befindet sich noch im Cache `iValue` des ersten Prozessors und wurde nicht in den Arbeitsspeicher geschrieben.

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

Diese Racebedingung oben kann mithilfe  des volatile-Schlüsselworts oder der [**InterlockedExchange-Funktion**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) repariert werden, um sicherzustellen, dass der Wert von `iValue` für alle Prozessoren aktualisiert wird, bevor der Wert von `fValueHasBeenComputed` auf **TRUE** festgelegt wird.

Ab Visual Studio 2005 verwendet der Compiler bei Kompilierung im **Modus /volatile:ms** die Semantik zum Abrufen von Lesevorgängen für **flüchtige** Variablen und die Releasesemantik für Schreibvorgänge **für flüchtige** Variablen (sofern von der CPU unterstützt). Daher können Sie das Beispiel wie folgt korrigieren:

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

Mit Visual Studio 2003 werden **flüchtige** auf **flüchtige** Verweise sortiert. Der Compiler ordnen den Zugriff auf **flüchtige** Variablen nicht neu an. Diese Vorgänge können jedoch vom Prozessor neu sortiert werden. Daher können Sie das Beispiel wie folgt korrigieren:

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kritische Abschnittsobjekte](critical-section-objects.md)
</dt> <dt>

[Interlocked Variable Access](interlocked-variable-access.md)
</dt> <dt>

[Wait-Funktionen](wait-functions.md)
</dt> </dl>

 

 



