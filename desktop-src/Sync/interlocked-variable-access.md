---
description: Anwendungen müssen den Zugriff auf Variablen synchronisieren, die von mehreren Threads gemeinsam genutzt werden.
ms.assetid: 729c0e68-ef52-4d6c-b771-a89043a937e6
title: Interlocked Variable Access
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b298dffe45d1a0de655e225c8a240dd72be15a0fff7e4d6eac25ebb0a1130ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126320"
---
# <a name="interlocked-variable-access"></a>Interlocked Variable Access

Anwendungen müssen den Zugriff auf Variablen synchronisieren, die von mehreren Threads gemeinsam genutzt werden. Anwendungen müssen auch sicherstellen, dass Vorgänge für diese Variablen atomisch (vollständig oder gar nicht) ausgeführt werden.

Einfache Lese- und Schreibvorgänge in ordnungsgemäß ausgerichtete 32-Bit-Variablen sind atomare Vorgänge. Anders ausgedrückt: Am Ende wird nicht nur ein Teil der Variablen aktualisiert. alle Bits werden atomar aktualisiert. Es ist jedoch nicht garantiert, dass der Zugriff synchronisiert wird. Wenn zwei Threads aus derselben Variablen lesen und schreiben, können Sie nicht bestimmen, ob ein Thread seinen Lesevorgang ausführt, bevor der andere den Schreibvorgang ausführt.

Einfache Lese- und Schreibvorgänge in ordnungsgemäß ausgerichtete 64-Bit-Variablen sind atomar auf 64-Bit-Windows. Lese- und Schreibvorgänge in 64-Bit-Werte sind nicht garantiert atomar auf 32-Bit-Windows. Lese- und Schreibvorgänge in Variablen anderer Größen sind auf einer Plattform nicht garantiert atomar.

## <a name="the-interlocked-api"></a>Die Interlocked-API

Die ineinandergreifenden Funktionen bieten einen einfachen Mechanismus zum Synchronisieren des Zugriffs auf eine Variable, die von mehreren Threads gemeinsam genutzt wird. Sie führen auch Vorgänge für Variablen atomar aus. Die Threads verschiedener Prozesse können diese Funktionen verwenden, wenn sich die Variable im freigegebenen Arbeitsspeicher befindet.

Die [**Funktionen InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) und [**InterlockedDecrement**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement) kombinieren die Schritte zum Erhöhen oder Dekrementen einer Variablen in einem atomaren Vorgang. Dieses Feature ist in einem Multitaskingbetriebssystem nützlich, bei dem das System die Ausführung eines Threads unterbrechen kann, um einem anderen Thread einen Teil der Prozessorzeit zu gewähren. Ohne eine solche Synchronisierung könnten zwei Threads den gleichen Wert lesen, ihn um 1 erhöhen und den neuen Wert für eine Gesamterhöhung von 1 anstelle von 2 speichern. Die ineinandergreifenden Variablenzugriffsfunktionen schützen vor dieser Art von Fehler.

Die [**Funktionen InterlockedExchange**](/windows/win32/api/winnt/nf-winnt-interlockedexchange) und [**InterlockedExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer) tauschen atomisch die Werte der angegebenen Variablen aus. Die [**InterlockedExchangeAdd-Funktion**](/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd) kombiniert zwei Vorgänge: das Hinzufügen von zwei Variablen und das Speichern des Ergebnisses in einer der Variablen.

Die [**Funktionen InterlockedCompareExchange,**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange) [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))und [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) kombinieren zwei Vorgänge: das Vergleichen von zwei Werten und das Speichern eines dritten Werts in einer der Variablen basierend auf dem Ergebnis des Vergleichs.

Die [**InterlockedAnd-,**](/windows/win32/api/winnt/nf-winnt-interlockedand) [**InterlockedOr-**](/windows/win32/api/winnt/nf-winnt-interlockedor)und [**InterlockedXor-Funktionen**](/windows/win32/api/winnt/nf-winnt-interlockedxor) führen DIE- bzw. OR- bzw. XOR-Vorgänge atomisch aus.

Es gibt Funktionen, die speziell für den Interlocked Variable-Zugriff auf 64-Bit-Speicherwerte und -Adressen konzipiert sind und für die Verwendung auf 64-Bit-Windows. Jede dieser Funktionen enthält "64" im Namen. Beispiel: [**InterlockedDecrement64**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement64) und [**InterlockedCompareExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683566(v=vs.85)).

Die meisten der ineinandergreifenden Funktionen bieten vollständige Speicherbarrieren auf allen Windows Plattformen. Es gibt auch Funktionen, die die grundlegenden Interlocked-Variablenzugriffsvorgänge mit der Semantik zum Erwerben und Veröffentlichen der Speicher reihenfolge kombinieren, die von bestimmten Prozessoren unterstützt wird. Jede dieser Funktionen enthält das Wort "Acquire" oder "Release" in ihren Namen. Beispiel: [**InterlockedDecrementAcquire**](/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)) und [**InterlockedDecrementRelease.**](/previous-versions/windows/desktop/legacy/ms683586(v=vs.85)) Speichersemantik erwerben gibt an, dass der vom aktuellen Thread ausgeführte Speichervorgang sichtbar ist, bevor andere Speichervorgänge versucht werden. Die Semantik des Freigabespeichers gibt an, dass der vom aktuellen Thread ausgeführte Speichervorgang sichtbar ist, nachdem alle anderen Speichervorgänge abgeschlossen wurden. Mit dieser Semantik können Sie erzwingen, dass Speichervorgänge in einer bestimmten Reihenfolge ausgeführt werden. Verwenden Sie die Acquire-Semantik, wenn Sie einen geschützten Bereich eingeben, und geben Sie semantische Daten frei, wenn Sie ihn verlassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Intrinsische Compilerfunktionen](/cpp/intrinsics/compiler-intrinsics?view=vs-2019)
</dt> <dt>

[Synchronisierungs- und Multiprozessorprobleme](synchronization-and-multiprocessor-issues.md)
</dt> </dl>

 

 
