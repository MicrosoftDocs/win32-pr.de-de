---
description: Um die Daten aus einer Datei dem virtuellen Arbeitsspeicher eines Prozesses zuzuordnen, müssen Sie eine Ansicht der Datei erstellen.
ms.assetid: b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4
title: Erstellen einer Dateiansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498f7ba132efd9ecf82f9ec087492c9622824b51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959669"
---
# <a name="creating-a-file-view"></a>Erstellen einer Dateiansicht

Um die Daten aus einer Datei dem virtuellen Arbeitsspeicher eines Prozesses zuzuordnen, müssen Sie eine Ansicht der Datei erstellen. Die Funktionen [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) und [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) verwenden das von " [**kreatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " zurückgegebene dateimappingobjekthandle, um eine Ansicht der Datei oder einen Teil der Datei im virtuellen Adressraum des Prozesses zu erstellen. Diese Funktionen schlagen fehl, wenn die Zugriffsflags einen Konflikt mit den **beim Erstellen des** Datei Zuordnungsobjekts angegebenen Zugriffsflags verursachen.

Die [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) -Funktion gibt einen Zeiger auf die Dateiansicht zurück. Durch Dereferenzierung eines Zeigers im Adressbereich, der in **MapViewOfFile** angegeben ist, kann eine Anwendung Daten aus der Datei lesen und Daten in die Datei schreiben. Das Schreiben in die Dateiansicht führt zu Änderungen am Datei Zuordnungsobjekt. Das eigentliche Schreiben in die Datei auf dem Datenträger wird vom System verarbeitet. Die Daten werden nicht tatsächlich zu dem Zeitpunkt übertragen, zu dem das Datei Mapping-Objekt geschrieben wird. Stattdessen wird ein Großteil der Dateieingabe und-Ausgabe (e/a) zwischengespeichert, um die allgemeine Systemleistung zu verbessern. Anwendungen können dieses Verhalten überschreiben, indem Sie die [**flushviewoffile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) -Funktion aufrufen, um die sofortige Ausführung von Datenträger Transaktionen durch das System zu erzwingen.

Die [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) -Funktion funktioniert genau wie die [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) -Funktion, mit der Ausnahme, dass Sie es einem Prozess ermöglicht, die Basisadresse der Dateiansicht im virtuellen Adressraum des Prozesses im *lpvBase* -Parameter anzugeben. Wenn an der angegebenen Adresse nicht genügend Speicherplatz vorhanden ist, tritt ein Fehler auf. Wenn Sie also eine Datei derselben Adresse in mehreren Prozessen zuordnen müssen, sollten die Prozesse eine entsprechende Adresse aushandeln: der *lpvBase* -Parameter muss ein ganzzahliges Vielfaches der Granularität der systemarbeitsspeicherbelegung sein, oder der-Rückruf schlägt fehl. Verwenden Sie die [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) -Funktion, die die Elemente einer [**System \_ Informations**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) Struktur füllt, um die Granularität der Speicher Belegung des Systems zu ermitteln.

Eine Anwendung kann mehrere Datei Sichten aus demselben Datei Mapping-Objekt erstellen. Eine Dateiansicht kann eine andere Größe aufweisen als das Datei Zuordnungsobjekt, von dem Sie abgeleitet ist, aber Sie muss kleiner als das Datei Zuordnungsobjekt sein. Der Offset, der von den Parametern *dwoffsethigh* und *dwoffsetlow* von [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) angegeben wird, muss ein Vielfaches der Zuordnungs Granularität des Systems sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Ansicht in einer Datei](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
