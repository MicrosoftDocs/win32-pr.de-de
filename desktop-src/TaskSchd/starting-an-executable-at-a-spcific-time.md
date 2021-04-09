---
title: Starten einer ausführbaren Datei zu einem bestimmten Zeitpunkt
description: Das Schreiben einer Aufgabe, die eine ausführbare Datei zu einem bestimmten Zeitpunkt startet, erfolgt durch Definieren eines Zeit Auslösers und einer ausführbaren Aktion.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Taskplaner Beispiele Taskplaner, Zeit Auslösung
- Taskplaner Beispiele Taskplaner, Starten einer ausführbaren Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856500"
---
# <a name="starting-an-executable-at-a-specific-time"></a><span data-ttu-id="49958-105">Starten einer ausführbaren Datei zu einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="49958-105">Starting an Executable at a Specific Time</span></span>

<span data-ttu-id="49958-106">Das Schreiben einer Aufgabe, die eine ausführbare Datei zu einem bestimmten Zeitpunkt startet, erfolgt durch Definieren eines Zeit Auslösers und einer ausführbaren Aktion.</span><span class="sxs-lookup"><span data-stu-id="49958-106">Writing a task that starts an executable at a specific time is done by defining a time trigger and an executable action.</span></span>

## <a name="start-boundary"></a><span data-ttu-id="49958-107">Start Grenze</span><span class="sxs-lookup"><span data-stu-id="49958-107">Start Boundary</span></span>

<span data-ttu-id="49958-108">Es ist wichtig zu beachten, dass ein Zeit Trigger von anderen zeitbasierten Triggern abweicht, dass er ausgelöst wird, wenn der Trigger durch seine Start Grenze aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="49958-108">It is important to note that a time trigger is different from other time-based triggers in that it is fired when the trigger is activated by its start boundary.</span></span> <span data-ttu-id="49958-109">Andere Zeitbasierte Trigger werden über die Start Grenze aktiviert, aber Sie beginnen nicht mit der Ausführung ihrer Aktionen (in diesem Fall das Starten einer ausführbaren Datei), bis ein geplantes Datum erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="49958-109">Other time-based triggers are activated by their start boundary, but they do not start performing their actions (in this case starting an executable) until a scheduled date is reached.</span></span>

## <a name="time-trigger-examples"></a><span data-ttu-id="49958-110">Beispiele für Zeit Beispiele</span><span class="sxs-lookup"><span data-stu-id="49958-110">Time Trigger Examples</span></span>

<span data-ttu-id="49958-111">In den folgenden Beispielen wird der Editor 30 Sekunden nach der Aktivierung der Aufgabe gestartet:</span><span class="sxs-lookup"><span data-stu-id="49958-111">The following examples start Notepad 30 seconds after the task is activated:</span></span>

-   [<span data-ttu-id="49958-112">Beispiel für Zeit Auslösung (C++)</span><span class="sxs-lookup"><span data-stu-id="49958-112">Time Trigger Example (C++)</span></span>](time-trigger-example--c---.md)
-   [<span data-ttu-id="49958-113">Beispiel für Zeit Auslösung (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="49958-113">Time Trigger Example (Scripting)</span></span>](time-trigger-example--scripting-.md)
-   [<span data-ttu-id="49958-114">Beispiel für Zeit Auslösung (XML)</span><span class="sxs-lookup"><span data-stu-id="49958-114">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="49958-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49958-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49958-116">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="49958-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




