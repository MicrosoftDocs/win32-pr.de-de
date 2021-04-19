---
description: Die dynamische Verknüpfung bietet im Vergleich zur statischen Verknüpfung die folgenden Vorteile.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Vorteile dynamischer Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349469"
---
# <a name="advantages-of-dynamic-linking"></a>Vorteile dynamischer Verknüpfungen

Die dynamische Verknüpfung bietet im Vergleich zur statischen Verknüpfung folgende Vorteile:

-   Bei mehreren Prozessen, die dieselbe DLL in derselben Basisadresse laden, wird eine einzelne Kopie der dll im physischen Speicher gemeinsam genutzt. Dadurch wird der System Arbeitsspeicher gespart und der Austausch reduziert.
-   Wenn sich die Funktionen in einer DLL ändern, müssen die Anwendungen, die Sie verwenden, nicht neu kompiliert oder erneut verknüpft werden, solange sich die Funktionsargumente, die Aufruf Konventionen und die Rückgabewerte nicht ändern. Im Gegensatz dazu erfordert ein statisch verknüpfter Objektcode, dass die Anwendung neu verknüpft wird, wenn sich die Funktionen ändern.
-   Eine DLL kann nach Marktunterstützung bereitstellen. So kann z. b. eine Anzeigetreiber-DLL geändert werden, um eine Anzeige zu unterstützen, die beim ersten Versand der Anwendung nicht verfügbar war.
-   Programme, die in verschiedenen Programmiersprachen geschrieben wurden, können dieselbe DLL-Funktion aufrufen, solange die Programme derselben Aufruf Konvention folgen, die von der Funktion verwendet wird. Die Aufruf Konvention (z. b. C, Pascal oder Standard Aufruf) steuert die Reihenfolge, in der die aufrufende Funktion die Argumente auf den Stapel übertragen muss, unabhängig davon, ob die Funktion oder die aufrufende Funktion für das Bereinigen des Stapels zuständig ist und ob Argumente in Registern übermittelt werden. Weitere Informationen finden Sie in der Dokumentation, die in Ihrem Compiler enthalten ist.

Ein möglicher Nachteil bei der Verwendung von DLLs liegt darin, dass die Anwendung nicht unabhängig ausgeführt werden kann; sie hängt von der Existenz eines separaten DLL-Moduls ab. Das System beendet Prozesse mithilfe dynamischer Ladezeit-Verknüpfungen, wenn Sie eine DLL benötigen, die beim Prozessstart nicht gefunden wurde, und eine Fehlermeldung an den Benutzer übergibt. Das System beendet einen Prozess nicht mithilfe der dynamischen Lauf Zeit Verknüpfung in dieser Situation, aber Funktionen, die von der fehlenden dll exportiert werden, sind für das Programm nicht verfügbar.

 

 



