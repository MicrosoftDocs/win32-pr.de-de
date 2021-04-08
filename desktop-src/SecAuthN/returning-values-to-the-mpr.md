---
description: Die Windows-Netzwerkfunktionen geben \_ bei Erfolg die WN-Funktion zurück, oder Sie geben einen eindeutigen Wert ungleich NULL zurück, wenn die Funktion einen Fehler feststellt. Außerdem geben Sie mithilfe von wnetsetlasterror und SetLastError erweiterte Fehlerinformationen zurück.
ms.assetid: cb9d29a1-b3a5-4440-a069-3cd1565b1699
title: Zurückgeben von Werten an die MPR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c96a5636f57d5c926af4e43e676f0b6db75d164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959639"
---
# <a name="returning-values-to-the-mpr"></a>Zurückgeben von Werten an die MPR

Die Windows-Netzwerkfunktionen geben \_ bei Erfolg die WN-Funktion zurück, oder Sie geben einen eindeutigen Wert ungleich NULL zurück, wenn die Funktion einen Fehler feststellt. Außerdem geben Sie mithilfe von [**wnetsetlasterror**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) und [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)erweiterte Fehlerinformationen zurück.

Um das oben beschriebene Verhalten zu unterstützen, sollten die Netzwerkanbieter Funktionen vor der Rückgabe nicht [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) aufrufen. Dies liegt daran, dass die MPR **SetLastError** für die Funktionen in der Netzwerkanbieter-API aufruft, nachdem diese zurückgegeben wurden. Wenn der Netzwerkanbieter **SetLastError** direkt aufruft, werden redundante Funktionsaufrufe durchgeführt. Netzwerkanbieter Funktionen sollten einfach einen Fehlercode zurückgeben. Die Fehlercodes werden in den Funktionsbeschreibungen oder [Rückgabe Werten](network-security-return-values.md)angegeben. Netzwerkanbieter Funktionen können auch [System Fehler Codes](../debug/system-error-codes.md)zurückgeben, z. b. unzureichenden Arbeitsspeicher. Die einzige Ausnahme ist [**NPgetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps), die eine Maske zurückgeben soll, die die vom Netzwerkanbieter unterstützten Funktionen angibt.

Wenn eine Netzwerkanbieter Funktion Erweiterte Fehlerinformationen zurückgeben muss, sollte [**wnetsetlasterror**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora)aufgerufen werden. Diese Funktion wird vom Windows-Betriebssystem zur Verwendung durch Netzwerkanbieter bereitgestellt. Wenn der Anbieter **wnetsetlasterror** aufruft, kann er eine Zeichenfolge mit zusätzlichen Informationen über den Fehler festlegen. Diese Informationen werden Thread bezogen gespeichert. Dies ist analog zu [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) für Windows-Anwendungen. Das Windows-Betriebssystem ruft **wnetsetlasterror** auf, um nach einer Zeichenfolge zu suchen, die mit **wnetsetlasterror** gespeichert wird, und gibt, sofern gefunden, die erweiterten Fehlerinformationen an die aufrufende Anwendung zurück, die die Netzwerk Anforderung initiiert hat.

> [!Note]  
> Das WNET-Präfix von [**wnetsetlasterror**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) ist irreführend, da diese API im Gegensatz zu **wnetsetlasterror** nicht Teil des Windows-Netzwerk-API-Satzes ist. **Wnetsetlasterror** ist nur für die Verwendung durch Netzwerkanbieter vorgesehen. Der Name, **wnetsetlasterror**, wird aus Gründen der Kompatibilität mit vorhandenen Anbietern beibehalten.

 

 

 
