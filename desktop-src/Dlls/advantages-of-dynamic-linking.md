---
description: Dynamisches Verknüpfen hat gegenüber statischer Verknüpfung die folgenden Vorteile.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Vorteile der dynamischen Verknüpfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00a35e254ae14f74d5e2ed4c260f3ee201e2fd1f62efd8aa953b708256e437c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632280"
---
# <a name="advantages-of-dynamic-linking"></a>Vorteile der dynamischen Verknüpfung

Die dynamische Verknüpfung hat gegenüber der statischen Verknüpfung die folgenden Vorteile:

-   Mehrere Prozesse, die dieselbe DLL an derselben Basisadresse laden, verwenden eine einzige Kopie der DLL im physischen Speicher. Dadurch wird Systemspeicher gespart und der Austausch reduziert.
-   Wenn sich die Funktionen in einer DLL ändern, müssen die Anwendungen, die sie verwenden, nicht neu kompiliert oder neu verknüpft werden, solange sich die Funktionsargumente, Aufrufkonventionen und Rückgabewerte nicht ändern. Im Gegensatz dazu erfordert ein statisch verknüpfter Objektcode, dass die Anwendung neu verknüpft wird, wenn sich die Funktionen ändern.
-   Eine DLL kann Unterstützung nach dem Markt bieten. Beispielsweise kann eine Anzeigetreiber-DLL geändert werden, um eine Anzeige zu unterstützen, die beim ersten Versand der Anwendung nicht verfügbar war.
-   In verschiedenen Programmiersprachen geschriebene Programme können dieselbe DLL-Funktion aufrufen, solange die Programme derselben Aufrufkonvention folgen, die von der Funktion verwendet wird. Die Aufrufkonvention (z. B. C, Pascal oder Standardaufruf) steuert die Reihenfolge, in der die aufrufende Funktion die Argumente auf den Stapel pushen muss, ob die Funktion oder die aufrufende Funktion für die Bereinigung des Stapels verantwortlich ist und ob Argumente in Registern übergeben werden. Weitere Informationen finden Sie in der Dokumentation, die in Ihrem Compiler enthalten ist.

Ein möglicher Nachteil bei der Verwendung von DLLs liegt darin, dass die Anwendung nicht unabhängig ausgeführt werden kann; sie hängt von der Existenz eines separaten DLL-Moduls ab. Das System beendet Prozesse mit dynamischer Verknüpfung zur Ladezeit, wenn sie eine DLL benötigen, die beim Prozessstart nicht gefunden wird, und gibt dem Benutzer eine Fehlermeldung aus. Das System beendet in dieser Situation keinen Prozess mit dynamischer Laufzeitverknüpfung, aber funktionen, die von der fehlenden DLL exportiert werden, sind für das Programm nicht verfügbar.

 

 



