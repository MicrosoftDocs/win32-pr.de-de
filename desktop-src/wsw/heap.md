---
title: Heap
description: Ein Heap verfolgt eine Gruppe von Zuordnungen, die als Einheit freigegeben werden.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Heap-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391259"
---
# <a name="heap"></a>Heap

Ein Heap verfolgt eine Gruppe von Zuordnungen, die als Einheit freigegeben werden.

Auf diese Weise können Sie komplexe Muster der Zuordnung und Freigabe von Arbeitsspeicher vermeiden, wenn Sie wwsapi verwenden.


Jeder Nachricht ist ein Heap zugeordnet. Wenn eine Nachricht gesendet wird, oder wenn eine Nachricht empfangen wird, wird der Heap der Nachricht für alle Zuordnungen in Bezug auf die jeweilige Nachricht verwendet. Nachdem eine Nachricht gesendet oder empfangen wurde, wird der Heap zurückgesetzt (wodurch alle Zuordnungen bereinigt werden, die mit der jeweiligen Nachricht verknüpft sind).

Heaps können auch verwendet werden, um Nachrichten Daten getrennt von der Lebensdauer einer Nachricht zu speichern. Viele der API-Zulassungs Spezifikation des Heaps, der beim Lesen von Daten verwendet werden soll, ermöglichen eine explizite Kontrolle über die Lebensdauer von gelesenen Daten.

Die Zuweisung von Zuordnungen aus einem Heap wird garantiert an mindestens einer 8-Byte-Grenze ausgerichtet.

Null-Byte Zuordnungen geben einen nicht-NULL-Zeiger zurück.

In Windows 7 wird ein von HeapCreate zurückgegebener Heap verwendet, um den Arbeitsspeicher zu verwalten. In diesem Fall wird " [**wsalloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) " direkt zu "heapzuzuordnungen" und " [**wsreseethap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) " zu "HeapDestroy" zugeordnet.

Die folgende Enumeration wird mit dem Heap verwendet:

-   [**WS- \_ Heap- \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

Die folgenden Funktionen werden mit dem Heap verwendet:

-   [**Wsalloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**Wscreateheap**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**Wsfreeheap**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**Wsgeder approperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**Wsreabthap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

Das folgende Handle wird mit dem Heap verwendet:

-   [WS- \_ Heap](ws-heap.md)

Die folgenden Strukturen werden mit dem Heap verwendet:

-   [**Eigenschaften von WS- \_ Heap \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**WS- \_ Heap- \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




