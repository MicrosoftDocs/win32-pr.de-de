---
description: Obwohl Anbietern empfohlen wird, eindeutige Instanznamen zu verwenden, ist dies nicht bei allen Anbietern der Fall.
ms.assetid: 3c8fcb8d-2ea4-4b24-b649-7bd375c1133d
title: Behandeln doppelter Instanznamen
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: f58f6ed11951c7b66951f5154009127c5029de3760a9419a7c9716781be8234f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144003"
---
# <a name="handling-duplicate-instance-names"></a>Behandeln doppelter Instanznamen

Obwohl Anbietern dringend empfohlen wird, eindeutige Instanznamen zu verwenden, ist dies nicht bei allen Anbietern der Fall. Die Konvention zum Anzeigen doppelter Instanznamen besteht im Anfügen eines Zeichens und einer Seriennummer an den Instanznamen, mit Ausnahme des ersten `#` Vorkommens des Namens. Wenn beispielsweise drei Instanzen von in einem Beispiel enthalten sind, werden die drei Namen `svchost` `svchost` als , und `svchost#1` `svchost#2` angezeigt.

Leider löst diese Konvention das Problem nicht vollständig. Seriennummern werden basierend auf der Reihenfolge zugewiesen, in der ein bestimmter Instanzname in einem Beispiel angezeigt wird, und diese Reihenfolge kann von Beispiel zu Stichprobe inkonsistent sein. Beispiel A könnte beispielsweise `svchost` (PID 100), `svchost#1` (PID 200) und `svchost#2` (PID 300) sehen. Wenn dann svchost mit PID 100 heruntergefahren wird, werden im nächsten Beispiel `svchost` (PID 200) und `svchost#1` (PID 300) angezeigt. Die grundlegende Abgleichslogik versucht, die Statistiken von Beispiel A (von PID 200) mit den Statistiken von Beispiel `svchost#1` B `svchost#1` (von PID 300) zu abgleichen, was zu ungültigen Ergebnissen für Beispiel B führt. Fehler treten auf, wenn eine neue nicht eindeutige Instanz in einem Beispiel angezeigt wird oder wenn eine nicht eindeutige Instanz nicht mehr in einem Beispiel angezeigt wird (es sei denn, die hinzugefügte/entfernte Instanz war die letzte).

## <a name="process-counterset"></a>Prozesszählersatz

Dieses Problem ist besonders problematisch für das Counterset, da es nur den EXE-Namen des Prozesses als Instanznamen verwendet, obwohl der `Process` EXE-Name nicht eindeutig ist. Das Standardverhalten des `Process` Countersets für Windows aufgrund von Kompatibilitätsproblemen nicht geändert werden.

Sie können das Verhalten der Leistungsindikatoren und ändern, um eindeutige Instanznamen zu verwenden, indem Sie die Registrierungswerte oder unter `Process` `Thread` dem `ProcessNameFormat` `ThreadNameFormat` `HKLM\System\CurrentControlSet\Services\Perfproc\Performance` Registrierungsschlüssel festlegen.

> [!CAUTION]
> Das Aktivieren eindeutiger Instanznamen für das Counterset kann dazu führen, dass sich einige Programme falsch verhalten, da viele Programme das nicht `Process` eindeutige Benennungsmuster erwarten. Beispielsweise kann ein Programm, das nach einer Instanz mit einem bestimmten bekannten EXE-Namen sucht, diese Instanz nach dem Aktivieren eindeutiger Instanznamen nicht mehr finden.

Der Registrierungstyp für diese Werte ist `REG_DWORD` . Wenn Sie den Wert auf festlegen, wird der Prozessbezeichner (PID) an den Prozessinstanznamen und der Threadbezeichner `2` (TID) an den Threadinstanznamen angefügt. Um dieses Feature zu deaktivieren, legen Sie den Wert auf 1 fest, oder löschen Sie den Wert.
