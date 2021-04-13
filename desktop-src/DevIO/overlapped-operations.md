---
description: Überlappende Vorgänge ermöglichen einem Thread das Ausführen eines zeitaufwändigen e/a-Vorgangs im Hintergrund, sodass der Thread keine weiteren Aufgaben ausführen kann.
ms.assetid: 8c0eb20d-685a-4750-8253-a87089b68509
title: Überlappende Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d8dc9e39386e25129d3e7d7a5281a8299d54ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483270"
---
# <a name="overlapped-operations"></a>Überlappende Vorgänge

Überlappende Vorgänge ermöglichen einem Thread das Ausführen eines zeitaufwändigen e/a-Vorgangs im Hintergrund, sodass der Thread keine weiteren Aufgaben ausführen kann. Um überlappende e/a-Vorgänge für eine Kommunikations Ressource zu aktivieren, muss der Thread das überlappende Flag für das **\_ Dateiflag \_** in der Funktion " [**foratefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " angeben, wenn das Handle geöffnet wird. Um die Funktion "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " oder " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " als überlappenden Vorgang auszuführen, muss der aufrufende Thread einen Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur angeben. Die **über** Lapp Ende Struktur muss ein Handle für ein Ereignis Objekt für manuelles Zurücksetzen (kein automatisches Zurücksetzen) enthalten. Das System legt den Status des Ereignis Objekts auf "nicht signalisiert" fest, wenn ein Aufrufe an die e/a-Funktion zurückgegeben wird, bevor der Vorgang abgeschlossen wurde. Das System legt den Status des Ereignis Objekts auf signalisiert fest, wenn der Vorgang abgeschlossen wurde. Der Thread verwendet eine wait-Funktion, um den aktuellen Status des Ereignis Objekts zu überprüfen oder zu warten, bis der Zustand signalisiert wird.

Die Funktionen "read [**fileex**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) " und " [**Write fileex**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) " können nur als überlappende Vorgänge ausgeführt werden. Der aufrufende Thread gibt einen Zeiger auf die Funktion " [**fleiocompletionroutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) " an, die ausgeführt wird, wenn der überlappende Vorgang abgeschlossen ist. Die Vervollständigungs Routine wird nur ausgeführt, wenn der aufrufende Thread einen mindestwarnzeit-Vorgang ausführt.

Weitere Informationen zu Ereignis Objekten, Wait-Funktionen, wartetabellenwartezeiten und Vervollständigungs Routinen finden Sie unter [Informationen zur Synchronisierung](/windows/desktop/Sync/about-synchronization).

 

 
