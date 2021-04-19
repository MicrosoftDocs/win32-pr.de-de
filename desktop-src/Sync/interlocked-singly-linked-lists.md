---
description: Eine Interlocked einzeln verknüpfte Liste (SLIST) vereinfacht die Aufgabe zum Einfügen und löschen aus einer verknüpften Liste.
ms.assetid: 35463ace-33ab-4eb9-9901-2504a92456e2
title: Miteinander verknüpfte, einzeln verknüpfte Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af39847fa2fd1b1873c661d6ec904783e0139b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348750"
---
# <a name="interlocked-singly-linked-lists"></a>Miteinander verknüpfte, einzeln verknüpfte Listen

Eine *Interlocked einzeln verknüpfte Liste* (SLIST) vereinfacht die Aufgabe zum Einfügen und löschen aus einer verknüpften Liste. Slists werden mithilfe eines nicht blockierenden Algorithmus implementiert, um eine atomarische Synchronisierung bereitzustellen, die Systemleistung zu erhöhen und Probleme wie Prioritäts-und Sperr Konvois zu vermeiden.

Slists sind einfach zu implementieren und in 32-Bit-Code zu verwenden. Es ist jedoch eine Herausforderung, Sie in 64-Bit-Code zu implementieren, da die Menge der Daten, die durch die systemeigenen, austauschbaren Austausch primitiven ausgetauscht werden, nicht doppelt so groß wie die Adressgröße ist, da Sie in 32-Bit-Code vorliegt. Slists ermöglichen daher das Portieren von skalierbaren High-End-Algorithmen auf Windows.

**Windows 8:** Ab Windows 8 sind die entsprechenden systemeigenen, systeminternen Austausch primitiven für 64-Bit-Code verfügbar, z. b. [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85)).

Anwendungen können slists verwenden, indem Sie die [**initializeslisorad**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) -Funktion aufrufen, um den Anfang der Liste zu initialisieren. Um Elemente in die Liste einzufügen, verwenden Sie die Funktion [**interlockedpushentryslist**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) . Um Elemente aus der Liste zu löschen, verwenden Sie die Funktion [**interlockedpopentryslist**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) .

Alle Listenelemente müssen an der **\_ \_ Ausrichtungs Grenze der Speicher Belegung** ausgerichtet werden. Nicht ausgerichtete Elemente können zu unvorhersehbaren Ergebnissen führen. Siehe **\_ ausgerichtete \_ malloc**.

Ein Beispiel finden Sie unter [Verwenden von einzeln verknüpften Listen](using-singly-linked-lists.md).

In der folgenden Tabelle sind die slist-Funktionen aufgeführt.



| Funktion                                                         | BESCHREIBUNG                                                                                                                                               |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Initializeslisder AD**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead)               | Initialisiert den Anfang einer einzeln verknüpften Liste.                                                                                                             |
| [**Interlockedflushslist**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist)           | Leert die gesamte Liste der Elemente in einer einzeln verknüpften Liste.                                                                                                 |
| [**Interlockedpopentryslist**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)     | Entfernt ein Element von der Vorderseite einer einzeln verknüpften Liste.                                                                                                   |
| [**Interlockedpushentryslist**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)   | Fügt ein Element am Anfang einer einzeln verknüpften Liste ein.                                                                                                     |
| [**Interlockedpushlistslist**](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))     | Fügt eine einzeln verknüpfte Liste an der Vorderseite einer anderen verknüpften Liste ein.                                                                                  |
| [**Interlockedpushlistslistex**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex) | Fügt eine einzeln verknüpfte Liste an der Vorderseite einer anderen verknüpften Liste ein. Diese Version der-Methode verwendet nicht die **\_ \_ fastcall** -Aufruf Konvention. |
| [**Rtlfirstentryslist**](/windows/desktop/api/WinNT/nf-winnt-rtlfirstentryslist)                 | Ruft den ersten Eintrag in einer einzeln verknüpften Liste ab.                                                                                                        |
| [**Querydepthslist**](/windows/win32/api/interlockedapi/nf-interlockedapi-querydepthslist)                       | Ruft die Anzahl der Einträge in der angegebenen einzeln verknüpften Liste ab.                                                                                      |



 

 

 
