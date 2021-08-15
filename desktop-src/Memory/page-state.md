---
description: Die Seiten des virtuellen Adressraums eines Prozesses können einen der folgenden Zustände haben.
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: Seitenstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ec9c162220cd0c1accdb35e35309082a2e94c4af6023af7e7d9d7cd55be620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386403"
---
# <a name="page-state"></a>Seitenstatus

Die Seiten des virtuellen Adressraums eines Prozesses können einen der folgenden Zustände haben.



| State     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kostenlos      | Für die Seite wird weder ein Committed noch ein Reservierter seitenaufruft. Der Prozess kann nicht auf die Seite zugegriffen werden. Sie kann reserviert, ausgeführt oder gleichzeitig reserviert und ausgeführt werden. Der Versuch, von einer kostenlosen Seite zu lesen oder auf diese zu schreiben, führt zu einer Zugriffsverletzungsausnahme. <br/> Ein Prozess kann die [**VirtualFree-**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) oder [**VirtualFreeEx-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) verwenden, um reservierte oder ausgeführte Seiten seines Adressraums frei zu geben und in den freien Zustand zurück zu setzen.<br/>                                                                                                                                                                                                                                                                                                                              |
| Reserviert  | Die Seite wurde für die zukünftige Verwendung reserviert. Der Adressbereich kann nicht von anderen Zuordnungsfunktionen verwendet werden. Auf die Seite kann nicht zugegriffen werden, und ihr ist kein physischer Speicher zugeordnet. Es ist verfügbar, um ein Committed zu erhalten. <br/> Ein Prozess kann die [**VirtualAlloc-**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) oder [**VirtualAllocEx-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) verwenden, um Seiten seines Adressraums zu reservieren und später einen Commit für die reservierten Seiten zu erstellen. Er kann [**VirtualFree oder**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) verwenden, um dieCommits für seiten mit ausgeführtem Committed zu decommitieren und in den reservierten Zustand zurück zu setzen.<br/>                                                                                                                                                                                                                          |
| Committet | Arbeitsspeichergebühren wurden aus der Gesamtgröße von RAM- und Pagingdateien auf dem Datenträger zugeordnet. Auf die Seite kann zugegriffen werden, und der Zugriff wird durch eine der [Speicherschutzkonst constants gesteuert.](memory-protection-constants.md) Das System initialisiert und lädt jede Seite, für die ein Committed unternommen wurde, nur beim ersten Versuch, diese Seite zu lesen oder zu schreiben, in den physischen Speicher. Wenn der Prozess beendet wird, gibt das System den Speicher für seiten frei, für die ein Committed() übermittelt wurde. <br/> Ein Prozess kann [**VirtualAlloc oder**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) verwenden, um physische Seiten aus einer reservierten Region zu commiten. Sie können Seiten auch gleichzeitig reservieren und ausführen.<br/> Die [**Funktionen GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [**und LocalAlloc weisen**](/windows/desktop/api/WinBase/nf-winbase-localalloc) Seiten mit Lese-/Schreibzugriff zu, für die ein Committed verwendet wurde.<br/> |



 

 

 
