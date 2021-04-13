---
description: Ein Synchronisierungs Objekt ist ein Objekt, dessen Handle in einer der Wait-Funktionen angegeben werden kann, um die Ausführung mehrerer Threads zu koordinieren.
ms.assetid: 11558ae9-1056-48bf-96f5-94a051df41c3
title: Synchronisierungs Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299cbd6225b3cc7629378f5fe500fc36ccbe8e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529228"
---
# <a name="synchronization-objects"></a>Synchronisierungs Objekte

Ein *Synchronisierungs Objekt* ist ein Objekt, dessen Handle in einer der Wait- [Funktionen](wait-functions.md) angegeben werden kann, um die Ausführung mehrerer Threads zu koordinieren. Mehrere Prozesse können über ein Handle für das gleiche Synchronisierungs Objekt verfügen, sodass die prozessübergreifende Synchronisierung möglich ist.

Die folgenden Objekttypen werden exklusiv für die Synchronisierung bereitgestellt.



| type           | BESCHREIBUNG                                                                                                                                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ereignis          | Benachrichtigt einen oder mehrere wartende Threads über das Eintreten eines Ereignisses. Weitere Informationen finden Sie unter [Event Objects](event-objects.md).                                                                                   |
| Mutex          | Kann im Besitz von nur einem Thread gleichzeitig sein, sodass Threads den sich gegenseitig ausschließenden Zugriff auf eine freigegebene Ressource koordinieren können. Weitere Informationen finden Sie unter [Mutex Objects](mutex-objects.md).                          |
| Semaphore      | Behält eine Anzahl zwischen null und einem maximalen Wert bei und schränkt die Anzahl von Threads ein, die gleichzeitig auf eine freigegebene Ressource zugreifen. Weitere Informationen finden Sie unter [Semaphore-Objekte](semaphore-objects.md). |
| Aktivierungszeit Geber | Benachrichtigt einen oder mehrere wartende Threads, dass eine angegebene Zeit erreicht wurde. Weitere Informationen finden Sie unter [wanutzbare Timer-Objekte](waitable-timer-objects.md).                                                          |



 

Obwohl die folgenden Objekte für andere Verwendungszwecke verfügbar sind, können Sie auch für die Synchronisierung verwendet werden.



| Object                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Benachrichtigung ändern          | Der Status wird durch die [**findfirstchangenotifi-**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) Funktion erstellt und ist auf "signalisiert" festgelegt, wenn ein bestimmter Änderungstyp innerhalb eines angegebenen Verzeichnisses oder einer Verzeichnisstruktur auftritt. Weitere Informationen finden Sie unter Abrufen von [Benachrichtigungen zu Verzeichnisänderungen](../fileio/obtaining-directory-change-notifications.md).                                                                                                                                   |
| Konsolen Eingabe                | Wird erstellt, wenn eine-Konsole erstellt wird. Das Handle für die Konsolen Eingabe wird von der Funktion " [**reatefile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) " zurückgegeben, wenn "$" oder die Funktion " [**getstdhandle**](/windows/console/getstdhandle) " angegeben wird. Der Status wird auf "signalisiert" festgelegt, wenn ungelesene Eingaben im Eingabepuffer der Konsole vorhanden sind, und auf "nicht signalisiert" festgelegt, wenn der Eingabepuffer leer ist. Weitere Informationen zu-Konsolen finden Sie unter [Zeichenmodus-Anwendungen](/windows/console/character-mode-applications) . |
| Auftrag                          | Wird durch Aufrufen der [**CreateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-createjobobjectw) -Funktion erstellt. Der Status eines Auftrags Objekts wird auf "signalisiert" festgelegt, wenn alle zugehörigen Prozesse beendet werden, da das angegebene Zeitlimit für das Zeitlimit überschritten wurde. Weitere Informationen zu Auftrags Objekten finden Sie unter [Auftrags Objekte](../procthread/job-objects.md).                                                                                                                                                             |
| Benachrichtigung zu Speicherressourcen | Wird von der Funktion " [**kreatememoryresourcenotifi"**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) erstellt. Der Status wird auf "signalisiert" festgelegt, wenn ein angegebener Änderungstyp im physischen Speicher auftritt. Weitere Informationen zum Arbeitsspeicher finden Sie unter [Speicherverwaltung](../memory/memory-management.md).                                                                                                                                                                                  |
| Prozess                      | Wird durch Aufrufen der [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) -Funktion erstellt. Der Status wird auf "nicht signalisiert" festgelegt, während der Prozess ausgeführt wird, und wird beim Beenden des Prozesses auf "signalisiert" festgelegt. Weitere Informationen zu Prozessen finden Sie unter [Prozesse und Threads](../procthread/processes-and-threads.md).                                                                                                                                                                                  |
| Thread                       | Wird erstellt, wenn ein neuer Thread erstellt wird, indem die [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)-, [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)-oder [**createremotethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) -Funktion aufgerufen wird. Der Status wird auf "nicht signalisiert" festgelegt, während der Thread ausgeführt wird, und wird beim Beenden des Threads auf "signalisiert" festgelegt. Weitere Informationen zu Threads finden Sie unter [Prozesse und Threads](../procthread/processes-and-threads.md).                                                            |



 

Unter bestimmten Umständen können Sie auch ein Datei-, Named Pipe-oder Kommunikationsgerät als Synchronisierungs Objekt verwenden. Allerdings wird davon abgeraten, zu diesem Zweck zu verwenden. Verwenden Sie stattdessen asynchrone e/a-Vorgänge, und warten Sie auf das Ereignis Objekt, das in der [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur festgelegt ist. Es ist sicherer, das Ereignis Objekt aufgrund der Verwirrung zu verwenden, die auftreten kann, wenn mehrere gleichzeitig überlappende Vorgänge für dieselbe Datei, Named Pipe oder dasselbe Kommunikationsgerät ausgeführt werden. In dieser Situation gibt es keine Möglichkeit, zu ermitteln, welcher Vorgang bewirkt hat, dass der Objektzustand signalisiert wird.

Weitere Informationen zu e/a-Vorgängen für Dateien, Named Pipes oder Mitteilungen finden Sie unter [Synchronisierung und überlappende Eingabe und Ausgabe](synchronization-and-overlapped-input-and-output.md).

 

 
