---
description: Der gesamte Arbeitsspeicher, der von einem Prozess mithilfe der Speicher Belegungs Funktionen (HeapAlloc, VirtualAlloc, GlobalAlloc oder LocalAlloc) zugewiesen wird, ist nur für den Prozess zugänglich.
ms.assetid: b47200dc-6824-4fd8-8d9f-2aaa439a74ff
title: Bereich von zugewiesener Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d2db67a04c019683e737d0f9c581ce8d16b800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214760"
---
# <a name="scope-of-allocated-memory"></a>Bereich von zugewiesener Arbeitsspeicher

Der gesamte Arbeitsspeicher, der von einem Prozess mithilfe der Speicher Belegungs Funktionen ( [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc), [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)oder [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)) zugewiesen wird, ist nur für den Prozess zugänglich. Der durch eine DLL zugewiesene Arbeitsspeicher wird jedoch im Adressraum des Prozesses zugeordnet, der die dll aufgerufen hat, und für andere Prozesse, die dieselbe DLL verwenden, kann nicht darauf zugegriffen werden. Zum Erstellen von frei gegebenem Speicher müssen Sie die Datei Zuordnung verwenden.

Die benannte Datei Zuordnung bietet eine einfache Möglichkeit, einen Block von frei gegebenem Speicher zu erstellen. Ein Prozess kann einen Namen angeben, wenn er mithilfe [**der Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) "Funktion erstellen" ein Datei Zuordnung-Objekt erstellt. Andere Prozesse **können den gleichen** Namen für die Funktion "-Funktion" oder " [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) " angeben, um ein Handle für das Mapping-Objekt zu erhalten.

Jeder Prozess gibt das Handle für das Datei Zuordnungs Objekt in der [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) -Funktion an, um eine Ansicht der Datei einem eigenen Adressraum zuzuordnen. Die Sichten aller Prozesse für ein einzelnes Datei Zuordnungsobjekt werden den gleichen freigegebenen Seiten des physischen Speichers zugeordnet. Allerdings können die virtuellen Adressen der zugeordneten Sichten von einem Prozess zu einem anderen abweichen, es sei denn, die [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) -Funktion wird verwendet, um die Ansicht an einer bestimmten Adresse zuzuordnen. Auch wenn es möglich ist, sind die Seiten des physischen Speichers, der für eine zugeordnete Dateiansicht verwendet wird, nicht global. Es sind keine Prozesse verfügbar, die keine Ansicht der Datei zugeordnet haben.

Alle Seiten, die durch Zuordnen einer Ansicht einer Datei committet werden, werden freigegeben, wenn der letzte Prozess mit einer Ansicht des Zuordnungs Objekts die Ansicht beendet oder die Zuordnung aufgehoben wird, indem die [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) -Funktion aufgerufen wird. Zu diesem Zeitpunkt wird die angegebene Datei (sofern vorhanden), die dem Mapping-Objekt zugeordnet ist, aktualisiert. Eine angegebene Datei kann auch durch Aufrufen der [**flushviewoffile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) -Funktion aktualisiert werden.

Weitere Informationen finden Sie unter [Datei Zuordnung](file-mapping.md). Ein Beispiel für freigegebenen Arbeitsspeicher in einer DLL finden Sie unter Verwenden von frei gegebenem Arbeits [Speicher in einer Dynamic-Link-Bibliothek](../dlls/using-shared-memory-in-a-dynamic-link-library.md).

Wenn mehrere Prozesse über Schreibzugriff auf gemeinsam genutzten Speicher verfügen, müssen Sie den Zugriff auf den Arbeitsspeicher synchronisieren. Weitere Informationen finden Sie unter [Synchronisierung](../sync/synchronization.md).

 

 
