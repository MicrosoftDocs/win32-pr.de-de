---
description: 'Weitere Informationen finden Sie hier: Ablauf Verfolgungs Ereignisse der Speicherverwaltung'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Ablauf Verfolgungs Ereignisse für die Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ca05260b6c29ecae765c047691b81a26116fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355450"
---
# <a name="memory-management-tracing-events"></a>Ablauf Verfolgungs Ereignisse für die Speicherverwaltung

In diesem Abschnitt werden ausführliche Informationen zu den Details zu bestimmten Ablauf Verfolgungs Ereignissen der Speicherverwaltung beschrieben.

Die Ablauf Verfolgung für die Speicherverwaltung ist eine Funktion zur Problembehandlung, die in Binärdateien im Einzelhandel aktiviert werden kann, um bestimmte Speicher Verwaltungs Ereignisse mit minimalem mehr Aufwand Diese Funktion ermöglicht bessere Diagnosefunktionen für Entwickler und den Produktsupport. Die Ereignis Ablauf Verfolgung für die Speicherverwaltung unterstützt die Ablauf Verfolgung der Heap Zuordnung, Neuzuordnung und kostenlose Vorgänge

Die Ereignis Ablauf Verfolgung für die Speicherverwaltung verwendet die Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw), eine allgemeine, hoch Geschwindigkeits Ablauf Verfolgungs Funktion des Betriebssystems. Etw bietet einen Ablauf Verfolgungs Mechanismus für Ereignisse, die von Anwendungen im Benutzermodus und im Kernel Modus-Gerätetreibern ausgelöst werden. Etw kann die Protokollierung dynamisch aktivieren und deaktivieren, sodass eine ausführliche Ablauf Verfolgung in Produktionsumgebungen ohne Neustarts oder Anwendungs Neustarts problemlos durchgeführt werden kann. Die Ereignis Ablauf Verfolgung für die Speicherverwaltung mithilfe von etw wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt. Allgemeine Informationen zu etw finden Sie unter verbessertes [Debugging und Leistungsoptimierung mit etw](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

In der folgenden Liste finden Sie ausführliche Informationen zu den einzelnen Ablauf Verfolgungs Ereignissen für die Speicherverwaltung. Klicken Sie auf den Ereignis Namen, um weitere Informationen zu einem beliebigen Ereignis zu erhalten.



| Veranstaltungsname                                                  | BESCHREIBUNG                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [**etw- \_ Heap \_ Ereignis \_ Zuweisung**](etw-heap-event-alloc.md)     | Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap Zuordnungs Vorgang.    |
| [**etw- \_ Heap- \_ Ereignis \_ frei**](etw-heap-event-free.md)       | Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap freien Vorgang.          |
| [**rezuweisung von etw- \_ Heap \_ Ereignissen \_**](etw-heap-event-realloc.md) | Ablauf Verfolgungs Ereignis der Speicherverwaltung für einen Heap-neuzuordnungs Vorgang. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessertes Debugging und Leistungsoptimierung mit ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
