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
# <a name="memory-management-tracing-events"></a><span data-ttu-id="0755f-103">Ablauf Verfolgungs Ereignisse für die Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="0755f-103">Memory Management Tracing Events</span></span>

<span data-ttu-id="0755f-104">In diesem Abschnitt werden ausführliche Informationen zu den Details zu bestimmten Ablauf Verfolgungs Ereignissen der Speicherverwaltung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0755f-104">This section describes detailed information on specific Memory management tracing event details.</span></span>

<span data-ttu-id="0755f-105">Die Ablauf Verfolgung für die Speicherverwaltung ist eine Funktion zur Problembehandlung, die in Binärdateien im Einzelhandel aktiviert werden kann, um bestimmte Speicher Verwaltungs Ereignisse mit minimalem mehr Aufwand</span><span class="sxs-lookup"><span data-stu-id="0755f-105">Memory management tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain memory management events with minimal overhead.</span></span> <span data-ttu-id="0755f-106">Diese Funktion ermöglicht bessere Diagnosefunktionen für Entwickler und den Produktsupport.</span><span class="sxs-lookup"><span data-stu-id="0755f-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="0755f-107">Die Ereignis Ablauf Verfolgung für die Speicherverwaltung unterstützt die Ablauf Verfolgung der Heap Zuordnung, Neuzuordnung und kostenlose Vorgänge</span><span class="sxs-lookup"><span data-stu-id="0755f-107">Memory management event tracing supports tracing heap allocation, reallocation, and free operations.</span></span>

<span data-ttu-id="0755f-108">Die Ereignis Ablauf Verfolgung für die Speicherverwaltung verwendet die Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw), eine allgemeine, hoch Geschwindigkeits Ablauf Verfolgungs Funktion des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="0755f-108">Memory management event tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="0755f-109">Etw bietet einen Ablauf Verfolgungs Mechanismus für Ereignisse, die von Anwendungen im Benutzermodus und im Kernel Modus-Gerätetreibern ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="0755f-109">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="0755f-110">Etw kann die Protokollierung dynamisch aktivieren und deaktivieren, sodass eine ausführliche Ablauf Verfolgung in Produktionsumgebungen ohne Neustarts oder Anwendungs Neustarts problemlos durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0755f-110">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="0755f-111">Die Ereignis Ablauf Verfolgung für die Speicherverwaltung mithilfe von etw wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0755f-111">Memory management event tracing using ETW is supported on Windows 7 , Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="0755f-112">Allgemeine Informationen zu etw finden Sie unter verbessertes [Debugging und Leistungsoptimierung mit etw](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="0755f-112">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="0755f-113">In der folgenden Liste finden Sie ausführliche Informationen zu den einzelnen Ablauf Verfolgungs Ereignissen für die Speicherverwaltung.</span><span class="sxs-lookup"><span data-stu-id="0755f-113">The following list provides detailed information for each memory management tracing event.</span></span> <span data-ttu-id="0755f-114">Klicken Sie auf den Ereignis Namen, um weitere Informationen zu einem beliebigen Ereignis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0755f-114">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="0755f-115">Veranstaltungsname</span><span class="sxs-lookup"><span data-stu-id="0755f-115">Event Name</span></span>                                                  | <span data-ttu-id="0755f-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0755f-116">Description</span></span>                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="0755f-117">**etw- \_ Heap \_ Ereignis \_ Zuweisung**</span><span class="sxs-lookup"><span data-stu-id="0755f-117">**ETW\_HEAP\_EVENT\_ALLOC**</span></span>](etw-heap-event-alloc.md)     | <span data-ttu-id="0755f-118">Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap Zuordnungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0755f-118">Memory management tracing event for a heap allocation operation.</span></span>    |
| [<span data-ttu-id="0755f-119">**etw- \_ Heap- \_ Ereignis \_ frei**</span><span class="sxs-lookup"><span data-stu-id="0755f-119">**ETW\_HEAP\_EVENT\_FREE**</span></span>](etw-heap-event-free.md)       | <span data-ttu-id="0755f-120">Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap freien Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0755f-120">Memory management tracing event for a heap free operation.</span></span>          |
| [<span data-ttu-id="0755f-121">**rezuweisung von etw- \_ Heap \_ Ereignissen \_**</span><span class="sxs-lookup"><span data-stu-id="0755f-121">**ETW\_HEAP\_EVENT\_REALLOC**</span></span>](etw-heap-event-realloc.md) | <span data-ttu-id="0755f-122">Ablauf Verfolgungs Ereignis der Speicherverwaltung für einen Heap-neuzuordnungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0755f-122">Memory management tracing event for a heap re-allocation operation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0755f-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0755f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0755f-124">Verbessertes Debugging und Leistungsoptimierung mit ETW</span><span class="sxs-lookup"><span data-stu-id="0755f-124">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
