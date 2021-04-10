---
description: Wenn ein Prozess mit dem Datei Zuordnungs Objekt abgeschlossen ist, sollte er alle Datei Sichten in seinem Adressraum mithilfe der UnmapViewOfFile-Funktion für jede Dateiansicht zerstören.
ms.assetid: d62d068c-9b1d-4dbf-8b21-31a636a41456
title: Schließen eines Datei Mapping-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab35152bd90d401ca7f30a7497d1f0b06263539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864864"
---
# <a name="closing-a-file-mapping-object"></a>Schließen eines Datei Mapping-Objekts

Wenn ein Prozess mit dem Datei Zuordnungs Objekt abgeschlossen ist, sollte er alle Datei Sichten in seinem Adressraum mithilfe der [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) -Funktion für jede Dateiansicht zerstören.

Durch das Aufheben der Zuordnung einer zugeordneten Sicht einer Datei wird der von der Sicht im Adressraum des Prozesses belegte Bereich ungültig, und der Bereich wird für andere Zuordnungen zur Verfügung gestellt. Der Arbeits Satz Eintrag für jede nicht zugeordnete virtuelle Seite, die Teil des Workingsets des Prozesses war, wird entfernt, und die Workingsetgröße des Prozesses wird reduziert. Außerdem wird die Freigabe Anzahl der entsprechenden physischen Seite verringert.

Geänderte Seiten in der nicht zugeordneten Sicht werden erst auf den Datenträger geschrieben, wenn ihre Freigabe Anzahl 0 (null) erreicht, d. h., bis die Zuordnung aufgehoben oder die Arbeits Sätze aller Prozesse, die die Seitenteilen, nicht zugeordnet sind. Auch dann werden die geänderten Seiten "verzögert" auf den Datenträger geschrieben. Das heißt, Änderungen können im Arbeitsspeicher zwischengespeichert und zu einem späteren Zeitpunkt auf den Datenträger geschrieben werden. Um das Risiko eines Daten Verlusts im Falle eines Stromausfalls oder eines Systemabsturzes zu minimieren, sollten Anwendungen geänderte Seiten explizit mithilfe der [**flushviewoffile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) -Funktion leeren.

Wenn jeder Prozess mit dem Datei Zuordnungsobjekt abgeschlossen wird und alle Sichten nicht zugeordnet wurden, muss er das Handle des Datei Zuordnungsobjekts und die Datei auf dem Datenträger schließen, indem [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)aufgerufen wird. Diese Aufrufe von **CloseHandle** sind auch dann erfolgreich, wenn Datei Sichten vorhanden sind, die noch geöffnet sind. Das belassen von Datei Sichten verursacht jedoch Speicher Verluste.

 

 
