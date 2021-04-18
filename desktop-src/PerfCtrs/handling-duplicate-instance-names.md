---
description: Obwohl es für Anbieter empfehlenswert ist, eindeutige Instanznamen zu verwenden, werden nicht alle Anbieter unterstützt.
ms.assetid: 3c8fcb8d-2ea4-4b24-b649-7bd375c1133d
title: Verarbeiten doppelter Instanznamen
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 220e5d7d0181a79c1d1415486cc946d484e11952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351681"
---
# <a name="handling-duplicate-instance-names"></a>Verarbeiten doppelter Instanznamen

Obwohl es für Anbieter dringend empfehlenswert ist, eindeutige Instanznamen zu verwenden, werden nicht alle Anbieter unterstützt. Die Konvention zum Anzeigen doppelter Instanznamen besteht darin, ein `#` Zeichen und eine Seriennummer an den Instanznamen anzufügen, mit Ausnahme des ersten Vorkommens des Namens. Wenn z. b. drei Instanzen von `svchost` in einem Beispiel vorhanden sind, werden die drei Namen als `svchost` , `svchost#1` und angezeigt `svchost#2` .

Leider löst diese Konvention das Problem nicht vollständig aus. Seriennummern werden basierend auf der Reihenfolge zugewiesen, in der ein bestimmter Instanzname in einem Beispiel angezeigt wird, und diese Reihenfolge kann nicht von Sample zu Sample abweichen. Beispielsweise könnte Sample A `svchost` (PID 100), `svchost#1` (PID 200) und `svchost#2` (PID 300) angezeigt werden. Wenn der svchost mit PID 100 heruntergefahren wird, wird im nächsten Beispiel `svchost` (PID 200) und `svchost#1` (PID 300) angezeigt. Die grundlegende übereinstimmende Logik würde versuchen, die Beispiel `svchost#1` Statistik Statistik (von PID 200) mit der `svchost#1` Statistik von Beispiel b (von PID 300) abzugleichen, was zu ungültigen Ergebnissen für Beispiel b führt. Fehler treten auf, wenn eine neue, nicht eindeutige Instanz in einem Beispiel angezeigt wird oder wenn eine nicht eindeutige Instanz in einem Beispiel nicht mehr angezeigt wird

## <a name="process-counterset"></a>Prozess CounterSet

Dieses Problem ist besonders problematisch für das `Process` CounterSet, weil es nur den exe-Namen des Prozesses als Instanznamen verwendet, auch wenn der Name der exe-Datei nicht eindeutig ist. Das Standardverhalten des `Process` countersets unter Windows kann aufgrund von Kompatibilitätsproblemen nicht geändert werden.

Sie können das Verhalten der `Process` -und- `Thread` Gegensätze ändern, um eindeutige Instanznamen zu verwenden, indem Sie die- `ProcessNameFormat` oder- `ThreadNameFormat` Registrierungs Werte unter dem `HKLM\System\CurrentControlSet\Services\Perfproc\Performance` Registrierungsschlüssel festlegen.

> [!CAUTION]
> Das Aktivieren eindeutiger Instanznamen für den `Process` CounterSet kann dazu führen, dass einige Programme nicht ordnungsgemäß Verhalten, da viele Programme das nicht eindeutige Benennungs Muster erwarten. Beispielsweise ist ein Programm, das nach einer Instanz mit einem bestimmten bekannten exe-Namen sucht, nicht mehr in der Lage, diese Instanz nach dem Aktivieren eindeutiger Instanznamen zu finden.

Der Registrierungstyp für diese Werte ist `REG_DWORD` . Wenn Sie den Wert auf festlegen, wird `2` die Prozess-ID (PID) an den prozessinstanznamen und den Thread Bezeichner (TID) an den Thread Instanznamen angehängt. Um diese Funktion zu deaktivieren, legen Sie den Wert auf 1 fest, oder löschen Sie den Wert.
