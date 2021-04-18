---
description: Bei Anwendungen können Probleme auftreten, wenn Sie auf Multiprozessorsystemen ausgeführt werden. Dies trifft auf Annahmen zu, die nur für Systeme mit nur einem Prozessor gültig sind.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Synchronisierungs- und Multiprozessorprobleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106361094"
---
# <a name="synchronization-and-multiprocessor-issues"></a>Synchronisierungs- und Multiprozessorprobleme

Bei Anwendungen können Probleme auftreten, wenn Sie auf Multiprozessorsystemen ausgeführt werden. Dies trifft auf Annahmen zu, die nur für Systeme mit nur einem Prozessor gültig sind.

## <a name="thread-priorities"></a>Threadprioritäten

Stellen Sie sich ein Programm mit zwei Threads vor, eine mit einer höheren Priorität als die andere. Bei einem System mit einem einzelnen Prozessor übergibt der Thread mit höherer Priorität die Steuerung nicht an den Thread mit niedrigerer Priorität, da der Scheduler die Threads mit höherer Priorität bevorzugt. Auf einem Multiprozessorsystem können beide Threads gleichzeitig ausgeführt werden, jeweils auf dem eigenen Prozessor.

Anwendungen sollten den Zugriff auf Datenstrukturen synchronisieren, um Racebedingungen zu vermeiden. Code, der davon ausgeht, dass Threads mit höherer Priorität ohne Störungen von Threads mit niedrigerer Priorität ausgeführt werden, schlagen auf Multiprozessorsystemen fehl

## <a name="memory-ordering"></a>Speicher Anordnung

Wenn ein Prozessor in einen Speicherort schreibt, wird der Wert zwischengespeichert, um die Leistung zu verbessern. Ebenso versucht der Prozessor, Lese Anforderungen aus dem Cache zu erfüllen, um die Leistung zu verbessern. Außerdem beginnen Prozessoren mit dem Abrufen von Werten aus dem Arbeitsspeicher, bevor Sie von der Anwendung angefordert werden. Dies kann als Teil der spekulativen Ausführung oder aufgrund von Cache Zeilen Problemen auftreten.

CPU-Caches können in Banken partitioniert werden, auf die gleichzeitig zugegriffen werden kann. Dies bedeutet, dass Speichervorgänge außerhalb der Reihenfolge abgeschlossen werden können. Um sicherzustellen, dass Speichervorgänge in der richtigen Reihenfolge abgeschlossen werden, stellen die meisten Prozessoren Speicher Absperr Anweisungen bereit. Eine *vollständige Speicherbarriere* stellt sicher, dass Arbeitsspeicher Lese-und-Schreibvorgänge, die vor der Speicher Abbild Anweisung angezeigt werden, vor Lese-und Schreibvorgängen im Arbeitsspeicher, die nach der Speicher Abbild Anweisung angezeigt werden, Eine *Lese Speicherbarriere* ordnet nur die Speicher Lesevorgänge zu, und eine *Schreib Speicherbarriere* ordnet nur die Speicher Schreibvorgänge an. Diese Anweisungen stellen außerdem sicher, dass der Compiler alle Optimierungen deaktiviert, die Arbeitsspeicher Vorgänge über die Barrieren hinweg neu anordnen können.

Prozessoren können Anweisungen für Speicherbarrieren mit Abruf-, Release-und Fence Semantik unterstützen. Diese Semantik beschreibt die Reihenfolge, in der die Ergebnisse eines Vorgangs verfügbar werden. Bei der Semantik zum Abrufen sind die Ergebnisse des Vorgangs vor den Ergebnissen eines beliebigen Vorgangs verfügbar, der im Code angezeigt wird. Bei der releasesemantik sind die Ergebnisse des Vorgangs nach den Ergebnissen eines beliebigen Vorgangs verfügbar, der im Code vor ihm angezeigt wird. Die Fence-Semantik kombiniert die Semantik zum Abrufen und freigeben. Die Ergebnisse eines Vorgangs mit der Fence-Semantik sind vor den Vorgängen eines beliebigen Vorgangs verfügbar, der im Code nach dem Vorgang angezeigt wird, und nach dem eines beliebigen Vorgangs, der vor ihm angezeigt wird.

Auf x86-und x64-Prozessoren, die SSE2 unterstützen, sind die Anweisungen **mfence** (arbeitsspeicherfence), **lfence** (Load Fence) und **sfence** (Store Fence). Bei ARM-Prozessoren sind die instrumentierten **DMB** und **DSB**. Weitere Informationen finden Sie in der Dokumentation für den Prozessor.

Die folgenden Synchronisierungs Funktionen verwenden die entsprechenden Barrieren, um die Arbeitsspeicher Anordnung sicherzustellen:

-   Funktionen, die kritische Abschnitte eingeben oder verlassen
-   Funktionen, die SRW-Sperren abrufen oder freigeben
-   Einmalige Initialisierung beginnt und Fertigstellung
-   **Entersynchronizationbarrier** -Funktion
-   Funktionen, die Synchronisierungs Objekten signalisieren
-   Wait-Funktionen
-   Interlocked-Funktionen (außer Funktionen mit einem _nofence_ -Suffix oder intrinsie mit dem _\_ NF_ -Suffix)

## <a name="fixing-a-race-condition"></a>Reparieren einer Racebedingung

Der folgende Code hat eine Racebedingung auf einem Multiprozessorsystem, da der Prozessor, `CacheComputedValue` der zum ersten Mal ausgeführt wird, in den Hauptspeicher schreiben kann, `fValueHasBeenComputed` bevor er `iValue` in den Hauptspeicher geschrieben wird. Folglich liest ein zweiter Prozessor, der `FetchComputedValue` gleichzeitig ausgeführt wird `fValueHasBeenComputed` , **true**, aber der neue Wert von `iValue` befindet sich noch im Cache des ersten Prozessors und wurde nicht in den Arbeitsspeicher geschrieben.

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

Diese Racebedingung oben kann mithilfe des **volatile** -Schlüssel Worts oder der [**interlockedexchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) -Funktion repariert werden, um sicherzustellen, dass der Wert von `iValue` für alle Prozessoren aktualisiert wird, bevor der Wert von `fValueHasBeenComputed` auf **true** festgelegt wird.

Beim Starten von Visual Studio 2005 verwendet der Compiler bei der Kompilierung im **/volatile: ms** -Modus die erfassten Semantik für Lesevorgänge für **flüchtige** Variablen und releasesemantik für Schreibvorgänge für **flüchtige** Variablen (sofern von der CPU unterstützt). Aus diesem Grund können Sie das Beispiel wie folgt korrigieren:

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

Mit Visual Studio 2003 werden **flüchtige** und **flüchtige** Verweise angeordnet. der Compiler wird den Zugriff auf **flüchtige** Variablen nicht neu anordnen. Diese Vorgänge können jedoch vom Prozessor neu angeordnet werden. Aus diesem Grund können Sie das Beispiel wie folgt korrigieren:

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

[Kritische Abschnitts Objekte](critical-section-objects.md)
</dt> <dt>

[Interlocked-Variablen Zugriff](interlocked-variable-access.md)
</dt> <dt>

[Wait-Funktionen](wait-functions.md)
</dt> </dl>

 

 



