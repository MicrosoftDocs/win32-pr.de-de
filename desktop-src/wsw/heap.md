---
title: Heap
description: Ein Heap verfolgt eine Gruppe von Zuordnungen nach, die als Einheit frei werden.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Heapwebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a581d4173ed16423ac55e82d3dde356bad1e310047dd44d8f92fded0c6f458e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005930"
---
# <a name="heap"></a>Heap

Ein Heap verfolgt eine Gruppe von Zuordnungen nach, die als Einheit frei werden.

Dadurch können Sie komplexe Muster der Speicherzuweisung und -zuordnung vermeiden, wenn Sie die WWSAPI verwenden.


Jeder Nachricht ist ein Heap zugeordnet. Wenn eine Nachricht gesendet wird oder eine Nachricht empfangen wird, wird der Heap der Nachricht für alle Zuordnungen im Zusammenhang mit dieser bestimmten Nachricht verwendet. Nachdem eine Nachricht gesendet oder empfangen wurde, wird der Heap zurückgesetzt (wodurch alle Zuordnungen im Zusammenhang mit der jeweiligen Nachricht bereinigt werden).

Heaps können auch verwendet werden, um Nachrichtendaten getrennt von der Lebensdauer einer Nachricht zu speichern. Viele der APIs ermöglichen die Angabe des Heaps, der beim Lesen von Daten verwendet werden soll, geben explizite Kontrolle über die Lebensdauer aller gelesenen Daten.

Zuordnungen aus einem Heap sind garantiert an mindestens einer 8-Byte-Grenze ausgerichtet.

Null-Bytezuordnungen geben einen Zeiger zurück, der nicht NULL ist.

In Windows 7 wird ein von HeapCreate zurückgegebener Heap verwendet, wenn PageHeap aktiviert ist, um den Arbeitsspeicher zu verwalten. In diesem Fall wird [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) direkt HeapAlloc und [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) HeapDestroy zugewiesen.

Die folgende Enumeration wird mit dem Heap verwendet:

-   [**\_ \_ WS-HEAP-EIGENSCHAFTEN-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

Die folgenden Funktionen werden mit dem Heap verwendet:

-   [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**WsCreateHeap**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**WsFreeHeap**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**WsGetHeapProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

Das folgende Handle wird mit dem Heap verwendet:

-   [\_WS-HEAP](ws-heap.md)

Die folgenden Strukturen werden mit dem Heap verwendet:

-   [**\_WS-HEAPEIGENSCHAFTEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**\_WS-HEAP-EIGENSCHAFT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




