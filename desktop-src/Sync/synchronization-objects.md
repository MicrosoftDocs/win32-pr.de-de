---
description: Ein Synchronisierungsobjekt ist ein Objekt, dessen Handle in einer der Wartefunktionen angegeben werden kann, um die Ausführung mehrerer Threads zu koordinieren.
ms.assetid: 11558ae9-1056-48bf-96f5-94a051df41c3
title: Synchronisierungsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfd011663e13d8d6992355d99cc643e2f7243f8385ae75f9274367bfc43fe5f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885908"
---
# <a name="synchronization-objects"></a>Synchronisierungsobjekte

Ein *Synchronisierungsobjekt* ist ein Objekt, dessen Handle in einer der [Wartefunktionen](wait-functions.md) angegeben werden kann, um die Ausführung mehrerer Threads zu koordinieren. Mehrere Prozesse können über ein Handle für dasselbe Synchronisierungsobjekt verfügen, um die prozessübergreifende Synchronisierung zu ermöglichen.

Die folgenden Objekttypen werden ausschließlich für die Synchronisierung bereitgestellt.



| type           | BESCHREIBUNG                                                                                                                                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ereignis          | Benachrichtigt einen oder mehrere wartende Threads über das Eintreten eines Ereignisses. Weitere Informationen finden Sie unter [Ereignisobjekte.](event-objects.md)                                                                                   |
| Mutex          | Kann jeweils nur einem Thread gehören, sodass Threads den sich gegenseitig ausschließenden Zugriff auf eine freigegebene Ressource koordinieren können. Weitere Informationen finden Sie unter [Mutex-Objekte.](mutex-objects.md)                          |
| Semaphore      | Behält eine Anzahl zwischen 0 (null) und einem bestimmten Höchstwert bei und begrenzt die Anzahl der Threads, die gleichzeitig auf eine freigegebene Ressource zugreifen. Weitere Informationen finden Sie unter [Semaphore Objects](semaphore-objects.md). |
| Wartebarer Timer | Benachrichtigt mindestens einen wartenden Thread, dass eine angegebene Zeit erreicht ist. Weitere Informationen finden Sie unter [Wartebare Timerobjekte.](waitable-timer-objects.md)                                                          |



 

Obwohl für andere Zwecke verfügbar, können die folgenden Objekte auch für die Synchronisierung verwendet werden.



| Object                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Änderungsbenachrichtigung          | Der von der [**FindFirstChangeNotification-Funktion**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) erstellte Zustand wird auf signalisiert festgelegt, wenn ein angegebener Änderungstyp innerhalb eines angegebenen Verzeichnisses oder einer Verzeichnisstruktur auftritt. Weitere Informationen finden Sie unter [Abrufen von Verzeichnisänderungsbenachrichtigungen.](../fileio/obtaining-directory-change-notifications.md)                                                                                                                                   |
| Konsoleneingabe                | Wird erstellt, wenn eine Konsole erstellt wird. Das Handle für die Konsoleneingabe wird von der [**CreateFile-Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) zurückgegeben, wenn CONIN$ angegeben wird, oder von der [**GetStdHandle-Funktion.**](/windows/console/getstdhandle) Der Status wird auf signalisiert festgelegt, wenn im Eingabepuffer der Konsole ungelesene Eingaben vorhanden sind, und auf Nicht signalisiert festgelegt, wenn der Eingabepuffer leer ist. Weitere Informationen zu Konsolen finden Sie unter [Zeichenmodusanwendungen.](/windows/console/character-mode-applications) |
| Auftrag                          | Erstellt durch Aufrufen der [**CreateJobObject-Funktion.**](/windows/win32/api/jobapi2/nf-jobapi2-createjobobjectw) Der Status eines Auftragsobjekts wird auf signalisiert festgelegt, wenn alle prozesse beendet werden, da das angegebene Zeitlimit für das Ende des Auftrags überschritten wurde. Weitere Informationen zu Auftragsobjekten finden Sie unter [Auftragsobjekte.](../procthread/job-objects.md)                                                                                                                                                             |
| Speicherressourcenbenachrichtigung | Wird von der [**CreateMemoryResourceNotification-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) erstellt. Der Zustand wird auf signalisiert festgelegt, wenn ein angegebener Änderungstyp innerhalb des physischen Arbeitsspeichers auftritt. Weitere Informationen zum Arbeitsspeicher finden Sie unter [Speicherverwaltung.](../memory/memory-management.md)                                                                                                                                                                                  |
| Prozess                      | Wird durch Aufrufen der [**CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) erstellt. Sein Zustand wird auf nicht signalisiert festgelegt, während der Prozess ausgeführt wird, und auf signalisiert, wenn der Prozess beendet wird. Weitere Informationen zu Prozessen finden Sie unter [Prozesse und Threads.](../procthread/processes-and-threads.md)                                                                                                                                                                                  |
| Thread                       | Wird erstellt, wenn ein neuer Thread durch Aufrufen der [**CreateProcess-,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) [**CreateThread-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)oder [**CreateRemoteThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) erstellt wird. Sein Zustand wird auf nicht signalisiert festgelegt, während der Thread ausgeführt wird, und auf signalisiert, wenn der Thread beendet wird. Weitere Informationen zu Threads finden Sie unter [Prozesse und Threads.](../procthread/processes-and-threads.md)                                                            |



 

In einigen Fällen können Sie auch eine Datei, eine Named Pipe oder ein Kommunikationsgerät als Synchronisierungsobjekt verwenden. von der Verwendung zu diesem Zweck wird jedoch abgeraten. Verwenden Sie stattdessen asynchrone E/A, und warten Sie auf das Ereignisobjekt, das in der [**OVERLAPPED-Struktur**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) festgelegt ist. Aufgrund der Verwirrung, die auftreten kann, wenn mehrere gleichzeitig überlappende Vorgänge auf demselben Datei-, Named Pipe- oder Kommunikationsgerät ausgeführt werden, ist es sicherer, das Ereignisobjekt zu verwenden. In dieser Situation gibt es keine Möglichkeit zu wissen, welcher Vorgang dazu geführt hat, dass der Zustand des Objekts signalisiert wurde.

Weitere Informationen zu E/A-Vorgängen für Dateien, Named Pipes oder Kommunikation finden Sie unter [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md).

 

 
