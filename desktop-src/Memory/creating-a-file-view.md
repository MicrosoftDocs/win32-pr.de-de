---
description: Um die Daten aus einer Datei dem virtuellen Speicher eines Prozesses zuzuordnen, müssen Sie eine Ansicht der Datei erstellen.
ms.assetid: b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4
title: Erstellen einer Dateiansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eadae741e9f74e8a3e1cd68006100d6acf82aad5019a8d31b18a7761c5620b69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067880"
---
# <a name="creating-a-file-view"></a>Erstellen einer Dateiansicht

Um die Daten aus einer Datei dem virtuellen Speicher eines Prozesses zuzuordnen, müssen Sie eine Ansicht der Datei erstellen. Die Funktionen [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) und [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) verwenden das von [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) zurückgegebene Dateizuordnungsobjekthandle, um eine Ansicht der Datei oder einen Teil der Datei im virtuellen Adressraum des Prozesses zu erstellen. Diese Funktionen schlagen fehl, wenn die Zugriffsflags mit denen in Konflikt geraten, die beim Erstellen des Dateizuordnungsobjekts durch **CreateFileMapping** angegeben wurden.

Die [**MapViewOfFile-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) gibt einen Zeiger auf die Dateiansicht zurück. Durch Dereferenzieren eines Zeigers im Adressbereich, der in **MapViewOfFile** angegeben ist, kann eine Anwendung Daten aus der Datei lesen und Daten in die Datei schreiben. Das Schreiben in die Dateiansicht führt zu Änderungen am Dateizuordnungsobjekt. Das eigentliche Schreiben in die Datei auf dem Datenträger wird vom System verarbeitet. Daten werden zu dem Zeitpunkt, zu dem das Dateizuordnungsobjekt geschrieben wird, nicht tatsächlich übertragen. Stattdessen wird ein Großteil der Dateieingabe und -ausgabe (E/A) zwischengespeichert, um die allgemeine Systemleistung zu verbessern. Anwendungen können dieses Verhalten überschreiben, indem sie die [**FlushViewOfFile-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) aufrufen, um das System zum sofortigen Ausführen von Datenträgertransaktionen zu zwingen.

Die [**MapViewOfFileEx-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) funktioniert genau wie die [**MapViewOfFile-Funktion,**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) mit der Ausnahme, dass ein Prozess die Basisadresse der Ansicht der Datei im virtuellen Adressraum des Prozesses im *lpvBase-Parameter* angeben kann. Wenn an der angegebenen Adresse nicht genügend Speicherplatz vorhanden ist, schlägt der Aufruf fehl. Wenn Sie daher eine Datei in mehreren Prozessen derselben Adresse zuordnen müssen, sollten die Prozesse eine geeignete Adresse aushandeln: Der *lpvBase-Parameter* muss ein integrales Vielfaches der Granularität der Systemspeicherbelegung sein, andernfalls schlägt der Aufruf fehl. Um die Granularität der Speicherbelegung des Systems zu erhalten, verwenden Sie die [**GetSystemInfo-Funktion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) die die Member einer [**SYSTEM \_ INFO-Struktur**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) auffüllt.

Eine Anwendung kann mehrere Dateiansichten aus demselben Dateizuordnungsobjekt erstellen. Eine Dateiansicht kann eine andere Größe als das Dateizuordnungsobjekt aufweisen, von dem sie abgeleitet wird, muss aber kleiner als das Dateizuordnungsobjekt sein. Der durch die Parameter *dwOffsetHigh* und *dwOffsetLow* von [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) angegebene Offset muss ein Vielfaches der Zuordnungsgranularität des Systems sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Ansicht in einer Datei](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
