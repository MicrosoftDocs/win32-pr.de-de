---
description: Weitere Informationen finden Sie unter Ablaufverfolgungsereignisse für die Speicherverwaltung.
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Ablaufverfolgungsereignisse für die Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb395082d46ddd668cbb91ee396f211a4055472f49682ab75efc90cedca7ad5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809007"
---
# <a name="memory-management-tracing-events"></a>Ablaufverfolgungsereignisse für die Speicherverwaltung

In diesem Abschnitt werden ausführliche Informationen zu bestimmten Ablaufverfolgungsereignissen für die Speicherverwaltung beschrieben.

Die Speicherverwaltungsablaufverfolgung ist ein Feature zur Problembehandlung, das in Binärdateien für den Einzelhandel aktiviert werden kann, um bestimmte Speicherverwaltungsereignisse mit minimalem Aufwand nachzuverfolgen. Dieses Feature ermöglicht bessere Diagnosefunktionen für Entwickler und Produktsupport. Die Ereignisablaufverfolgung für die Speicherverwaltung unterstützt die Ablaufverfolgung von Heapzuordnung, Neuzuordnung und freien Vorgängen.

Die Ereignisablaufverfolgung für die Speicherverwaltung verwendet die Ereignisablaufverfolgung für Windows (ETW), eine allgemeine Hochgeschwindigkeits-Ablaufverfolgungsfunktion, die vom Betriebssystem bereitgestellt wird. ETW bietet einen Ablaufverfolgungsmechanismus für Ereignisse, die sowohl von Benutzermodusanwendungen als auch von Gerätetreibern im Kernelmodus ausgelöst werden. ETW kann die Protokollierung dynamisch aktivieren und deaktivieren, sodass eine detaillierte Ablaufverfolgung in Produktionsumgebungen problemlos durchgeführt werden kann, ohne dass Neustarts oder Neustarts der Anwendung erforderlich sind. Die Speicherverwaltungsereignisablaufverfolgung mit ETW wird auf Windows 7, Windows Server 2008 R2 und höher unterstützt. Allgemeine Informationen zu ETW finden Sie unter [Improve Debugging and Performance Tuning With ETW (Verbessern des Debuggens und der Leistungsoptimierung mit ETW).](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)

Die folgende Liste enthält ausführliche Informationen zu jedem Ablaufverfolgungsereignis für die Speicherverwaltung. Klicken Sie auf den Ereignisnamen, um weitere Informationen zu jedem Ereignis zu erfahren.



| Veranstaltungsname                                                  | BESCHREIBUNG                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [**ETW \_ HEAP \_ EVENT \_ ALLOC**](etw-heap-event-alloc.md)     | Ablaufverfolgungsereignis für die Speicherverwaltung für einen Heapzuordnungsvorgang.    |
| [**ETW \_ HEAP \_ EVENT \_ FREE**](etw-heap-event-free.md)       | Ablaufverfolgungsereignis für die Speicherverwaltung für einen heapfreien Vorgang.          |
| [**ETW \_ HEAP \_ EVENT \_ REALLOC**](etw-heap-event-realloc.md) | Ablaufverfolgungsereignis für die Speicherverwaltung für einen Heap-Neuzuordnungsvorgang. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessertes Debugging und Leistungsoptimierung mit ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
