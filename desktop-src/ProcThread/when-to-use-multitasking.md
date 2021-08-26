---
description: 'Es gibt zwei Möglichkeiten, Multitasking zu implementieren: als einzelner Prozess mit mehreren Threads oder als mehrere Prozesse mit jeweils einem oder mehreren Threads.'
ms.assetid: ac0a8163-1498-4274-acfc-6a36b4c02a27
title: Verwendung von Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e37f63ada4aa1a17355ac3bc5b7361d498a1a20ec87b490965b53c4811ebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031340"
---
# <a name="when-to-use-multitasking"></a>Verwendung von Multitasking

Es gibt zwei Möglichkeiten, Multitasking zu implementieren: als einzelner Prozess mit mehreren Threads oder als mehrere Prozesse mit jeweils einem oder mehreren Threads. Eine Anwendung kann jeden Thread, der einen privaten Adressraum und private Ressourcen erfordert, in einen eigenen Prozess setzen, um ihn vor den Aktivitäten anderer Prozessthreads zu schützen.

Ein Multithreadprozess kann sich gegenseitig ausschließende Aufgaben mit Threads verwalten, z. B. das Bereitstellen einer Benutzeroberfläche und das Ausführen von Hintergrundberechnungen. Das Erstellen eines Multithreadprozesses kann auch eine bequeme Möglichkeit sein, ein Programm zu strukturieren, das mehrere ähnliche oder identische Aufgaben gleichzeitig ausführt. Beispielsweise kann ein Named Pipe-Server einen Thread für jeden Clientprozess erstellen, der an die Pipe angefügt wird. Dieser Thread verwaltet die Kommunikation zwischen dem Server und dem Client. Ihr Prozess kann mehrere Threads verwenden, um die folgenden Aufgaben auszuführen:

-   Verwalten von Eingaben für mehrere Fenster.
-   Verwalten von Eingaben von mehreren Kommunikationsgeräten.
-   Unterscheiden von Tasks unterschiedlicher Priorität. Beispielsweise verwaltet ein Thread mit hoher Priorität zeitkritische Tasks, und ein Thread mit niedriger Priorität führt andere Tasks aus.
-   Gewährleisten einer reaktionsschnellen Benutzeroberfläche bei gleichzeitigem Zuweisen von Zeitsegmenten für im Hintergrund ausgeführten Tasks

Es ist in der Regel effizienter, wenn eine Anwendung Multitasking implementiert, indem ein einzelner Multithreadprozess erstellt wird, anstatt mehrere Prozesse zu erstellen. Dies hat folgende Gründe:

-   Das System kann einen Kontextwechsel für Threads schneller ausführen als Prozesse, da ein Prozess mehr Aufwand auf sich hat als ein Thread (der Prozesskontext ist größer als der Threadkontext).
-   Alle Threads eines Prozesses verwenden denselben Adressraum und können auf die globalen Variablen des Prozesses zugreifen, was die Kommunikation zwischen Threads vereinfachen kann.
-   Alle Threads eines Prozesses können geöffnete Handles für Ressourcen wie Dateien und Pipes freigeben.

Es gibt andere Techniken, die Sie statt Multithreading verwenden können. Die wichtigsten davon sind: asynchrone Eingabe und Ausgabe (E/A), E/A-Abschlussports, asynchrone Prozeduraufrufe (APC) und die Möglichkeit, auf mehrere Ereignisse zu warten.

Ein einzelner Thread kann mehrere zeitaufwändige E/A-Anforderungen initiieren, die mit asynchronen E/A-Vorgängen gleichzeitig ausgeführt werden können. Asynchrone E/A-Vorgänge können auf Dateien, Pipes und seriellen Kommunikationsgeräten ausgeführt werden. Weitere Informationen finden Sie unter [Synchronisierung und überlappende Eingabe und Ausgabe.](../sync/synchronization-and-overlapped-input-and-output.md)

Ein einzelner Thread kann seine eigene Ausführung blockieren, während darauf gewartet wird, dass ein oder mehrere Ereignisse auftreten. Dies ist effizienter als die Verwendung mehrerer Threads, von denen jeder auf ein einzelnes Ereignis wartet, und effizienter als die Verwendung eines einzelnen Threads, der Prozessorzeit verbraucht, indem kontinuierlich überprüft wird, ob Ereignisse auftreten. Weitere Informationen finden Sie unter [Wait Functions](../sync/wait-functions.md).

 

 
