---
description: Der gesamte Arbeitsspeicher, den ein Prozess mithilfe der Speicherbelegungsfunktionen (HeapAlloc, VirtualAlloc, GlobalAlloc oder LocalAlloc) zuordnet, ist nur für den Prozess zugänglich.
ms.assetid: b47200dc-6824-4fd8-8d9f-2aaa439a74ff
title: Umfang des zugeordneten Arbeitsspeichers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f06b0ee3f9446962bb508c23d4c5542fd16168027c5913b63438d16b6cea910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067670"
---
# <a name="scope-of-allocated-memory"></a>Umfang des zugeordneten Arbeitsspeichers

Der gesamte Arbeitsspeicher, den ein Prozess mithilfe der Speicherbelegungsfunktionen [**(HeapAlloc,**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)oder [**LocalAlloc)**](/windows/desktop/api/WinBase/nf-winbase-localalloc)zuordnet, ist nur für den Prozess zugänglich. Der von einer DLL belegte Arbeitsspeicher wird jedoch im Adressraum des Prozesses zugeordnet, der die DLL aufgerufen hat, und ist für andere Prozesse, die dieselbe DLL verwenden, nicht zugänglich. Um freigegebenen Arbeitsspeicher zu erstellen, müssen Sie die Dateizuordnung verwenden.

Die Zuordnung benannter Dateien bietet eine einfache Möglichkeit, einen Block mit gemeinsam genutzten Speicher zu erstellen. Ein Prozess kann einen Namen angeben, wenn er die [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) verwendet, um ein Dateizuordnungsobjekt zu erstellen. Andere Prozesse können den gleichen Namen für die **CreateFileMapping-** oder [**OpenFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) angeben, um ein Handle für das Zuordnungsobjekt abzurufen.

Jeder Prozess gibt sein Handle für das Dateizuordnungsobjekt in der [**MapViewOfFile-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) an, um eine Ansicht der Datei einem eigenen Adressraum zuzuordnen. Die Ansichten aller Prozesse für ein einzelnes Dateizuordnungsobjekt werden den gleichen teilbaren Seiten des physischen Speichers zugeordnet. Die virtuellen Adressen der zugeordneten Ansichten können jedoch von Prozess zu Prozess variieren, es sei denn, die [**MapViewOfFileEx-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) wird verwendet, um die Ansicht an einer angegebenen Adresse zuzuordnen. Obwohl die Seiten des physischen Speichers, die für eine zugeordnete Dateiansicht verwendet werden, global sind, sind sie nicht global. Sie sind für Prozesse, die keine Ansicht der Datei zugeordnet haben, nicht zugänglich.

Alle Seiten, für die durch das Zuordnen einer Ansicht einer Datei ein Commit ausgeführt wurde, werden freigegeben, wenn der letzte Prozess mit einer Ansicht des Zuordnungsobjekts durch Aufrufen der [**UnmapViewOfFile-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) beendet oder die Zuordnung der Ansicht aufheben wird. Zu diesem Zeitpunkt wird die angegebene Datei (sofern vorhanden), die dem Zuordnungsobjekt zugeordnet ist, aktualisiert. Eine angegebene Datei kann auch zum Aktualisieren gezwungen werden, indem die [**FlushViewOfFile-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) aufgerufen wird.

Weitere Informationen finden Sie unter [Dateizuordnung.](file-mapping.md) Ein Beispiel für freigegebenen Speicher in einer DLL finden Sie unter [Using Shared Memory in a Dynamic-Link Library](../dlls/using-shared-memory-in-a-dynamic-link-library.md).

Wenn mehrere Prozesse Schreibzugriff auf freigegebenen Arbeitsspeicher haben, müssen Sie den Zugriff auf den Arbeitsspeicher synchronisieren. Weitere Informationen finden Sie unter [Synchronisierung.](../sync/synchronization.md)

 

 
