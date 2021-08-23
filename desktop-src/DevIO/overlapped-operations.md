---
description: Überlappende Vorgänge ermöglichen es einem Thread, einen zeitaufwändigen E/A-Vorgang im Hintergrund auszuführen, sodass der Thread andere Aufgaben ausführen kann.
ms.assetid: 8c0eb20d-685a-4750-8253-a87089b68509
title: Überlappende Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ba148d0b2085e2c44e71c4c8d309f9a068223eebe8de8e239f13095c8ddd39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956889"
---
# <a name="overlapped-operations"></a>Überlappende Vorgänge

Überlappende Vorgänge ermöglichen es einem Thread, einen zeitaufwändigen E/A-Vorgang im Hintergrund auszuführen, sodass der Thread andere Aufgaben ausführen kann. Um überlappende E/A-Vorgänge für eine Kommunikationsressource zu aktivieren, muss der Thread das **FLAG FILE \_ FLAG \_ OVERLAPPED** in der [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) angeben, wenn das Handle geöffnet wird. Um die [**ReadFile-**](/windows/desktop/api/fileapi/nf-fileapi-readfile) oder [**WriteFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-writefile) als überlappenden Vorgang auszuführen, muss der aufrufende Thread einen Zeiger auf eine [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) angeben. Die **OVERLAPPED-Struktur** muss ein Handle für ein Ereignisobjekt mit manueller Zurücksetzung (kein automatisches Zurücksetzen) enthalten. Das System legt den Zustand des Ereignisobjekts auf not-signaled fest, wenn ein Aufruf der E/A-Funktion zurückgegeben wird, bevor der Vorgang abgeschlossen wurde. Das System legt den Zustand des Ereignisobjekts so fest, dass er signalisiert wird, wenn der Vorgang abgeschlossen wurde. Der Thread verwendet eine Wait-Funktion, um den aktuellen Zustand des Ereignisobjekts zu überprüfen oder auf die Signalisierung des Zustands zu warten.

Die [**Funktionen ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) und [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) können nur als überlappende Vorgänge ausgeführt werden. Der aufrufende Thread gibt einen Zeiger auf die [**FileIOCompletionRoutine-Funktion**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) an, die ausgeführt wird, wenn der überlappende Vorgang abgeschlossen wird. Die Abschlussroutine wird nur ausgeführt, wenn der aufrufende Thread einen warnungsfähigen Vorgang ausführt.

Weitere Informationen zu Ereignisobjekten, Wartefunktionen, warnungsfähigen Warte- und Abschlussroutinen finden Sie unter Informationen zur [Synchronisierung.](/windows/desktop/Sync/about-synchronization)

 

 
