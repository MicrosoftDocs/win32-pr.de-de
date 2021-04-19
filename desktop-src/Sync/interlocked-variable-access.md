---
description: Anwendungen müssen den Zugriff auf Variablen synchronisieren, die von mehreren Threads gemeinsam genutzt werden.
ms.assetid: 729c0e68-ef52-4d6c-b771-a89043a937e6
title: Interlocked-Variablen Zugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2e083d3e3420e870ad9781b0d262df3d0786f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363618"
---
# <a name="interlocked-variable-access"></a>Interlocked-Variablen Zugriff

Anwendungen müssen den Zugriff auf Variablen synchronisieren, die von mehreren Threads gemeinsam genutzt werden. Anwendungen müssen außerdem sicherstellen, dass Vorgänge für diese Variablen atomisch ausgeführt werden (vollständig oder überhaupt nicht ausgeführt werden).

Einfache Lese-und Schreibvorgänge für ordnungsgemäß ausgerichtete 32-Bit-Variablen sind atomarische Vorgänge. Dies bedeutet, dass Sie nicht nur einen Teil der Variablen aktualisiert haben. alle Bits werden atomarisch aktualisiert. Es ist jedoch nicht gewährleistet, dass der Zugriff synchronisiert wird. Wenn zwei Threads die gleiche Variable Lesen und schreiben, können Sie nicht feststellen, ob ein Thread seinen Lesevorgang ausführt, bevor der andere den Schreibvorgang ausführt.

Einfache Lese-und Schreibvorgänge für ordnungsgemäß ausgerichtete 64-Bit-Variablen sind atomarisch auf 64-Bit-Fenstern. Lese-und Schreibvorgänge in 64-Bit-Werten sind nicht garantiert atomarisch auf 32-Bit-Fenstern. Lese-und Schreibvorgänge für Variablen anderer Größen sind nicht unbedingt atomarisch auf einer beliebigen Plattform.

## <a name="the-interlocked-api"></a>Die Interlocked-API

Die Interlocked-Funktionen bieten einen einfachen Mechanismus für die Synchronisierung des Zugriffs auf eine Variable, die von mehreren Threads gemeinsam genutzt wird. Außerdem führen Sie Vorgänge für Variablen atomarisch aus. Die Threads verschiedener Prozesse können diese Funktionen verwenden, wenn sich die Variable im gemeinsam genutzten Speicher befindet.

Die Funktionen [**interlockedinkrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) und [**InterlockedDecrement**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement) kombinieren die Schritte zum Inkrementieren oder Dekrementieren einer Variablen in einen atomaren Vorgang. Diese Funktion ist in einem Multitasking-Betriebssystem nützlich, bei dem das System die Ausführung eines Threads unterbrechen kann, um einem anderen Thread einen Slice der Prozessorzeit zu gewähren. Ohne diese Synchronisierung können zwei Threads denselben Wert lesen, den Wert um 1 erhöhen und den neuen Wert für eine Gesamterhöhung von 1 anstelle von 2 speichern. Die Interlocked-Variablen Zugriffs Funktionen schützen gegen diese Art von Fehler.

Die [**interlockedexchange**](/windows/win32/api/winnt/nf-winnt-interlockedexchange) -Funktion und die [**interlockedexchangepointer**](/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer) -Funktion tauschen die Werte der angegebenen Variablen atomisch aus. Die [**interlockedexchangeadd**](/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd) -Funktion kombiniert zwei Vorgänge: das Hinzufügen von zwei Variablen und das Speichern des Ergebnisses in einer der Variablen.

Die Funktionen [**interlockedcompareexchange**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange), [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))und [**interlockedcompareexchangepointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) kombinieren zwei Vorgänge: Vergleichen von zwei Werten und Speichern eines dritten Werts in einer der Variablen, basierend auf dem Ergebnis des Vergleichs.

Die Funktionen [**interlockedand**](/windows/win32/api/winnt/nf-winnt-interlockedand), [**interlockedor**](/windows/win32/api/winnt/nf-winnt-interlockedor)und [**interlockedxor**](/windows/win32/api/winnt/nf-winnt-interlockedxor) führen atomarisch und bzw. bzw. bzw. Xor-Vorgänge aus.

Es gibt Funktionen, die speziell für die Ausführung von Interlocked-Variablen Zugriff auf 64-Bit-Speicher Werte und-Adressen entwickelt wurden und für die Verwendung auf 64-Bit-Fenstern optimiert sind. Jede dieser Funktionen enthält "64" im Namen; beispielsweise [**InterlockedDecrement64**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement64) und [**InterlockedCompareExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683566(v=vs.85)).

Die meisten der Interlocked-Funktionen stellen vollständige Speicherbarrieren auf allen Windows-Plattformen bereit. Es gibt auch Funktionen, die die grundlegenden Interlocked-Variablen Zugriffs Vorgänge mit der von bestimmten Prozessoren unterstützten Speicher Bestell Semantik für die Erfassung und Freigabe kombinieren. Jede dieser Funktionen enthält das Wort "abrufen" oder "Release" in ihren Namen. beispielsweise [**interlockeddecrementpick**](/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)) und [**interlockeddecrementrelease**](/previous-versions/windows/desktop/legacy/ms683586(v=vs.85)). Speicher Semantik abrufen gibt an, dass der Arbeitsspeicher Vorgang, der vom aktuellen Thread ausgeführt wird, sichtbar ist, bevor andere Speichervorgänge versucht werden. Die Semantik des releasespeichers gibt an, dass der Arbeitsspeicher Vorgang, der vom aktuellen Thread ausgeführt wird, sichtbar ist, nachdem alle anderen Speichervorgänge abgeschlossen wurden. Diese Semantik ermöglicht es Ihnen, Speichervorgänge in einer bestimmten Reihenfolge durchzuführen. Verwenden Sie die Semantik zum Abrufen bei der Eingabe einer geschützten Region und releasesemantik, wenn Sie Sie verlässt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Intrinsische Compilerfunktionen](/cpp/intrinsics/compiler-intrinsics?view=vs-2019)
</dt> <dt>

[Synchronisierungs- und Multiprozessorprobleme](synchronization-and-multiprocessor-issues.md)
</dt> </dl>

 

 
