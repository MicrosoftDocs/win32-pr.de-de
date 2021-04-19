---
description: 'Multitasking kann auf zwei Arten implementiert werden: als einzelner Prozess mit mehreren Threads oder als mehrere Prozesse mit jeweils einem oder mehreren Threads.'
ms.assetid: ac0a8163-1498-4274-acfc-6a36b4c02a27
title: Verwendung von Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17e52f39a08120d3038663a95307ad72f228cfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353524"
---
# <a name="when-to-use-multitasking"></a>Verwendung von Multitasking

Multitasking kann auf zwei Arten implementiert werden: als einzelner Prozess mit mehreren Threads oder als mehrere Prozesse mit jeweils einem oder mehreren Threads. Eine Anwendung kann jeden Thread, der einen privaten Adressraum und private Ressourcen benötigt, in einen eigenen Prozess versetzen, um ihn vor den Aktivitäten anderer Prozessthreads zu schützen.

Ein Multithreadprozess kann sich gegenseitig ausschließende Aufgaben mit Threads verwalten, z. b. das Bereitstellen einer Benutzeroberfläche und das Ausführen von Hintergrund Berechnungen. Das Erstellen eines Multithread-Prozesses kann auch eine bequeme Möglichkeit zum Strukturieren eines Programms sein, das mehrere ähnliche oder identische Aufgaben gleichzeitig ausführt. Beispielsweise kann ein Named Pipe Server einen Thread für jeden Client Prozess erstellen, der an die Pipe angefügt wird. Dieser Thread verwaltet die Kommunikation zwischen dem Server und dem Client. Der Prozess kann mehrere Threads verwenden, um die folgenden Aufgaben auszuführen:

-   Verwalten von Eingaben für mehrere Fenster.
-   Verwalten von Eingaben über verschiedene Kommunikationsgeräte
-   Unterscheiden von Tasks unterschiedlicher Priorität. Beispielsweise verwaltet ein Thread mit hoher Priorität zeitkritische Tasks, und ein Thread mit niedriger Priorität führt andere Tasks aus.
-   Gewährleisten einer reaktionsschnellen Benutzeroberfläche bei gleichzeitigem Zuweisen von Zeitsegmenten für im Hintergrund ausgeführten Tasks

Aus den folgenden Gründen ist es in der Regel effizienter, wenn eine Anwendung Multitasking implementiert, indem ein einzelner Multithread-Prozess erstellt wird, anstatt mehrere Prozesse zu erstellen:

-   Das System kann einen Kontextwechsel schneller für Threads ausführen als Prozesse, da ein Prozess mehr Aufwand als ein Thread hat (der Prozess Kontext ist größer als der Thread Kontext).
-   Alle Threads eines Prozesses verwenden denselben Adressraum und können auf die globalen Variablen des Prozesses zugreifen, wodurch die Kommunikation zwischen Threads vereinfacht werden kann.
-   Alle Threads eines Prozesses können offene Handles für Ressourcen freigeben, wie z. b. Dateien und Pipes.

Es gibt weitere Techniken, die Sie anstelle von Multithreading verwenden können. Dies sind die folgenden: asynchrone Eingabe-und Ausgabe Vorgänge (e/a), e/a-Abschlussports, asynchrone Prozedur Aufrufe (APC) und die Möglichkeit, auf mehrere Ereignisse zu warten.

Ein einzelner Thread kann mehrere zeitaufwändige e/a-Anforderungen initiieren, die gleichzeitig mithilfe asynchroner e/a-Vorgänge ausgeführt werden können. Asynchrone e/a-Vorgänge können für Dateien, Pipes und serielle Kommunikationsgeräte ausgeführt werden. Weitere Informationen finden Sie unter [Synchronisierung und überlappende Eingabe und Ausgabe](../sync/synchronization-and-overlapped-input-and-output.md).

Ein einzelner Thread kann seine eigene Ausführung blockieren, während darauf gewartet wird, dass ein oder alle von mehreren Ereignissen eintreten. Dies ist effizienter als die Verwendung mehrerer Threads, die jeweils auf ein einzelnes Ereignis warten, und effizienter als die Verwendung eines einzelnen Threads, der Prozessorzeit beansprucht, indem ständig überprüft wird, ob Ereignisse eintreten. Weitere Informationen finden Sie unter [Wait-Funktionen](../sync/wait-functions.md).

 

 
