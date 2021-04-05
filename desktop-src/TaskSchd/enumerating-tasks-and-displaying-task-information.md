---
title: Auflisten von Aufgaben und Anzeigen von Aufgabeninformationen
description: Zum Anzeigen von Informationen zu einer Aufgabe, z. b. Aufgaben Name, Status oder Zeitpunkt der letzten Ausführung der Aufgabe, werden die ausgeführten Tasks oder die Tasks in einem Aufgaben Ordner aufgelistet und die gewünschten Informationen angezeigt.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- Aufzählen von Aufgaben Taskplaner
- Taskplaner Beispiele Taskplaner, Auflisten von Aufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707278"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a><span data-ttu-id="11c72-105">Auflisten von Aufgaben und Anzeigen von Aufgabeninformationen</span><span class="sxs-lookup"><span data-stu-id="11c72-105">Enumerating Tasks and Displaying Task Information</span></span>

<span data-ttu-id="11c72-106">Zum Anzeigen von Informationen zu einer Aufgabe, z. b. Aufgaben Name, Status oder Zeitpunkt der letzten Ausführung der Aufgabe, werden die ausgeführten Tasks oder die Tasks in einem Aufgaben Ordner aufgelistet und die gewünschten Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11c72-106">Displaying information about a task, such as the task name, state, or the last time the task was run, is done by enumerating through running tasks or the tasks in a task folder and displaying the desired information.</span></span>

## <a name="accessing-properties-of-registered-tasks"></a><span data-ttu-id="11c72-107">Zugreifen auf Eigenschaften registrierter Tasks</span><span class="sxs-lookup"><span data-stu-id="11c72-107">Accessing Properties of Registered Tasks</span></span>

<span data-ttu-id="11c72-108">Um den Eigenschafts Wert einer registrierten Aufgabe anzuzeigen, müssen Sie eine Verbindung mit dem Taskplaner-Dienst herstellen und dann eine Instanz des Aufgaben Ordners mit den Tasks, über die Sie Informationen erhalten möchten, erhalten.</span><span class="sxs-lookup"><span data-stu-id="11c72-108">To display a registered task's property value, you must connect to the Task Scheduler service, and then get an instance of the task folder that contains the tasks you want information about.</span></span> <span data-ttu-id="11c72-109">Anschließend erhalten Sie eine Sammlung aller registrierten Tasks im Aufgaben Ordner.</span><span class="sxs-lookup"><span data-stu-id="11c72-109">You then get a collection of all the registered tasks in the task folder.</span></span> <span data-ttu-id="11c72-110">Anschließend durchlaufen Sie jede registrierte Aufgabe und erhalten und zeigen einen Eigenschafts Wert für jede Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="11c72-110">Then you enumerate through each registered task and get and display a property value for each task.</span></span>

## <a name="accessing-properties-of-running-tasks"></a><span data-ttu-id="11c72-111">Zugreifen auf Eigenschaften von laufenden Tasks</span><span class="sxs-lookup"><span data-stu-id="11c72-111">Accessing Properties of Running Tasks</span></span>

<span data-ttu-id="11c72-112">Um den Eigenschafts Wert einer ausgewerenden Aufgabe anzuzeigen, müssen Sie eine Verbindung mit dem Taskplaner-Dienst herstellen und dann eine Auflistung aller ausgelaufenden Tasks (einschließlich oder ausschließen ausgeblendeter Tasks) erhalten.</span><span class="sxs-lookup"><span data-stu-id="11c72-112">To display a running task's property value, you must connect to the Task Scheduler service, and then get a collection of all the running tasks (including or excluding hidden tasks).</span></span> <span data-ttu-id="11c72-113">Anschließend durchlaufen Sie jede ausgestellte Aufgabe und erhalten und zeigen einen Eigenschafts Wert für jede Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="11c72-113">Then you enumerate through each running task and get and display a property value for each task.</span></span>

## <a name="example"></a><span data-ttu-id="11c72-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="11c72-114">Example</span></span>

<span data-ttu-id="11c72-115">In den folgenden Beispielen werden Aufgaben aufgelistet und der Name und der Zustand der Aufgaben angezeigt:</span><span class="sxs-lookup"><span data-stu-id="11c72-115">The following examples enumerate tasks and display the name and state of the tasks:</span></span>

-   [<span data-ttu-id="11c72-116">Anzeigen von Aufgaben Namen und-Zuständen (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="11c72-116">Displaying Task Names and States (Scripting)</span></span>](displaying-task-names-and-state--scripting-.md)
-   [<span data-ttu-id="11c72-117">Anzeigen von Aufgaben Namen und-Status (C++)</span><span class="sxs-lookup"><span data-stu-id="11c72-117">Displaying Task Names and State (C++)</span></span>](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a><span data-ttu-id="11c72-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11c72-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11c72-119">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="11c72-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




